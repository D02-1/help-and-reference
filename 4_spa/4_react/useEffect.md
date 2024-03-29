# useEffect - (side-effects)

Die Idee, den useEffect-Hook zu verwenden, besteht darin, Code auszuführen, der während des Lebenszyklus der Komponente anstelle von bestimmten Benutzerinteraktionen oder DOM-Ereignissen passiert.

Mit diesem Hook teilen wir React mit, dass unsere Komponente nach dem Rendern etwas tun muss. React merkt sich die Funktion, die wir übergeben haben (unseren „Effekt“) und ruft diese auf, nachdem die DOM-Updates durchgeführt wurden.

```jsx
useEffect(
    () => {
        // execute side effect
    },
    // optional dependency array
    [
        // 0 or more entries
    ] 
)
```

---

:orange_circle: **erstes Argument - callback function**

- `useEffect` nimmt eine callback function welche als side-effekt ausgeführt wird, nachdem die Komponente gerendert wurde
- wird dem `useEffect` kein zweites Argument übergeben, wird der Effekt nach jedem neu-rendern aufgerufen.
- jeder Effekt in einer Komponente wird nacheinander ausgeführt, basierend auf der Positionierung im Quellcode

```jsx
useEffect(() => {
  console.log('I will run on every render');
});
```
---
:orange_circle: **zweites Argument - optionales dependency array**

- macht die Ausführung von bestimmten Bedingungen abhängig
- der Effekt wird nur dann erneut ausgeführt, wenn sich die Werte innerhalb des Arrays über die erneuten Renderings hinweg geändert haben. Dadurch können wir optimieren, wie oft der Effekt ausgeführt wird.

```jsx
useEffect(() => {
  console.log('I will run when propXYZ or stateXYZ changes');
}, [propXYZ, stateXYZ]);
```
---
:orange_circle: **leeres Array als zweites Argument**

- der Effekt wird nur einmal nach dem ersten Rendern ausgeführt und für die folgenden Renderzyklen übersprungen
- ist ein sehr häufiges Muster, wenn wir am Anfang des Lebenszyklus einer Komponente etwas tun möchten, beispielsweise um Daten abzurufen, event-listener zu "attachen" ...

```jsx
useEffect(() => {
  console.log('I will run only on first render');
}, []);
```
---
## clean up

- manchmal ist es notwenig, Effekte beim Beenden des "Lebenszyklusses" einer Komponente wieder aufzuräumen, um kein unerwünschtes Verhalten zu produzieren. Bspw. beim asynchronen fetch, welcher eventuell noch gar nicht abgeschlossen ist, bevor der Lebenszyklus der Komponente beendet wird (user klickt weiter). Das fetch muss dann mit einem clean up beendet werden, da es sonst zu Fehlermeldungen kommt, beim Versuch den state upzudaten `setData(data)`.

```jsx
useEffect(() => {
  // This is the effect itself.
  return () => {
    // This is its cleanup.
  };
});
```
---

**klassenbasierte Lifecycle Methoden in Hooks übersetzt**

<img src="lifecycle-in-hooks.jpg" alt="lifecycle-in-hooks" width="70%">

:eight_spoked_asterisk: mount - aufgebaut\
:eight_spoked_asterisk: unmount - abgebaut

---


**mehr Lesematerial**

:point_right:[logrocket - useeffect-hook](https://blog.logrocket.com/guide-to-react-useeffect-hook/)\
:point_right:[React docs - Using the Effect Hook](https://reactjs.org/docs/hooks-effect.html)\
:point_right:[6-use-cases-of-the-useeffect-reactjs-hook](https://dev.to/colocodes/6-use-cases-of-the-useeffect-reactjs-hook-282o)\
:point_right:[dev.to - useeffect-cleanup-how-and-when-to-use-it](https://dev.to/otamnitram/react-useeffect-cleanup-how-and-when-to-use-it-2hbm)\
:point_right:[dmitripavlutin.com - useEffect-explanation](https://dmitripavlutin.com/react-useeffect-explanation/)\
:point_right:[dmitripavlutin.com - useEffect-infinite-loop](https://dmitripavlutin.com/react-useeffect-infinite-loop/)\
:point_right:[Visual Guide to useEffect - Cleanups](https://alexsidorenko.com/blog/useeffect-cleanups/)\
:point_right::fire:[Complete Guide to useEffect](https://overreacted.io/a-complete-guide-to-useeffect/)


**Practice React's useEffect hook with 4 Interactive Exercises**

:point_right:[useEffect interactive exercises](https://www.clientside.dev/blog/react-use-effect-practice-exercises)


**Youtube Videos**

:point_right:[Sonny Sangha - Learn the React useEffect Hook in 24 minutes (for beginners)](https://www.youtube.com/watch?v=UVhIMwHDS7k)

