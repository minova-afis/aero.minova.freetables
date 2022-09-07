# MatchCode

Jede Stammdatenmaske besitzt das Feld MatchCode, in dem ein eindeutiges Kürzel für den anzulegenden Datensatz vergeben werden muss.
Wurde der Datensatz einmal gespeichert, kann der MatchCode nicht mehr verändert werden.
Er dient als Identifikation des Datensatzes z. B. bei der Eingabe von Adressen oder bei der Auswahl aus einer Liste.
In diesem Feld sollten Leerzeichen möglichst vermieden werden.

Zulässige Zeichen für MatchCodes sind:

Hex Code | Zeichen | Beschreibung
-------- | ------- | ------------
ASCII 0x32 |       | Space
ASCII 0x2A | * | Stern
ASCII 0x2C | , | Komma
ASCII 0x2E | . | Punkt
ASCII 0x2D | - | Minus
ASCII 0x2F | / | Schrägstrich
ASCII 0x30-0x39 | 0-9 | Zahlen
ASCII 0x41-0x5A | A-Z | Großbuchstaben
ASCII 0x5F | _ | Unterstrich
Unicode 0x00E4 | Ä | Groß Ä
Unicode 0x00FC | Ü | Groß Ü
Unicode 0x00F6 | Ö | Groß Ö
