Add default class names while Anim
==================================

A veces puede ser necesario agregar nombres de clases determinados para saber que un objeto se esta animando. En el caso de la biblioteca [animate.css library](http://daneden.github.io/animate.css/) se usa el nombre de clase 'animated'.

```xml
<div class="bounce animated"></div>
```

Resultaria poco legible tener que agregar en los behaviors de las declaraciones estos nombres de clase. 

```xml
<div data-anijs="if: click, do: animated bounce"></div>
```

Por esta razon AniJS tiene un atributo cuyo nombre es **classNamesWhenAnim** y que puede ser cambiado mediante el metodo **setClassNamesWhenAnim**.

```javascript
	//Put #container as root travel scope
	AniJS.setClassNamesWhenAnim('animated');
```

De ahora en adelante cada vez que se valla a animar un objeto AniJS le pondrá tambien esta clase.
