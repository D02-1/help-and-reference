# Git einrichten

Bevor wir Git nutzen können, müssen wir git sagen wer wir sind, das machen wir indem wir unsere Daten mit folgenden Befehlen in die globale Konfigurationsdatei von Git schreiben:

- `git config --global user.email [unsere email adresse]` - mit diesem Befehl fügen wir unsere Email-Adresse hinzu.
- `git config --global user.name "[unser name]"` - mit diesem Befehl fügen wir unseren Namen hinzu.

Wir dürfen bei der eingabe des Namen`s die sogenannten "Gänsefüßchen" nicht vergessen, da es sich hierbei um einen text-string handelt.

Wenn alles geklappt hat, müssten wir mit dem befehl `git config --list` unsere eingegebenen Daten sehen können.
