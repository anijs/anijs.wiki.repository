Sentence Definitions
==========================

Para manejar una animación se deben establecer los siguientes parámetros en algún HTML element.

##### If
Indica el evento que disparará la animación. Usted puede ver una lista detallada de eventos [aqui](https://developer.mozilla.org/en-US/docs/Web/Reference/Events).

Algunos ejemplos de eventos son:

- click
- focus
- scroll
- DOMContentLoaded

Ejemplo:
```xml
    <!-- If click in footer animate header. -->
    <header data-anijs="if: click, on: footer, do: swing">
    <!-- ... -->
    </header>
    <!-- If mouseover header animate footer. -->
    <footer data-anijs="if: mouseover, on: header do: bounce">
     <!-- ... -->
    </footer>
```

##### On
Elementos que pueden lanzar el evento que disparará la animación definido en el [if](#if). Si no se especifica se tomará el propio elemento que contiene la declaracion. Se define mediante un selector CSS.

Ejemplo especificando el elemento que dispara el evento:
```xml
	<!-- If click in footer animate header. -->
    <header data-anijs="if: click, on: footer, do: swing">
    <!-- ... -->
    </header>
    <footer>
     <!-- ... -->
    </footer>
```

Ejemplo sin especificar el elemento que dispara el evento:
```xml
	<!-- If click in header animate header. -->
    <header data-anijs="if: click, do: swing">
    <!-- ... -->
    </header>
    <footer>
     <!-- ... -->
    </footer>
```

##### Do
El tipo de animación que se ejecutara(esta dado por el nombre de la clase CSS que representa la animacion). We strongly recomend you  to use the amazing [animate.css library](http://daneden.github.io/animate.css/) as starting point, this library provides beautiful animations. Also, you can define your own animations.

Ejemplo:
```xml
    <!-- If click in header animate footer with bounceIn animation. -->
    <header data-anijs="if: click, do: bounceIn, to: footer">
    <!-- ... -->
    </header>
    <footer>
     <!-- ... -->
    </footer>
```

##### To
Elementos que se desean animar. Si no se especifica se tomará el propio elemento que contiene la declaracion.Se define mediante un selector CSS.

Ejemplo:
```xml
	<!-- If click in header animate footer. -->
    <header data-anijs="if: click, do: swing, to: footer">
    <!-- ... -->
    </header>
    <footer>
     <!-- ... -->
    </footer>
```

##### before
Nombre de la función que se ejecutará antes de iniciar la animación. Mediante esta se puede controlar si se ejecuta o no la animacion a traves del objeto [[Animation Context | Animation Context Object]]. Mas informcion read [[Writing before and after functions]].

Ejemplo:
```xml
	<!-- if click in header execute beforeAnimationFunction and do bounceIn animation-->
    <header data-anijs="if: click, do: bounceIn, before: beforeAnimationFunctionName">
    <!-- ... -->
    </header>
```

##### after
Nombre de la funcion que se ejecutara despues de terminada la animacion. Ver [[Writing before and after functions]].

Ejemplo:
```xml
	<!-- if click in header animate it with bounceIn animation and execute afterAnimationFunction -->
    <header data-anijs="if: click, do: bounceIn, after: afterAnimationFunctionName">
    <!-- ... -->
    </header>
```

##### helper
Nombre del ayudante que contiene las funciones after y before de la declaración. Si no se especifica se toma el helper por defecto cuyo nombre es 'default'. Y el cual contiene algunas funciones utiles como [[removeAnim | Remove animation after function]] la cual permite eliminar las clases asociadas a la animacion cuando esta termine.

Ejemplo:
```xml
	<!-- If click in header execute animate header with bounceIn animation and execute afterAnimationFunction -->
    <header data-anijs="if: click, how: do, after: afterAnimationFunctionName, helper: animationHelperInstanceName">
    <!-- ... -->
    </header>
```
