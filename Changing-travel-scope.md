Changing travel scope
==========================

Por defecto AniJS toma como su ambito de recorrido el **body** del documento. Si queremos cambiarlo you call the **.setDOMRootTravelScope** and [[run AniJS again | Running-AniJS-repeatedly]].

```javascript
	//Put #container as root travel scope
	AniJS.setDOMRootTravelScope('#container');

	//Runnig AniJS again
	AniJS.run();
```
