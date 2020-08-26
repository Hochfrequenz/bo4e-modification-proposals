|**Datum**|**Autor**|**bestehende Doku**|**Link**|
|---------|---------|-------------------|--------|
|26. August 2020|Hochfrequenz Unternehmensberatung GmbH|[bo4e.de](https://www.bo4e.de/dokumentation/geschaeftsobjekte/bo-geschaftspartner)|[Github](https://github.com/Hochfrequenz/bo4e-modification-proposals/blob/master/markdown/geschaeftspartner_geschaeftspartnerrolle.md)|

# Umbenennung des Feldes `geschaeftspartnerrolle` im BO Geschäftspartner

Wir schlagen vor, im Geschäftsobjekt `Geschaeftspartner` die Liste der Rollen, die der Geschäftspartner hat von `geschaeftspartnerrolle` in `geschaeftspartnerrollen` umzubenennen.

## Begründung
Durch die Verwendung des Plurals wird intuitiv klar, dass es sich um eine Liste/ein Array handelt.

## Komplette Liste aller Änderungen
|**#**|**Betroffenes Geschäftsobjekt**|**Vorher**|**Nachher**|
|-----|-------------------------------|----------|-----------|
|0| Geschaeftspartner | `geschaeftspartnerrolle` | `geschaeftspartnerrollen` |