# Flexbox (flex-container)

Mit Flexbox können wir unkompliziert variable und responsive Layouts erzeugen. Das Modell arbeitet mit zwei Achsen (horizontale und vertikale) auf denen Inhalte verteilt werden können. Im engl. Hauptachse (main axis) und Querachse (cross axis). Tatsächlich ist es einfacher, wenn wir uns an der "Hauptachse" orientieren. Da wir an dieser immer ausrichten. Bei `direction:row` ist x - die Hauptachse, bei `direction:column` wird y - zur Hauptachse.

<div>
<img src="flexbox.png" alt="flexbox" width="45%"> 
<img src="main-axis.png" alt="main-axis" width="45%">
</div>

### **Elternteil ist unser flex-container, in welchem wir mit folgenden properies bestimmen können, wie sich dessen Kinder (boxen / flex-items) verhalten sollen**

```css
.flex-container{
    display:flex;
    flex-direction: row (default) |row-reverse | column | column-reverse;
    justify-content:flex-start (default) | flex-end | center | space-between | space-around | space-evenly | start | end;
    align-items:stretch (default) | flex-start | flex-end | center | baseline;
    flex-wrap: nowrap | wrap | wrap-reverse
}
```
---
### **flex-direction**
<img src="flex-direction.jpg" alt="flex-direction" width="60%"> 

---

### **Ausrichtung auf den x/y Achsen**
**`bei flex-direction:row mit:`**


<div>

```css
justify-content:(richtet die Kinder auf der x-Achse (main axis) aus => Bild 1)
```
```css
align-items:(richtet die Kinder auf der y-Achse aus => Bild 2)
```
</div>


<div>

<img src="justify-content.png" alt="justify-content" width="28%"> 
<span> <-- x (main axis)</span>


<img src="align-items.png" alt="align-items" width="35%"> 
<span> <-- y</span>

</div>



---
**:exclamation::exclamation::exclamation: ACHTUNG bei `flex-direction:column` drehen sich die Befehle für die Ausrichtung mit. Es übernimmt:**\
 `justify-content` die y-Achse (nun die main-axis) und
  `align-items` die x-Achse.


:point_right:[alignment main-axis abhängig von der flex-direction](https://www.smashingmagazine.com/2018/08/flexbox-alignment/)

---
### **flex-wrap**

<img src="flex-wrap.png" alt="flex-wrap" width="35%"> 

Der `default` Wert ist `no-wrap`, das heißt, das alle Kinder des flex-containers bei `direction:row` z.b. in eine Reihe gequetscht werden und dabei unter Umständen ihre Orginalbreite verlieren können, um das zu verhinden, können wir dem Elternelement sagen 
```css 
 flex-wrap:wrap
 ```

---       

 **mehr Lesematerial**

:point_right:[selfhtml flexbox deutsch](https://wiki.selfhtml.org/wiki/CSS/Tutorials/Flexbox)\
:point_right:[flexbox help](https://flexbox.help/)\
:point_right:[flexbox-aligning with auto margins](https://dev.to/samanthaming/flexbox-aligning-with-auto-margins-4gfh)\
:point_right:[flexbox tutorial](https://marina-ferreira.github.io/tutorials/css/flexbox/)\
:point_right:[flexbox tutorial css-tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)\
:point_right:[flexbox cheatsheet](https://yoksel.github.io/flex-cheatsheet/#section-align-content)\
:point_right:[interaktiver flexbox playground](https://codepen.io/enxaneta/full/adLPwv)\
:point_right:[freecodecamp flexbox mit animierten gifs](https://www.freecodecamp.org/news/an-animated-guide-to-flexbox-d280cf6afc35/)
    
    



 **CSS Game**

:point_right:[css flexbox game froggy](https://flexboxfroggy.com/)
