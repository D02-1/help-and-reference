# Relationships

Obwohl MongoDB keine relationale Datenbank wie SQL ist, können wir dennoch Relationships erstellen. Wir können Dokumente in andere einbetten oder von einem Dokument auf ein anderes referenzieren. (Referenzierte Beziehungen ähneln eher den Beziehungen, die in relationalen Datenbanken verwendet werden.)

---
## :orange_circle: Subdocuments (Dokumente einbetten)


Subdocuments sind Dokumente, die in andere Dokumente eingebettet sind. In Mongoose heißt es, das wir ein Schema in ein anderes einbetten können. Mongoose hat zwei verschiedene Möglichkeiten Subdokumente einzubetten: ein Array von Subdokumenten oder ein einzelnes Subdokument. 

Es würde hier keinen Unterschied machen, alles in ein Schema zu schreiben, der einzigste Grund warum eine Aufteilung ratsam ist, ist das es bei komplexen genesteten Objekten aufgeräumter aussieht.


```javascript
const childSchema = new Schema({
  name: String
});

const parentSchema = new Schema({
  // Single subdocument
  child: childSchema,

  // Array of subdocuments
  children: [ childSchema ]
});
```

Wenn wir `one-to-one` oder `one-to-few relationship`   (Eins-zu-wenige) haben, betten wir normalerweise die zugehörigen Dokumente in die Eltern Dokumente mit ein. Eingebettete Dokumente sind eine effiziente und saubere Möglichkeit, zusammengehörige Daten zu speichern, insbesondere Daten, auf die regelmäßig gemeinsam zugegriffen wird.
Zum Beispiel hat ein Tutorial einige Bilder (15 oder weniger). 

----

## :orange_circle: Referenzieren

Bei `one-to-aLot relationship` verwenden wir immer Referenzen. Denn wenn wir tatsächlich viele Dokumente in ein Dokument einbetten, könnten wir das Dokument schnell zu groß werden lassen. Dementsprechend lange würde das Interagieren mit der Datenbank dadurch dauern.
Zum Beispiel eine Kategorie hat 300 Tutorials.

```javascript
const CategorySchema = new Schema({
  name: String,
  tutorials:[{
    type:Schema.Types.ObjectId,
    // Die ref-Option teilt Mongoose mit, welches Modell während der Population verwendet werden soll
    ref:"Tutorials"
  }]
})
module.exports = mongoose.model("Kategorie", KategorieSchema)

const TutorialSchema = new Schema({
  name:String,
  duration: Number,
  createdAt: Date,
  category: {
    type: Schema.Types.ObjectId,
    ref:"Kategorie"
  }
})
// mit der populate-Methode können wir ein Array aller Tutorialobjekte abrufen und nicht nur ihre ObjectID. 
const getAllTutorials async (req, res)=>{
  const foundInKategorie = await KategorieModel.find({name: req.body}).populate("tutorials")
}
```

---

## :grey_question::question: Reference vs. Embedding Guideline Helper :question::grey_question:

**:point_right:Embedding:**

- Small subdocuments

- Data that does not change regularly

- Eventual consistency is acceptable

- Document that grow by a small amout

- Data that you will often need to perform a second query to fetch

- Fast reads

---

**:point_right:Referencing:**

- Large subdocuments

- Volatile data

- Immediate consistency is necessary

- Document that grow a large amount

- Data that you will often exclude from results

- Fast writes

---

**mehr Lesematerial**

:point_right:[mongoose-subdocuments](https://zellwk.com/blog/mongoose-subdocuments/)\
:point_right:[mongoose docs subdocs](https://mongoosejs.com/docs/subdocs.html)\
:point_right:[medium one-to-many-relationships-with-mongodb-and-mongoose-in-node-express ](https://medium.com/@brandon.lau86/one-to-many-relationships-with-mongodb-and-mongoose-in-node-express-d5c9d23d93c2)\
:point_right:[guideline for choosing refernce over subdocuments](https://www.bezkoder.com/mongoose-one-to-many-relationship/)




