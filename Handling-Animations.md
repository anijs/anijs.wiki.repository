Handling Animations
==========================

Las animaciones pueden ser manejadas a partir de declaraciones directamente en los elementos HTML de la página. O [mediante Javascript](https://github.com/anijs/anijs/wiki/Handling-Animations-Using-JavaScript).

Una declaracion esta compuesta por 1 o muchas sentencias separadas por (;) y cada setencia a su vez por 1 o muchas definiciones.

```
Declaration -> Sentence 1; ... ; Sentence n
Sentence    -> Definition, ... , Definition n
Definition  -> if | on | do | to | before | after | helper  
```

Multiple Sentences example.
```xml
<header data-anijs="if: click, do: wobble; if: scroll, on: window, do: swing">
<!-- ... -->
</header>
```

