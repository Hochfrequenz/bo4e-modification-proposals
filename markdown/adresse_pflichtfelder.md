|**Datum**|**Autor**|**bestehende Doku**|**Link**|
|---------|---------|-------------------|--------|
|09. Dezember 2020|Hochfrequenz Unternehmensberatung GmbH|[bo4e.de](https://www.bo4e.de/dokumentation/komponenten/com-adresse)|[Github](https://github.com/Hochfrequenz/bo4e-modification-proposals/blob/master/markdown/adresse_pflichtfelder.md)|

# Anpassung der Pflichtfelder im COM Adresse
Wir schlagen vor, in der Komponente `Adresse` die Strasse und Hausnummer nicht mehr als Pflichtfelder anzugeben.
Wir schlagen außerdem vor analog zur `messadresse`/`geoadresse`/`katasteradresse` im BO Messlokation eine XOR-Validierung einzuführen, dass entweder Straße und Hausnummer (exklusiv) oder ein Postfach angegeben wird, wenn diese angegeben werden.

## Begründung
Für eine gültige Adresse in Deutschland sind die Minimalanforderung eine Postleitzahl und Ortsangabe. Dies ist bspw. der Fall bei größeren Insitutionen wie Universitäten oder Firmen oder bei Postfächern die keine eigene Nummer, sondern eine spezielle Postleitzahl vergeben bekommen.

Gleichzeitig wird ermöglicht ein Postfach anzugeben ohne dass zusätzlich noch die Angabe von Strasse und Hausnummer verlangt wird.

## Komplette Liste aller Änderungen
|**#**|**Betroffenes COM**|**Vorher**|**Nachher**|
|-----|-------------------------------|----------|-----------|
|0| Adresse | `strasse`: `String[1]` | `strasse`: `String[0.. 1]` |
|1| Adresse | `hausnummer`: `String[1]` | `hausnummer`: `String[0.. 1]` |
