
# Events

## addEventListener()

Mit einem Event Handler können wir genau steuern, was im Programm geschehen soll, wenn ein bestimmtes Ereignis eintritt.

- der erste Parameter ist das event auf welches gehört werden soll
- der zweite Parameter, ist die Funktion die immer dann ausgeführt wird, wenn das jeweilige Ereignis beim jeweiligen Element eintritt


```html
<a id ="my-link" href="www.google.com">google</a>
```

```javascript
const link = document.querySelector('#my-link')
link.addEventListener('click', handleClick) 

function handleClick(event){
  event.preventDefault()
  console.log(event.target);//=> <a id ="my-link" href="www.google.com">google</a>
  console.log(event.id);//=> my-link
  console.log(event.target.innerText)//=> google
}
```

In dieser Handler-Funktion ist es meistens nötig, auf die näheren Umstände des Ereignisses zu reagieren. Bspw. sind bei einem Mausklick die Koordinaten des Mauszeigers interessant oder bei einem Tastendruck die gedrückte Taste.

All diese Informationen sind im Event-Objekt gespeichert.(dieses wird standardmäßig als erster Parameter an die Handler-Funktion übergeben) Dieses Objekt repräsentiert das individuelle Ereignis, das der Handler gerade verarbeitet. Es bietet zahlreiche Eigenschaften mit Informationen zum Ereignis und einige Methoden, um das Verhalten des Ereignisses zu steuern.

## preventDefault()

Der Browser behandelt standardmäßig gewisse Ereignisse und führt die sogenannte Standardaktion (englisch default action) aus. Bspw.wenn wir, ein Formular submitten, wird die Seite neu geladen oder wenn wir auf einen Link klicken, werden wir vom Browser zur angegebenen URL weitergeleitet. Mit `preventDefault()`können wir solche Standartereignisse unterbinden.

## removeEventListener()

mit dieser Methode können wir Ereignishandler wieder entfernen
(nur möglich, wenn die angegebene Handler-Funktion extern ist)

```javascript
link.removeEventListener('click', handleClick) 
```


---
**mehr Lesematerial**

:point_right::fire:[javascripttutorial - javascript-mouse-events](https://www.javascripttutorial.net/javascript-dom/javascript-mouse-events/)\
:point_right:[MDN - Event](https://developer.mozilla.org/en-US/docs/Web/API/Event)\
:point_right:[W3schools - DOM Events](https://www.w3schools.com/jsref/dom_obj_event.asp)


**Youtube Videos**

:point_right:[Web Dev Simplified - Event Listeners](https://www.youtube.com/watch?v=XF1_MlZ5l6M&t=74s)




