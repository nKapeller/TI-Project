# TI-Project
Praktikum Sortierprojekt 

Fachbereich: Electronic Engineering
Themengebiet: Grundlagen der Informatik
PRAKTIKUM - SORTIERPROJEKT
Version 7, August 2024
Tobias Gawron-Deutsch
Grundlagen der Informatik
Autor: Tobias Gawron-Deutsch Seite: 2 / 10
Inhaltsverzeichnis
1 Aufgabe ................................................................................................................................... 3
1.1 Basisimplementierung ..................................................................................................... 3
1.2 Leistungsvergleich .......................................................................................................... 3
1.3 Vergleichbarkeit .............................................................................................................. 4
1.4 Strings.............................................................................................................................. 4
1.5 Verkette Listen ................................................................................................................ 4
1.6 StdLib .............................................................................................................................. 5
2 Beurteilung .............................................................................................................................. 6
2.1 Punkte .............................................................................................................................. 6
2.2 Beurteilung ...................................................................................................................... 6
2.3 Gruppenarbeit .................................................................................................................. 7
2.4 Abgabegespräch .............................................................................................................. 8
3 Angabe für Einzelpersonen ..................................................................................................... 9
3.1 Suchalgorithmus .............................................................................................................. 9
3.2 StdLib .............................................................................................................................. 9
Grundlagen der Informatik
Autor: Tobias Gawron-Deutsch Seite: 3 / 10
1 AUFGABE
1.1 BASISIMPLEMENTIERUNG
Schreiben Sie ein Programm in dem sie die folgenden vier Algorithmen, die ein Array
aufsteigend sortieren sollen, implementieren:
a) Quicksort
b) Bubblesort
c) Insertionsort
Das Array soll mit Zufallswerten initialisiert werden, wobei die Zahlen zwischen -32.768 und
32.767 liegen sollen. Die Initialisierung soll in einer eigenen Funktion gemacht werden.
Verwenden Sie dafür Pointer in einer geeigneten Art und Weise. Führen Sie die
Sortierfunktionen mit drei unterschiedlich großen Arrays aus (8, 16, und 64 Elemente).
Implementieren Sie eine Funktion, die überprüft ob das Ergebnis tatsächlich sortiert ist. Geben
Sie im Fehlerfall eine entsprechende Meldung aus.
Als Ergebnis sind die unsortierten und sortieren Arrays in der Konsole auszugeben. Stellen Sie
dabei sicher, dass in jeder Zeile nur maximal 15 Zahlen ausgedruckt werden um die Leserlichkeit
zu erhöhen.
1.2 LEISTUNGSVERGLEICH
Schreiben Sie ein Programm, mit dem die Sortieralgorithmen in ihrem Laufzeitverhalten
verglichen werden können. Führen Sie die Sortierfunktionen mit unterschiedlich großen Arrays
und unterschiedlichen Daten aus. Um die Performanz beurteilen zu können, soll die jeweilige
Laufzeit der Sortierung getrackt werden – für jede Größe der Arrays. Um eine Vergleichbarkeit
sicher zu stellen, sollen in einem Durchlauf alle Algorithmen mit den gleichen Ausgangsdaten
versorgt werden.
• Arraygrößen: 8, 32, 128, 512, 2048, 8192, 327681
• Datensätze:
o aufsteigend
o absteigend
o zufällig
1 Sie können auch gerne mit größeren Werten experimentieren – Die Abgabeversion soll aber nur diese Werte
benutzen UND größere Werte bitte nicht auf annuminas ausführen.
Grundlagen der Informatik
Autor: Tobias Gawron-Deutsch Seite: 4 / 10
Verwenden Sie dafür die clock() Funktion um die Laufzeit der jeweiligen Sortierung zu
speichern..
Geben Sie zusätzlich am Ende des Programms alle Laufzeiten von allen Sortierfunktionen für die
jeweilige Arraygröße aus. Geben Sie diese Informationen tabellarisch aus um auf den ersten
Blick eine Beurteilung hinsichtlich der Performanz treffen zu können. Wählen Sie dazu eine
geeignete Maßeinheit.
1.3 VERGLEICHBARKEIT
Schreiben Sie ein Programm, das zeigt, dass einmalige Codedurchläufe nur beschränkt für
Zeitvergleiche aussagekräftig2 sind. Führen Sie den Bubblesort mit dem gleichen zufälligen Set
an Daten mit einer Arraygröße von 2048 zwanzigmal aus und vergleichen Sie die Laufzeiten.
Geben Sie am Ende des Programms alle Laufzeiten sowie minimum, maximum und
durchschnittliche Laufzeiten aus.
1.4 STRINGS
Schreiben Sie einen Sortieralgorithmus der anstelle von Zahlen Strings als Arrayelemente
sortiert. Erweitern Sie dazu einen3 der von Ihnen implementierten Suchalgorithmen in einer
neuen Version so, dass jedes Element in dem Array einen String statt eines Integers speichert.
Lösen Sie das über eine struct. Der String soll 5 Zeichen lang sein und mit zufälligen
Buchstabenfolgen befüllt sein ([a-zA-Z]{5}). Erzeugen Sie ein Array mit 512 zufälligen Strings
und sortieren es.
Als Ergebnis sind die unsortierten und sortieren Arrays in der Konsole auszugeben. Stellen Sie
dabei sicher, dass in jeder Zeile nur maximal 15 Zahlen ausgedruckt werden um die Leserlichkeit
zu erhöhen. Geben Sie die Laufzeit der Sortierung in einer geeigneten Maßeinheit und
Darstellung aus (verwenden Sie die Funktion clock() für die Messung).
1.5 VERKETTE LISTEN
Schreiben Sie ein Programm, dass die Laufzeitunterschiede bei der Verwendung eines Arrays
und einer einfach verketten Liste zeigt. Implementieren sie eine zweite Version des Insertionsort
mit einer einfach verketten Liste anstelle eines Arrays und einer geeigneten Initialisierung. Der
2 Zumindest wenn der Zeitvergleich ohne weitere Maßnahmen auf einem Multitasking-Betriebssystem durchgeführt
wird.
3 Idealer Weise den Quicksort.
Grundlagen der Informatik
Autor: Tobias Gawron-Deutsch Seite: 5 / 10
Austausch der Position zweier Werte soll in diesem Fall durch Umverketten durchgeführt
werden (im Gegensatz zum Wertetausch zwischen Element bei einem Array).
Vergleichen Sie die beiden Implementierungen des Insertionsort-Algorithmus mit dem gleichen
zufälligen Datensatz und einer Arraygröße von 2048. Neben der reinen Sortierperformanz
vergleichen Sie auch die Laufzeiten der Initialisierung.
Als Ergebnis sind die unsortierten und sortieren Arrays in der Konsole auszugeben. Stellen Sie
dabei sicher, dass in jeder Zeile nur 15 Zahlen ausgedruckt werden um die Leserlichkeit zu
erhöhen. Geben Sie auch hier die jeweiligen Laufzeiten für die jeweilige Arraygröße aus. Geben
Sie diese Informationen tabellarisch aus um auf den ersten Blick eine Beurteilung hinsichtlich
der Performanz treffen zu können. Wählen Sie dazu eine geeignete Maßeinheit.
1.6 STDLIB
Die Stdlib stellt Sortierfunktionen zur Verfügung. Vergleichen Sie ihre Implementierung des
Quicksorts mit der Funktion aus der StdLib:
• void qsort(void *base, size_t nitems, size_t size, int (*compar)(const void *, const
void*))
Erzeugen Sie dazu ein Array mit 32768 zufälligen Werten als Ausgangsdaten. Sortieren Sie die
gleiche Ausgangsdaten einmal mit ihrer Implementierung und einmal mit der StdLib-
Implementierung. Messen Sie die Ausführungszeit mit der clock() Funktion.
Geben Sie die jeweiligen Laufzeiten aus. Wählen Sie dazu eine geeignete Maßeinheit und
Repräsentanz. Das Ziel ist es, auf den ersten Blick eine Beurteilung hinsichtlich der Performanz
treffen zu können.
Es soll möglich sein den Vergleich direkt mit den gleichen Ausgangsdaten zu wiederholen oder
den Vergleich zu beenden.
Grundlagen der Informatik
Autor: Tobias Gawron-Deutsch Seite: 6 / 10
2 BEURTEILUNG
2.1 PUNKTE
Aufgabe 2er Gruppe 3er Gruppe
1.1 – Basisimplementierung 25 25
1.2 – Leistungsvergleich - 6,25
1.3 – Vergleichbarkeit - 6,25
1.4 – String - 12,5
1.5 – Verkette Listen 12,5 12,5
1.6 – StdLib 12,5 12,5
Max. Gruppenpunkte 50 75
Einzelergebnis Gruppenpunkte/2 Gruppenpunkte/3
2.2 BEURTEILUNG
• Code
o Korrekt Implementierung aller Funktionalität wie oben beschrieben.
o Der Code muss dokumentiert sein.
o Verwenden Sie für die Implementierung die geeigneten Datenstrukturen.
o Der Speicher soll dynamisch alloziert werden und entsprechend wieder
freigegeben werden.
o Eine falsche Handhabung mit Pointern führt ebenfalls zu Punkteabzügen
o Warnungen bei einer Kompilierung mit -Wall und -Wextra führen zu
automatischen Punkteabzügen
o Zielplattform ist annuminas – dort muss der Code korrekt Kompilieren und
ausführbar sein4.
• Projektstruktur
o Sinnvolle Verzeichnisstruktur
o Sinnvolle Code-Wiederverwendung
o Einheitliche Dateitemplates
o Einheitliche Namenskonventionen
• Toolchain
o Es muss ein bash-script mit abgegeben werden, dass die benötigten
Executables erzeugt (alternativ ist natürlich auch ein makefile/cmakefile
möglich)
o Es muss eine Anleitung geben mit welchem Aufruf (Executable + ggf.
Parameter) welcher Aufgabe entspricht.
o Weiters sollen die beteiligten Studenten mit Namen, User und
Matrikelnummer in der Anleitung stehen.
• Abgabe
4 Es muss nicht auf annuminas entwickelt werden.
Grundlagen der Informatik
Autor: Tobias Gawron-Deutsch Seite: 7 / 10
o Es muss der vollständige C-Sourcecode (c & h-Dateien) abgegeben werden.
o Es muss git.technikum-wien.at für die Abgabe verwendet werden.
o Die Abgabe muss in dem git-Repository, dass der Gruppe zur Verfügung
gestellt wurde, erfolgen.
o Die Abgabe besteht aus dem Shellscript (bzw. makefile), der Anleitung und
den c-Sourcen (c- und header-Dateien). Keine Objectfiles, keine Executables,
keine temporären Dateien, etc.
o Es wird ausschließlich der Version, die im Branch „delivery“ liegt, beurteilt.
o Es wird die zuletzt hochgeladene Version beurteilt.
• Automatisches Nicht Genügend
o Falls das abgegebene Programm nicht kompiliert, führt das automatisch zu
einer Beurteilung mit Nicht Genügend
o Plagiate5,6 werden automatisch mit Nicht Genügend beurteilt7 (für die ganze
Gruppe).
o Unentschuldigte Nichtdurchführung des Abgabegesprächs bedeutet
automatisch ein Nicht Genügend (für die Person die unentschuldigt nicht
angetreten ist).
o Die Abgabe nicht rechtzeitig in git.technikum-wien.at im korrekten
Repository & Branch hochladen bedeutet automatisch ein Nicht Genügend.
o Nichtabgeben bedeutet automatisch ein Nicht Genügend für die ganze
Gruppe.
2.3 GRUPPENARBEIT
Das Projekt ist eine Gruppenarbeit für 3 Personen mit maximal zwei 2-Personengruppen aus
numerischen Gründen. Bei den 2-Personengruppen entfallen die drei Aufgaben „1.2
Leistungsvergleich“, „1.3 Vergleichbarkeit Listen“ und „1.4 String“. Die
Gruppenzusammenstellung ist vor Beginn des Praktikums bekannt zu geben – bitte in Moodle
das Datum nachschlagen. Nachträgliche Änderungen sind nach Absprache mit der LV-Leitung
möglich.
5 Da es in den meisten Fällen nicht nachträglich feststellbar ist, wer wen plagiiert hat sind alle Gruppen, die in den
Plagiatsfall verwickelt sind mit Nicht Genügend zu beurteilen.
6 Es werden die Abgaben aus allen BIC-TI Vorlesungen angeglichen.
7 Da zu unterschiedlichen Zeitpunkten abgegeben werden kann (die letzten beiden Termine und ggf. der
Nachprüfungstermin) kann es zu nachträglichen Feststellungen von Plagiaten und somit nachträglichen
Beurteilungskorrekturen kommen.
Grundlagen der Informatik
Autor: Tobias Gawron-Deutsch Seite: 8 / 10
2.4 ABGABEGESPRÄCH
In den letzten beiden Einheiten findet ein 5 bis 10 minütiges Abgabegespräch statt. Sie müssen
dabei in der Lage sein den abgegebenen Code erklären zu können und die Konzepte der
verwendeten Algorithmen beherrschen. Gruppen treten gemeinsam zu dem Abgabegespräch an8.
Die Abgabegespräche finden an in Moodle angegeben Terminen statt. Die Abgabe muss
entsprechend früher stattfinden (Termine ebenfalls in Moodle angegeben).
8 Es ist gewünscht, dass eine Gruppe gemeinsam Antritt. Sollte eine Gruppe nicht vollständig anwesend sein, so
wird mit den Anwesenden die Abgabe durchgeführt.
Grundlagen der Informatik
Autor: Tobias Gawron-Deutsch Seite: 9 / 10
3 ANGABE FÜR EINZELPERSONEN
Achtung: Es ist nur in vorher abgesprochenen Einzelfällen möglich das Praktikum als
Einzelarbeit zu absolvieren.
3.1 SUCHALGORITHMUS
15 Punkte
Schreiben Sie ein Programm welches ein Array von Integer in drei Arten sortiert:
• Mergesort
• Quicksort
• Bubblesort
Das Array soll mit Zufallswerten initialisiert werden, wobei die Zahlen zwischen -10.000 und
10.000 liegen sollen. Die Initialisierung soll in einer eigenen Funktion gemacht werden.
Verwenden Sie dafür Pointer in einer geeigneten Art und Weise. Führen Sie die
Sortierfunktionen mit drei unterschiedlich großen Arrays aus. Die Arraygrößen sollen sein 5000,
10.000 und 25.000 Elemente. Um die Performanz beurteilen zu können, soll die jeweilige
Laufzeit der Sortierung getrackt werden - für jede Größe der Arrays.
Verwenden Sie dafür die clock() Funktion um die Laufzeit der jewweiligen Sortierung zu
speichern..
Als Ergebnis sind die unsortierten und sortieren Arrays in der Konsole auszugaben. Stellen Sie
dabei sicher, dass in jeder Zeile nur 12 Zahlen angedruckt werden um die Leserlichkeit zu
erhöhen. Geben Sie zusätzlich am Ende des Programms alle Laufzeiten von allen
Sortierfunktionen für die jeweilige Arraygröße aus. Geben Sie diese Informationen tabellarisch
aus um auf den ersten Blick eine Beurteilung hinsichtlich der Performanz treffen zu können.
Wählen Sie dazu eine geeignete Maßeinheit.
3.2 STDLIB
10 Punkte
Die Stdlib stellt Sortierfunktionen zur Verfügung. Vergleichen Sie ihre Implementierung des
Quicksorts mit der Funktion aus der StdLib:
• void qsort(void *base, size_t nitems, size_t size, int (*compar)(const void *, const
void*))
Grundlagen der Informatik
Autor: Tobias Gawron-Deutsch Seite: 10 / 10
Erzeugen Sie dazu ein Array mit 15.000 zufälligen Werten als Ausgangsdaten. Sortieren Sie die
gleiche Ausgangsdaten einmal mit ihrer Implementierung und einmal mit der StdLib-
Implementierung. Messen Sie die Ausführungszeit mit der clock() Funktion.
Geben Sie die jeweiligen Laufzeiten aus. Wählen Sie dazu eine geeignete Maßeinheit und
Repräsentanz. Das Ziel ist es, auf den ersten Blick eine Beurteilung hinsichtlich der Performanz
treffen zu können.
