# fetch - ist eine Methode des globalen window Objekts

**Die Fetch-API ermöglicht Webbrowsern, asynchrone HTTP-Anfragen an Webserver zu senden**


- `fetch()` gibt ein promise-Objekt zurück
- ohne Optionen machen wir eine einfache GET-Anfrage, die den Inhalt einer URL herunterlädt.

```javascript
const promise = fetch(url, [options])
//url – the URL to access.
//options – optional parameters: method, headers etc.
```
---
## Beispiel für options bei einem post request

```javascript
const options = {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json;charset=utf-8'
  },
  body: JSON.stringify(data)
}
```
---
Nachdem das promise aufgelöst wurde (Erfolg / Miserfolg) können wir mit den Methoden `then()` und `catch()` Callbacks für die Ergebnis-und für die Fehlerbehandlung definieren.

:exclamation::exclamation::exclamation:fetch löst das promise jedoch auch bei einer HTTP 4xx or 5xx (Fehler) response vom Server erfolgreich auf. fetch landet nur im catch, wenn die Anfrage gar nicht gestellt werden konnte, bspw. wenn das Netzwerk nicht verfügbar ist oder die Domain gar nicht existiert. Daher sollte bei fetch zusätzlich auch auf `response.ok` geprüft werden.


```javascript
fetch('https://jsonplaceholder.typicode.com/todos/4') 
 .then((response) => {
   if (response.ok) { 
    return response.json();
   }else {
       throw new Errow('response was not ok.')
   }
 })
 .then((data) => { 
   console.log(data); 
 })
 .catch((error) => {
   console.log('Something went wrong.', error); 
 });
```

Das Response-Objekt enthält nicht direkt den eigentlichen JSON response body, sondern ist eine Darstellung der gesamten HTTP-Antwort. Um den JSON body Inhalt aus dem Response-Objekt zu extrahieren, verwenden wir die `json()`-Methode, die ein zweites Promise zurückgibt, das mit dem Ergebnis des Parsens aufgelöst wird.

Das response Objekt stellt weitere Methoden bereit bspw. `response.blob()` für Bilder oder `response.text()` für eine reine txt Datei.

---

## Was ist SOP und CORS?

- SOP (Same-Origin-Policy) ist eine Sicherheitseigenschaft des Webbrowsers, welche verhindert, dass Webseiten (bzw. deren Scripte) auf Inhalte zugreifen können, die aus einer anderen Quelle (Origin) stammen.


- „CORS“ steht für Cross-Origin Resource Sharing. Es ermöglicht uns, Anfragen von einer Webseite an eine andere Webseite im Browser zu senden. 


<img src="cors1.jpg" alt="cors1" width="40%">
<img src="cors2.png" alt="cors2" width="40%">



**mehr Lesematerial**

:point_right:[javascript.info/fetch](https://javascript.info/fetch)\
:point_right:[developers.google - working-with-the-fetch-api](https://developers.google.com/web/ilt/pwa/working-with-the-fetch-api)\
:point_right:[do-you-know-why-we-check-for-response-ok-while-using-fetch](https://dev.to/myogeshchavan97/do-you-know-why-we-check-for-response-ok-while-using-fetch-1mkd)\
:point_right:[http-ein-blick-hinter-die-kulissen-des-internets](https://enginsight.com/de/blog/http-ein-blick-hinter-die-kulissen-des-internets/)\
:point_right:[mdn - HTTP response status codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)\


**Youtube Videos**

:point_right:[Web Dev Simplified-Learn Fetch API In 6 Minutes](https://www.youtube.com/watch?v=cuEtnrL9-H0)\
:point_right:[Web Dev Simplified-Learn CORS In 6 Minutes](https://www.youtube.com/watch?v=PNtFSVU-YTI)\



headers / preflight