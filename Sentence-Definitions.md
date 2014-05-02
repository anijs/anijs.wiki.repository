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

##### On
Elementos que pueden lanzar el evento que disparará la animación definido en el [when](#when). Si no se especifica se tomará el propio elemento que contiene la declaracion. Se define mediante un selector CSS.

Ejemplo especificando el elemento que dispara el evento:
```xml
	<!-- When click in footer animate header. -->
    <header data-anijs="when: click, where: footer, how: swing">
    <!-- ... -->
    </header>
    <footer>
     <!-- ... -->
    </footer>
```

Ejemplo sin especificar el elemento que dispara el evento:
```xml
	<!-- When click in header animate header. -->
    <header data-anijs="when: click, how: swing">
    <!-- ... -->
    </header>
    <footer>
     <!-- ... -->
    </footer>
```

##### Do
El tipo de animación que se ejecutara(esta dado por el nombre de la clase CSS que representa la animacion). Usted puede crear sus propias clases, usar la magnifica biblioteca de animaciones CSS [animate.css](http://daneden.github.io/animate.css/) u otras similares.

Ejemplo:
```xml
    <!-- When click in header animate footer with bounceIn animation. -->
    <header data-anijs="when: click, what: footer, how: bounceIn">
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
	<!-- When click in header animate footer. -->
    <header data-anijs="when: click, what: footer, how: swing">
    <!-- ... -->
    </header>
    <footer>
     <!-- ... -->
    </footer>
```

##### before
Nombre de la función que se ejecutará antes de iniciar la animación. Mediante esta se puede controlar si se ejecuta o no la animacion a traves del objeto [animationContext](#animationcontext). Ver [Implementando funciones after y before](#implementando-funciones-after-y-before).

Ejemplo:
```xml
	<!-- When click in header execute beforeAnimationFunction -->
    <header data-anijs="when: click, how: bounceIn, before: beforeAnimationFunctionName">
    <!-- ... -->
    </header>
```

##### after
Nombre de la funcion que se ejecutara despues de terminada la animacion. Ver [Implementando funciones after y before](#implementando-funciones-after-y-before).

Ejemplo:
```xml
	<!-- When click in header animate it with bounceIn animation and execute afterAnimationFunction -->
    <header data-anijs="when: click, how: bounceIn, after: afterAnimationFunctionName">
    <!-- ... -->
    </header>
```

##### helper
Nombre del ayudante que contiene las funciones after y before de la declaración. Si no se especifica se toma el helper por defecto cuyo nombre es 'default'. Y el cual contiene algunas funciones utiles como [removeAnim](remove-anim-function) la cual permite eliminar las clases asociadas a la animacion cuando esta termine.

Ejemplo:
```xml
	<!-- When click in header execute animate header with bounceIn animation and execute afterAnimationFunction -->
    <header data-anijs="when: click, how: bounceIn, after: afterAnimationFunctionName, helper: animationHelperInstanceName">
    <!-- ... -->
    </header>
```
