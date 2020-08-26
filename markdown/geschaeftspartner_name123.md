|**Datum**|**Autor**|**bestende Doku**|**Link**|
|---------|---------|-----------------|--------|
|26. August 2020|Hochfrequenz Unternehmensberatung GmbH|[bo4e.de](https://www.bo4e.de/dokumentation/geschaeftsobjekte/bo-geschaftspartner)|[Github](https://github.com/Hochfrequenz/bo4e-modification-proposals/blob/master/markdown/geschaeftspartner_name123.md)|

# Ersetzen von `name1`, `name2`, `name3` im Geschäftsobjekt Geschaeftspartner durch intuitive Schlüssel
Wir schlagen vor, im Geschäftsobjekt `Geschaeftspartner` die Felder `name1`, `name2` und `name3` durch intuitiv verständliche Bezeichnungen in zwei neuen Komponenten namens `JuristischerPersonenName` und `PrivaterPersonenName` zu ersetzen.
 
## Begründung
Aktuell hängt die Bedeutung der Felder `name1/2/3` davon ab, ob es sich um einen gewerblichen Geschaeftspartner oder eine Privatperson handelt (die `gewerbekennzeichnung` also `true` oder `false` ist). Der Grund für diese schwer vermittelbare Mehrdeutigkeit erschließt sich nur aus der Nähe zum UTILMD-Format, in dem analog gewerbliche/private Geschäftspartner mit dem Qualifier `Z01` oder `Z02` versehen werden können, aus der sich dann die Bedeutung des Inhalts der einzelnen `NAD` Segmente ergibt.

Anders als EDIFACT ist JSON als Datenformat darauf ausgelegt, gut maschinen- **und** menschenlesbar zu sein. Auch die BO4E-Objekte sollten lesbar sein und folglich die Bedeutung der verwendeten Feldnamen ohne Hintergrundwissen in der Marktkommunikation ersichtlich sein. Bei den Feldern `name1`, `name2` und `name3` ist das aktuell nicht der Fall.

Wir schlagen vor, die Namensbestandteile für private und juristische Personen in zwei neue Komponenten `COM JuristischerPersonenname` und `COM PrivaterPersonenName` mit jeweils intuitiv verständlichen Bezeichnungen aufzutrennen und diese dann so in das Geschäftsobjekt Geschaeftspartner einzubetten, dass sie sich wechselseitig ausschließen. 

Dieses Vorgehen ist konsistent mit dem jetzigen BO Messlokation, wo genau eine Standortinformationen (Klassische Anschrift **oder** Geokoordinaten **oder** Katasteradresse) anzugeben ist. Die [Dokumentation](https://www.bo4e.de/dokumentation/geschaeftsobjekte/bo-messlokation) schreibt dazu:

> Achtung: Es darf immer nur eine Art der Ortsangabe vorhanden sein (entweder eine Adresse oder eine GeoKoordinate oder eine Katasteradresse.


## Komplette Liste aller Änderungen

### Die neue Komponente `JuristischerPersonenname`
|**\#**|**Format & Kardinalität**|**Fachliches Attribut**|**Bemerkung / Beispiel**|
|------|-------------------------|-----------------------|------------------------|
||`COM`|**JuristischerPersonenname**||
|0|`firmenname`|`String\[1\]`| Name der Firme, z.B. "Yellow Strom"|
|1|`erweiterungFirmenname`|`String\[0..1\]`| Erweiterung zum Firmennamen, z.B. "Bereich Süd"|
|2|`ergaenzungFirmenname`|`String\[0..1\]`| Ergänzungen zum Firmennamen, z.B. "und Afrika"|


|**\#**|**Betroffenes Geschäftsobjekt**|**Vorher**|**Nachher**|
|------|-------------------------------|----------|-----------|
|0| Geschaeftspartner | `name1` | "Erster Teil des Namens. Hier kann der Firmenname oder bei Privatpersonen beispielsweise der Nachname dagestellt werden. Beispiele: Yellow Strom GmbH oder Hagen" | _entfällt_ |
|1| Geschaeftspartner | `name2` | "Zweiter Teil des Namens. Hier kann der eine Erweiterung zum Firmennamen oder bei Privatpersonen beispielsweise der Vorname dagestellt werden. Beispiele: Bereich Süd oder Nina" | _entfällt_ |
|2| Geschaeftspartner | `name3` | "Dritter Teil des Namens. Hier können weitere Ergänzungen zum Firmennamen oder bei Privatpersonen Zusätze zum Namen dagestellt werden. Beispiele: und Afrika oder Sängerin" | _entfällt_ |