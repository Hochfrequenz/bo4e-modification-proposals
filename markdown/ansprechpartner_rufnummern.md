|**Datum**|**Autor**|**Link**|
|---------|---------|--------|
|26. August 2020|Hochfrequenz Unternehmensberatung GmbH|[Github](https://github.com/Hochfrequenz/bo4e-modification-proposals/blob/master/markdown/ansprechpartner_rufnummern.md)|

# Umbenennung des Feldes `rufnummer` im BO Ansprechpartner

Wir schlagen vor, im Geschäftsobjekt `Ansprechpartner` die Liste der Telefonnummern, unter denen der Ansprechpartner erreichbar ist  von `rufnummer` in `rufnummern` umzubenennen.

## Begründung
Durch die Verwendung des Plurals wird intuitiv klar, dass es sich um eine Liste/ein Array handelt.

## Komplette Liste aller Änderungen
|**#**|**Betroffenes Geschäftsobjekt**|**Vorher**|**Nachher**|
|-----|-------------------------------|----------|-----------|
|0| Ansprechpartner | `rufnummer` | `rufnummern` |