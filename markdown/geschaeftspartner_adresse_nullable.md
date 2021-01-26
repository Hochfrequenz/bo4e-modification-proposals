|**Datum**|**Autor**|**bestehende Doku**|**Link**|
|---------|---------|-------------------|--------|
|26. Januar 2021|Hochfrequenz Unternehmensberatung GmbH|[bo4e.de](https://www.bo4e.de/dokumentation/geschaeftsobjekte/bo-geschaftspartner)|[Github](https://github.com/Hochfrequenz/bo4e-modification-proposals/blob/master/markdown/geschaeftspartner_adresse_nullable.md)|

# Adresse im BO Geschäftspartner deutlich als optional kennzeichnen
Wir schlagen vor, in der Dokumentation des Geschäftsobjekts "Geschäftspartner" die Partneradresse deutlicher als optional zu kennzeichnen.

## Begründung
Aktuell geht weder aus dem Diagramm noch aus der tabellarischen Dokumentation eindeutig hervor, ob bzw. dass die Partneradresse optional ist.

Dass die Partneradresse optional ist, macht aus unserer Sicht v.a. für den vom Geschäftspartner abgeleiteten Marktteilnehmer Sinn, für den in der Praxis die Emailadresse zur Marktkommunikation deutlich relevanter ist als die postalische Adresse.

## Komplette Liste aller Änderungen
|**#**|**Betroffenes BO**|**Feld**|**Vorher**|**Nachher**|
|-----|-------------------|--------|----------|-----------|
|0| `Geschäftspartner` | `partneradresse`| Adresse des Geschäftspartners, ... | Optionale Adresse des Geschäftspartners, ...|
