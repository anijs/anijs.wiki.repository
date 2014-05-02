Handling animations.
==========================

Las animaciones pueden ser manejadas a partir de declaraciones directamente en los elementos HTML de la página. O [mediante Javascript](link a Manejando animaciones con javascript).

Una declaracion esta compuesta por 1 o muchas sentencias separadas por (;) y cada setencia a su vez por 1 o muchas definiciones.

```
	Declaration -> Setence 1; ... ; Sentence n
	Sentence -> Definition, ... , Definition n
	Definition-> When | Where | What | How | before | after | helper  
```

Multiple Sentences example.
```xml
    <header data-anijs="when: click, how: wobble; when: scroll, where: window, how: swing">
    <!-- ... -->
    </header>
```

