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
:orange_circle: **erstes Argument - callback function**

- `useEffect` nimmt eine callback function welche als side-effekt ausgeführt wird, nachdem die Komponente gerendert wurde\
- wird dem `useEffect` kein zweites Argument übergeben, wird der Effekt nach jedem neu-rendern aufgerufen.\
- jeder Effekt in einer Komponente wird nacheinander ausgeführt, basierend auf der Positionierung im Quellcode


:orange_circle: **zweites Argument - optionale dependency array**

- macht die Ausführung von bestimmten Bedingungen abhängig
- der Effekt wird nur dann erneut ausgeführt, wenn sich die Werte innerhalb des Arrays über die erneuten Renderings hinweg geändert haben. Dadurch können wir optimieren, wie oft der Effekt ausgeführt wird.


:orange_circle: **leeres Array als zweites Argument**

- der Effekt wird nur einmal nach dem ersten Rendern ausgeführt und für die folgenden Renderzyklen übersprungen\
- ist ein sehr häufiges Muster, wenn wir am Anfang des Lebenszyklus einer Komponente etwas tun möchten, beispielsweise um Daten abzurufen, event-listener zu "attachen" ...

---

## clean up

- manchmal ist es notwenig, Effekte beim Beenden des "Lebenszyklusses" einer Komponente wieder aufzuräumen, um kein unerwünschtes Verhalten zu produzieren. Bspw. beim asynchronen fetch, welcher eventuell noch gar nicht abgeschlossen ist, bevor der Lebenszyklus der Komponente beendet wird (user klickt weiter), Auch das fetch muss dann mit einem clean up beendet werden, da es sonst zu Fehlermeldungen kommt.

```jsx
useEffect(() => {
  // This is the effect itself.
  return () => {
    // This is its cleanup.
  };
});
```

---
**mehr Lesematerial**

:point_right:[logrocket - useeffect-hook](https://blog.logrocket.com/guide-to-react-useeffect-hook/)\
:point_right:[React docs - Using the Effect Hook](https://reactjs.org/docs/hooks-effect.html)\
:point_right:[dev.to - useeffect-cleanup-how-and-when-to-use-it](https://dev.to/otamnitram/react-useeffect-cleanup-how-and-when-to-use-it-2hbm)





**Youtube Videos**

:point_right:[Sonny Sangha - Learn the React useEffect Hook in 24 minutes (for beginners)](https://www.youtube.com/watch?v=UVhIMwHDS7k)

