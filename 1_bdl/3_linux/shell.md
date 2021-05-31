# Wichtige Kommandozeilenbefehle

Eine allgemeine Liste mit Befehlen finden wir hier: https://cheatography.com/davechild/cheat-sheets/linux-command-line/

## Durch pfade bewegen

Durch Pfade können wir uns mit dem Befehl `cd` bewegen, indem wir verschiedene pfade an das Kommando anhängen. Mit `cd ..` zum Beispiel, bewegen wir uns einen Ordner zurück und mit `cd /test/` bewegen wir uns vom aktuellen verzeichnis in das unterverzeichnis "test".

Wir können auch mehrere ordner zusammenfügen, indem wir zum Beispiel `cd test/assets` eingeben, auf diese weise können wir von einem verzeichnis auch in dessen Schwesterverzeichnis wechseln, zum beispiel vom Ordner Desktop zu Downloads, mit `cd ../Downloads`.

## Ordnerinhalte anzeigen

Den Inhalt eines Ordners können wir uns mit dem befehl `ls` anzeigen lassen. Um auch versteckte Dateien anzeigen zu lassen, benutzen wir den Befehl `ls -a`.

wenn wir das argument `-l` anfügen, können wir auch ein paar mehr informationen, wie das bearbeitungsdatum einer datei sehen. Wir können die beiden Argumente auch aneinanderreihen (`-la`), oder die abkürzung `ll` nutzen.

## Ordner anlegen

mit `mkdir [Ordnername]` legen wir einen neuen Ordner an. Mit mehreren aufeianderfolgenden Ordernamen können wir auch mehrere Ordner auf einmal anlegen.

Wenn wir nicht im aktuellen verzeichnis, sondern in einem anderen, einen ordner anlegen wollen, können wir das mit einem pfad vor dem Ordnernamen machen, zum beispiel `mkdir ./../test`.

## Datei erstellen

Mit `touch [Dateiname]` können wir eine neue Datei erstellen. Auch hier können wir genau wie bei den Ordnern sowohl in anderen verzeichnissen anlegen und  mehrere Dateien auf einmal erstellen.

## Dateien und Ordner löschen

Dateien können wir löschen, indem wir `rm [Dateiname]` eingeben. Falls wir einen Ordner löschen wollen, müssen wir das "recursive" argument nutzen, also `rm -r [Orndername]`.
