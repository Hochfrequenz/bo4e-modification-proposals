|**Datum**|**Autor**|**Link**|
|---------|---------|--------|
|26. August 2020|Hochfrequenz Unternehmensberatung GmbH|[Github](https://github.com/Hochfrequenz/bo4e-modification-proposals/blob/master/markdown/adresse_postleitzahl_string_not_int.md)|

# Modellierung der Postleitzahl als String im COM Adresse
Wir schlagen vor, in der Komponente `Adresse` die Postleitzahl als String und nicht als Integer zu modellieren.

## Begründung
Postleitzahlen sind keine Zahlen bei denen bspw. Rechenoperationen sinnvoll wären. Stattdessen handelt es sich um Schlüssel, die sich aus Zahlen zusammensetzen. Außerdem führt die Modellierung als Integer zu Problemen, wenn die Postleitzahlen mit 0 beginnen, wie z.B. in weiten Teilen Sachsens üblich.


## Komplette Liste aller Änderungen
|**#**|**Betroffenes COM**|**Vorher**|**Nachher**|
|-----|-------------------------------|----------|-----------|
|0| Adresse | `postleitzahl`: Integer\[1\] | `postleitzahl`: String\[1\] |