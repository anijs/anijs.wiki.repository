Running AniJS repeatedly
==========================

AniJS por defecto recorre todos los nodos del documento, y parsea todos los nodos que contengan el tag data-anijs. No obstante usted puede volver a parsear estos invocando la funcion **run**. 

Tenga en cuenta que las subscripciones de eventos viejas seran eliminadas.

```javascript
	//Traveled the DOM scope parsing all nodes with data-anijs tag.
	AniJS.run();
```
