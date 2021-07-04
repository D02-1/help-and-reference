# CSS positioning

### static - relative - absolute - fixed - sticky

Elemente können durch einer der positions Eigenschaften aus dem normalen Elementfluss entfernt werden und an jede beliebige Stelle des Viewports positioniert werden. 

* **`static`** (Standardwert) Das Element verbleibt im Textfluss. `top`, `bottom`, `left`, `right` werden ignoriert.

* **`relative`** Das Element kann mit `top`, `bottom`, `left`,`right` und `z-index` von seiner Orginalposition verschoben werden; es bleibt aber eine Lücke im Textfluss. Das Layout anderer Elemente wird nicht verändert.

<div>
<img src="posrelativ.png" alt="posrelativ" width="40%"> 
<img src="posrel2.png" alt="posrelativ2" width="20%"> 
<div>

* **`absolute`** Nimmt das Element komplett aus dem normalen Elementenfluss. Es existiert nicht mehr und andere Elemente rücken nach. Das Element kann mit `top`, `bottom`, `left`,`right` und `z-index` **zum nächsten nicht statischen Elternelement** positioniert werden. Sollten alle Elternelemente statisch sein, wird das Element `relative` zum viewport window positioniert. 

<img src="posabsolute.jpeg" alt="posabsolute" width="50%"> 

* **`fixed`** Ein Element mit position `fixed` kann relative zum viewport window positioniert werden. Es bleibt immer an dieser Position auch wenn die Seite hoch - bzw. runtergescrollt wird. `top`, `bottom`, `left`, `right` und `z-index` können verwendet werden.

<div>
<img src="posfixed2.jpg" alt="posfixed" width="53%"> 
<img src="posfixed.jpg" alt="posfixed" width="45%"> 
</div>

* **`sticky`**  wie fixed, aber es wird erst fest, wenn die Seite zu einem bestimmten, festgelegten Punkt gescrollt wird.

<img src="sticky.gif" alt="possticky" width="20%"> 


### Was ist der z-index?

wenn Elemente sich überlappen, hilft der z-index dabei zu bestimmen, in welcher Reihenfolge die Elemente angezeigt werden sollen.  Elemente mit einem größeren z-index liegen dabei näher am Betrachter und können Elemente mit kleinerem z-index überlagern.

<div>
<img src="z-index.png" alt="z-index" width="50%"> 
<img src="z-index2.png" alt="z-index2" width="40%"> 
</div>