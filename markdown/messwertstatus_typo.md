| **Datum**       | **Autor**                              | **bestende Doku**                                                             | **Link**                                                                                                          |
| --------------- | -------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| 27. August 2021 | Hochfrequenz Unternehmensberatung GmbH | [bo4e.de](https://www.bo4e.de/dokumentation/enumerations/enum-messwertstatus) | [Github](https://github.com/Hochfrequenz/bo4e-modification-proposals/blob/master/markdown/messwertstatus_typo.md) |

# Beheben des Typos im ENUM Messwertstatus

Wir schlagen vor, im ENUM `Messwertstatus` das Feld `VOLAEUFIGERWERT` in `VORLAEUFIGER_WERT` umzubenennen.
Wir schlagen vor, im ENUM `Messwertstatus` das Feld `ENERGIEMENGESUMMIERT` in `ENERGIEMENGE_SUMMIERT` umzubenennen.

## Begründung

Neben den fehlenden `R` in `VORLAEUFIGER_WERT` ist diese Schreibweise konsistent mit der Benamung der anderen Enums.

## Komplette Liste aller Änderungen

| **#** | **Betroffenes ENUM** | **Vorher**             | **Nachher**             |
| ----- | -------------------- | ---------------------- | ----------------------- |
| 0     | Messwertstatus       | `VOLAEUFIGERWERT`      | `VORLAEUFIGER_WERT`     |
| 0     | Messwertstatus       | `ENERGIEMENGESUMMIERT` | `ENERGIEMENGE_SUMMIERT` |
