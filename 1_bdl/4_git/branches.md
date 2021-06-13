# Branches

Wenn wir an unserem code arbeiten wollen, ohne den haupt-code zu beeinträchtigen, können wir in branches arbeiten, und wenn wir es wünschen, unseren code mit dem haupt-code verschmelzen.

## Logik

![alt text](./branch.png "Ein typischer Branch")

unsere "common base", also die basis von all unserem code, ist das Master Branch. 

- Wir erstellen einen Branch, und arbeiten in diesem. 
- Wenn wir fertig sind wechseln wir in unseren master branch
- Wir "mergen" beide branches

> *Ein "TIP" ist der letzte commit eines branches*

## Git Befehle für branches

| Befehl                                      | Erklärung                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------|
| `$ git branch`                              | gibt eine liste mit allen branches innerhalb des repositories aus                        |
| `$ git branch [branchname]`                 | erstellt einen neuen branch                                                              |
| `$ git branch -d [branchname]`              | löscht einen branch                                                                      |
| `$ git checkout [branchname]`               | wechselt vom aktuellen branch in ein anderes branch                                      |
| `$ git checkout -b [branchname]`            | erstellt ein neues branch und wechselt sofort dort hinein                                |
| `$ git merge [branchname]`                  | verschmelzt einen branch mit dem branch, in dem wir uns aktuell befinden                 |
| `$ git branch -m [neuer branch name]`       | verändert den namen des branches, in dem wir uns gerade befinden                         |
| `$ git branch -m [alter name] [neuer name]` | verändert den namen eines branches in dem wir uns gerade nicht befinden                  |

## Referenzen

Hier gibt es ein paar weiterführende Informationen zu allen git befehlen: https://git-scm.com/doc