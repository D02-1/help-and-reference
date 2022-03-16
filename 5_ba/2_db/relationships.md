# Subdocuments 


Subdocuments sind Dokumente, die in andere Dokumente eingebettet sind. In Mongoose heißt es, das wir ein Schema in ein anderes einbetten können. Mongoose hat zwei verschiedene Möglichkeiten Subdokumente einzubetten: ein Array von Subdokumenten oder ein einzelnes Subdokument. 

Es würde keinen Unterschied machen, alles in ein Schema zu schreiben, der einzigste Grund warum eine Aufteilung ratsam ist, das es bei komplexen genesteten Objekten aufgeräumter aussieht.


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


# Relations



---

**mehr Lesematerial**

:point_right:[mongoose-subdocuments](https://zellwk.com/blog/mongoose-subdocuments/)\
:point_right:[mongoose docs subdocs](https://mongoosejs.com/docs/subdocs.html)\

