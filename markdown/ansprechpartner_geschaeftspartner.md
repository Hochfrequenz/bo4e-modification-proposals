|**Datum**|**Autor**|**bestende Doku**|**Link**|
|---------|---------|-----------------|--------|
|27. Mai 2021|Hochfrequenz Unternehmensberatung GmbH|[bo4e.de](https://www.bo4e.de/dokumentation/geschaeftsobjekte/bo-ansprechpartner)|[Github](https://github.com/Hochfrequenz/bo4e-modification-proposals/blob/master/markdown/ansprechpartner_geschaeftspartner.md)|

# Kardinalität von Geschaeftspartner fehlt

Wir schlagen vor, im Geschäftsobjekt `Ansprechpartner` die Kardinalität von `[1]` zwischen Ansprechpartner und Geschaeftspartner zu ergänzen. 


## Begründung
Die Kardinalität ist eine wichtige Information für das Konzipieren einer Datenbankstruktur.
Ohne diese kann keine Relation zwischen Ansprechpartner und Geschaeftspartner erstellt werden.

## Komplette Liste aller Änderungen
|**#**|**Betroffenes Geschäftsobjekt**|**Vorher**|**Nachher**|
|-----|-------------------------------|----------|-----------|
|0| Ansprechpartner | keine Kardinalität zwischen Ansprechpartner und Geschaeftspartner | Kardinalität von `[1]` zwischen Ansprechpartner und Geschaeftspartner |