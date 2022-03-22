# Validierung (validation) und Bereinigung (sanitation) 

Ohne eine Validierung kommt es unter Umständen zu Anwendungsfehlern oder falschen Ergebnissen bei der Datenverarbeitung. 
Deshalb stellt die Validierung der Daten eine Grundvoraussetzung für eine korrekte und sinnvolle Datenverarbeitung dar.

### :large_blue_circle: Was ist der Unterschied zwischen Validierung Bereinigung der Daten

Validierung stellt sicher, dass die Daten, mit denen wir arbeiten werden, sowohl vorhanden sind als auch unseren Erwartungen entsprechen. Die Bereinigung der Daten verhindert bspw. Code-Injection oder entfernt überflüssigen whitespace.

### :large_blue_circle: Warum ist die serverseitige Validierung wichtig?

Hauptsächlich müssen wir uns um die serverseitige Validierung kümmern, da Daten, die von anderen Clients kommen (single-page apps, regular web apps, mobile applications, usw.), nicht vertrauenswürdig sind. Ein böswilliger Benutzer (oder Virus) kann z.b. die Front-End-Validierung (z. B. JavaScript) deaktiviert haben, damit die App falsche Daten an den Server sendet. 

---

## :red_circle: Mongoose Validation (im Schema)

:pushpin:SchemaTypes haben einen eingebauten Validator. Bspw. 

- Typenvalidierung

- Alle Typen haben die `required` Validierung,

- Number hat `min` und `max` Validierung. 

- Strings haben `Enum`-, `Match`-, `Minlength`- und `Maxlength`-Validatoren.

:pushpin:Benutzerdefinierte Fehlermeldungen

- Wir können die Fehlermeldung für die einzelnen Validatoren in unserem Schema konfigurieren.

:pushpin:Benutzerdefinierte Validatoren

- Wenn die integrierten Validatoren nicht ausreichen, können wir benutzerdefinierte Validatoren definieren, die unseren Anforderungen entsprechen.

:pushpin::bangbang:Schema Validierung bei Update

Mongoose unterstützt auch die Validierung für die Operationen `update()`, `updateOne()`, `updateMany()` und `findOneAndUpdate()`. Update-Validatoren sind jedoch standardmäßig deaktiviert!!!! – Beim update müssen wir die Option `{ runValidators: true }` mit angeben.

---

## :red_circle: Express-Validator

Express-Validator verwendet die validator.js Bibliothek, um Express Routen zu validieren.
Das npm Paket beinhaltet:

:pushpin:Sanitization

:pushpin:Custom validators/sanitizers

:pushpin:Custom error messages

:pushpin:Wildcards

:pushpin:Schema validation

---

### :large_blue_circle: Vorteile Express-Validator

- durch komplexe Validierungsregeln, oder custom Validierung kann eine Validierung direkt in der mongoose model Datei unübersichtlich werden lassen, mit Express-Validator lässt sich alles schön sauber und übersichtlich trennen

- Ablauf der Codeausführung, Express-Validator ist eine Validierungs-Middleware. Wenn wir ein Formular über eine Post-request senden, können Sie die Validierungslogik ausführen und im Falle eines Fehlers Fehlermeldungen an den Client zurücksenden, ohne den Controller zu erreichen.
Ohne Verwendung von Validierungs-Middleware muß Express die gesamte Controller-Logik ausführen und mögliche Validierungsfehler werden erst beim Aufrufen der mongoose save oder update Methode im Controller erkannt.


---

**mehr Lesematerial**

:point_right:[docs express-validator](https://express-validator.github.io/docs/)\
:point_right:[overview aller Methoden von validator.js](https://www.npmjs.com/package/validator)\
:point_right:[validation with express-validator](https://flaviocopes.com/express-validate-input/)\
:point_right:[FCC comparison-between-joi-express-validator](https://www.freecodecamp.org/news/how-to-choose-which-validator-to-use-a-comparison-between-joi-express-validator-ac0b910c1a8c/)\
:point_right:[stackabuse express-validator](https://stackabuse.com/form-data-validation-in-nodejs-with-express-validator/)\
:point_right:[clean-approach-to-using-express-validator](https://dev.to/nedsoft/a-clean-approach-to-using-express-validator-8go)\
:point_right:[how-to-use-mongoose-custom-validators](https://kb.objectrocket.com/mongo-db/how-to-use-mongoose-custom-validators-923)\
:point_right:[mongoosejs docs validation](https://mongoosejs.com/docs/validation.html)





