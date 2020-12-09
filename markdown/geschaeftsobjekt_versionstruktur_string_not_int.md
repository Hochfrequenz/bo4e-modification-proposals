|**Datum**|**Autor**|**bestehende Doku**|**Link**|
|---------|---------|-------------------|--------|
|09. Dezember 2020|Hochfrequenz Unternehmensberatung GmbH|[bo4e.de](https://www.bo4e.de/dokumentation/komponenten/com-adresse)|[Github](https://github.com/Hochfrequenz/bo4e-modification-proposals/blob/master/markdown/geschaeftsobjekt_versionstruktur_string_not_int.md)|

# Anpassung der Pflichtfelder im BO Geschaeftsobjekt
Wir schlagen vor, im Geschäftsobjekt `Geschaeftsobjekt` die Versionstrukur als String und nicht als Integer zu modellieren.

## Begründung
Versionsnummern sind keine Zahlen bei denen bspw. Rechenoperationen sinnvoll wären. Stattdessen handelt es sich um Schlüssel, die sich aus Ziffern, Zeichen und Buchstaben zusammensetzen bspw. 2.0a. 

## Komplette Liste aller Änderungen
|**#**|**Betroffenes Geschäftsobjekt**|**Vorher**|**Nachher**|
|-----|-------------------------------|----------|-----------|
|0| Geschaeftsobjekt | `versionstruktur`: `Integer[1]`| `versionstruktur`: `String[1]` |