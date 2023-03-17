# Platzhalter und Kürzel

Um die Bedienung von den verschiedenen Feldern zu vereifachen, nutzen wir Platzhalter und Kürzel. Diese machen schnelle und genaue Eingaben einfach. Nachfolgend werden die verschiedenen Felder und ihre Kürzel aufgelistet:

## Datums- und Zeitfelder

#### Datumsfelder

| Eingabe | Wert
|---|---
| `0` | heute
| `1` | der 1. des Monats im Dezember 2020 -> 01.12.2020
| `11` | der 1. Januar des Jahres im Dezember 2020 -> 01.01.2020
| `111` | der 1. des Monats November im aktuellen Jahr -> 01.11.2020
| `102` | der 1. Februar des aktuellen Jahres -> 01.02.2020
| `1205` | der 12. Mai des aktuellen Jahres -> 12.05.2020
| `80921` | der 8. September 2021 -> 0**8**.**09**.20**21**
| `180921` | der 18. September 2021 -> **18**.**09**.20**21**
| `8091967` | der 8. September 1967 -> 0**8**.**09**.**1967**
| `18091967` | der 18. September 1967 -> **18**.**09**.**1967**
| `+` | morgen
| `++` | übermorgen
| `+++` | ...
| `-` | gestern
| `--` | vorgestern
| `---` | ...

Um einfach Tage, Wochen, Monate oder Jahre an ein bestimmtes Datum zu addieren oder zu subtrahieren, können folgende Kürzel und +/- Kombinationen verwendet werden.

| Kürzel | Bedeutung
|---|---
| `D` oder `d` | Tage 
| `M` oder `m` | Monate 
| `Y` oder `y` | Jahre 
| `W` oder `w` | Wochen (7 Tage)

**Beispiele**

| Eingabe | Wert
|---|---
| `0+2w` | heute + 14 Tage (2 Wochen)
| `1+1m-1d` | der letzte des aktuellen Monats (m = Monat, d = Tag)
| `1+1m-` | wenn man - und + ohne Ziffer am Ende hat, kann man es als Tage interpretieren. Also auch der letzte des Monats.
| `11+1y-` | Der letzte Tag des Jahres
| `11+2m-` | der letzte Tag im Februar im aktuellen Jahr


#### Zeitfelder

| Eingabe | Wert
|---|---
| `0` | jetzt -> 12:34 Uhr bei Eingabe um 12:34 Uhr lokale Zeit
| `00` | 00:00 Uhr
| `1` | die Stunde am Tag und 0 Minuten -> 0**1**:00 Uhr
| `12` | dies liefert die Stunde am Tag. Werte > 23 liefern ein ungültiges Datum. -> **12**:00 Uhr
| `123` | Die 1. Stelle liefert die Stunde; die Stellen 2 und 3 die Minuten. -> 0**1**:**23** Uhr
| `1234` | Die 1. und 2. Stelle liefern die Stunde; die Stellen 3 und 4 die Minuten. -> **12**:**34** Uhr
| `+` | jetzt plus eine Stunde
| `++` | jetzt plus 2 Stunden
| `+++` | ...
| `-` | jetzt minus eine Stunde (vor einer Stunde)
| `--` | jetzt minus 2 Stunden
| `---` | ...

Um einfach Minuten oder Stunden an eine bestimmte Uhrzeit zu addieren oder zu subtrahieren können folgende Kürzel und +/- Kombinationen verwendet werden.

| Kürzel | Bedeutung
|---|---
| `H` oder `h` | Stunde
| `M` oder `m` | Minute

**Beispiele**

| Eingabe | Wert
|---|---
| `0+3h` | jetzt + 3 Stunden
| `1+2h-3m` | 01:00 Uhr + 2 Stunden - 3 Minuten -> 02:57 Uhr

#### "Datum / Zeit" Felder

In einem "Datum / Zeit" Feld werden das Datum und die Zeit gleichzeitig eingegeben. Diese werden entweder durch ein Leerzeichen oder einen Stern getrennt. Im Gesamten gelten für "Datum / Zeit" Felder die selben Kriterien und Abkürzungen, wie für die Datums- und Zeitfelder im Einzelnen.

Sonderregelungen für die "Datum / Zeit" Felder sind:

- Wenn für das Datum kein Wert eingegeben wird, dann rechnet man mit dem Wert 0.
- Für die Zeit muss immer ein Wert angegeben werden, sonst wird ein Fehler geworfen.

| Eingabe | Wert
|---|---
| `*0` | heute und jetzt
| `0*` | !ErrorConverting

## Suchbereich

In die Spalten in der Suche können neben direkten Werten auch Platzhalter und Vergleichszeichen eingegeben werden. So ist es möglich, Zeiträume einzugrenzen oder mehrere Ergebnisse anzuzeigen, die mit dem selben Begriff/Buchstaben beginnen.

#### Zahlenfelder
Bei einem Zahlenfeld können folgende Operatoren zum Einsatz kommen: `>`, `<`, `=`, `>=`, `\<=`, `<>`, `null`, `!null`.

#### Datums-, Zeit-, DateTimeFelder
Bei einem Datums-, Zeit-, DateTime-Feld können folgende Operatoren zum Einsatz kommen: `>`, `<`, `=`, `>=`, `\<=`, `<>`, `null`, `!null`.

#### Textfelder
Bei einem Textfeld können folgende Operatoren zum Einsatz kommen: `%`, `_`, `=`, `<>`, `null`, `!null`, `~`, `!~`.

 * `%` der Wildcard-Operator steht für einen beliebigen Text
 * `_` steht für eine einzelnes beliebiges Zeichen

|Eingabe   |Interpretation   |Darstellung beim Verlassen
|---|------|-------------
|`%burg`   |`%` + burg   |`%burg`
|`%varo%`   |`%` + varo + `%`|`%varo%`
|`% burg`   |`%` + ' ' + burg   |`% burg`

In diesem Beispiel werden alle Einträge gefunden, die mit dem Text `burg` enden.
Zusätzlich werden alle Datensätze gesucht, die `varo` enthalten.

**'>' Größer**\
Es werden alle Datensätze gesucht, deren Wert größer als der angegebene ist.

**'<' Kleiner**\
Es werden alle Datensätze gesucht, deren Wert kleiner als der angegebene ist.

**'=' Gleich**\
Es werden alle Datensätze gesucht, deren Wert genau dem angegebenen entspricht.

**'>=' Größer-Gleich**\
Es werden alle Datensätze gesucht, deren Wert größer oder gleich dem angegebenen ist.

**'\<=' Kleiner-Gleich**\
Es werden alle Datensätze gesucht, deren Wert kleiner oder gleich dem angegebenen ist.

**'<>' Ungleich**\
Es werden alle Datensätze gesucht, deren Wert nicht gleich dem angegebenen ist.

**'null' Nichts (kein Wert)**\
Es werden alle Datensätze gesucht, bei denen in diesem Feld kein Wert eingetragen wurde

**'!null' nicht Nichts (einen Wert)**\
Es werden alle Datensätze gesucht, bei denen in diesem Feld ein Wert eingetragen wurde

**'~' Like Operator (Ählichkeitssuche)**\
Es werden alle Datensätze gesucht, bei denen der Wert des Feldes mit dem Muster übereinstimmt.
Das Muster kann die Wildcards `%` und `?` enthalten.

**'!~' Not Like Operator**\
Es werden alle Datensätze gesucht, bei denen der Wert des Feldes nicht mit dem Muster übereinstimmt.
Das Muster kann die Wildcards `%` und `?` enthalten.

### Verhalten der Felder

Wenn der Nutzer keinen Operator einträgt, wird in Datums-, Zeit-, DateTime- und Zahlenfeldern automatisch ein `=` eingefügt.
In Textfeldern ist der Defaultoperator `~`.
Ist in einem Textfeld zudem kein Wildcard-Operator vorhanden, wird automatisch `%` am Ende des Strings hinzugefügt.
Damit wird bei der Eingabe von `ba` der Name `bauer` gefunden.
Es wird also sichergestellt, dass immer ein Operator vorhanden ist.

Trägt der Nutzer `null` oder `!null` ein, werden alle weiteren Angaben verworfen.

Wenn ein Nutzer in ein Feld klickt, in das bereits etwas eingetragen wurde, erscheint dort wieder der ursprüngliche Inhalt.
Die Eingabe von `12` in ein Datumsfeld wird als `= 01.02.2021` dargestellt.
Wird dieses Feld wieder ausgewählt, erscheint dort wieder `12`.
