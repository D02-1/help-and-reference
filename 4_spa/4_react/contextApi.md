# Context API - wurde entwickelt, um das Konsumieren von Daten zu vereinfachen


## Wann verwendet man Context?

- Context dient dazu, Daten auszutauschen, die für einen Baum von React-Komponenten als „global“ angesehen werden können, wie z. B. der aktuell authentifizierte Benutzer, das theme oder die bevorzugte Sprache. 

- Context wird hauptsächlich verwendet, wenn auf einige Daten, von vielen Komponenten auf verschiedenen Verschachtelungsebenen zugegriffen werden muss. 

- Daten im Context, sollten Daten sein, welche nicht zu oft aktualisiert werden müssen, da Context nicht als Zustandsverwaltungssystem erstellt wurde.

- Nachteil von Context ist, das es die Wiederverwendung von Komponenten erschwert


<img src="prop-drilling-v-context.png" alt="context-vs-prop-drilling" width="70%">

typischen React-Anwendung (prop-drilling) vs Context API 

---

<img src="provider-context.png" alt="context" width="40%">

---

## Wie verwendet man Context?

**Es gibt vier Schritte zur Verwendung des React Context:**

```javascript
import React from 'react';

export const UserContext = React.createContext();

export default function App() {
  return (
    <UserContext.Provider value="german">
      <User />
    </UserContext.Provider>
  )
}

function User() {
  const value = React.useContext(UserContext);  
    
  return <h1>{value}</h1>;
}
```

---

1. :orange_circle: Context mit der createContext-Methode erstellen

```javascript
const UserContext = React.createContext();
```
2. :orange_circle: In unserer App-Komponente verwenden wir UserContext mit dem `UserContext.Provider`. Wir wickeln die Provider-Komponente um den Komponentenbaum (in diesem Fall User). Die eingebetteten Components können nun auf die Daten im Context zugreifen. 

3. :orange_circle: Im UserContext.Provider legen wir den Wert fest, den wir an unseren gesamten Komponentenbaum weitergeben möchten. 
`value="german"`

4. :orange_circle: In User, oder wo immer wir den zur Verfügung gestellten Context verwenden wollen, können wir das gesamte Context object an React.useContext() übergeben
```javascript
const value = React.useContext(UserContext);
```


---

**mehr Lesematerial**

:point_right:[how-use-react-context](https://devtrium.com/posts/how-use-react-context-pro)\
:point_right:[freecodecamp - react-context-for-beginners](https://www.freecodecamp.org/news/react-context-for-beginners/)



**Youtube Videos**

:point_right:[Web Dev Simplified-Learn useContext In 13 Minutes](https://www.youtube.com/watch?v=5LrDIWkK_Bc)



