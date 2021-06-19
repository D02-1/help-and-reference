### Die .gitignore Datei

Dateien oder Ordner unseres Projektes, welche nicht versioniert (von Git getracked) werden sollen, schreiben wir in die `.gitignore` Datei. Diese Datei sollte im root unseres repositories liegen. Darin werden alle zu ignorierenden Dateien oder Ordner per Pfad relativ zum Git-Repo in einer eigenen Zeile genannt und Git wird diese Dateien fortan nicht weiter verfolgen

Grundsätzlich gehört alles hinein, was sich als Hürde für die gemeinsame Zusammenarbeit herausstellt oder aus anderen Gründen nicht geteilt werden sollte (Speicherplatz, Sicherheit). 

- beispielsweise findest du in der der `.gitignore` Datei:
    - persönliche IDE (Visual Studio Code) config files  
    - Dateien (env), welche z.b. Passwörter enthalten werden in der .gitignore aufgelistet
    - oder node modules (Packete von Dritten, welche wir in unserem Projekt nutzen und leicht von unserem Projektpartner selbst nach zu installieren sind)
    

Ordner und Dateien, welche einmal von Git versioniert wurden (z.b. versehentlich commited), müssen wir erst aus dem Trackingsystem entfernen, bevor wir sie mit dem nächsten commit in der .gitignore mit aufnehmen können.

`git ls-files` -zeigt Dateien/ Ordner der Staging area (index) an

```
git rm -r --cached <file>
git add .
git commit -m "removed file xyz"
git push
```