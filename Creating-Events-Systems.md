Creating Events Systems
============================================
This feature it's available in [v0.3.0](https://github.com/anijs/anijs/tree/v0.3.0)

The documentation is not completely ready yet :(


The EventSystem es un concepto que describe una interfaz para manejo de eventos. Mediante este podemos permitir que AniJS maneje los eventos a traves de otras bilbiotecas like JQuery. Take a look to [[JQuery Events System]].

The Default Events System of AniJS, is implemented using the native browser API, an uses the sames names of the standar [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget).

You can create your propio event system overwriting the default AniJS Event System methods.

- isEventTarget

- createEventTarget

- addEventListenerHelper

- removeEventListenerHelper


- **isEventTarget**

```javascript

/**
 * Return true if the element it's an event target object
 * @method isEventTarget
 * @param {} element
 * @return true or false
 */
AniJS.EventSystem.isEventTarget: function(element) {

	//Default AniJS Events System
    return (element.addEventListener) ? 1 : 0;

    //JQuery Events System looks like this
    //return (element.trigger) ? 1 : 0;

}

```

- **createEventTarget**

```javascript

/**
 * Create new EventTarget element
 * @method createEventTarget
 * @return An EventTarget
 */
AniJS.EventSystem.createEventTarget: function() {

	//Default AniJS Events System
    return new CustomEventTarget();

    //JQuery Events System looks like this
    //return $({});

}

```

- **addEventListenerHelper**

```javascript

/**
 * Put a listener in the object
 * @method addEventListenerHelper
 * @param {} eventTargetItem
 * @param {} event
 * @param {} listener
 * @param {} other
 * @return
 */
AniJS.EventSystem.addEventListenerHelper: function(eventTargetItem, event, listener, other) {

	//Default AniJS Events System
    eventTargetItem.addEventListener(event, listener, false);

    //JQuery Events System looks like this
    //$(eventTargetItem).on(event, listener);

}

```

- **removeEventListenerHelper**

```javascript

/**
 * Put a listener of the object
 * @method removeEventListenerHelper
 * @param {} e
 * @param {} arguments
 * @return
 */
AniJS.EventSystem.removeEventListenerHelper: function(element, type, listener) {

	//Default AniJS Events System
    element.removeEventListener(type, listener);

	//JQuery Events System looks like this
	$(element).off(type, listener);
}

```
You can ckeck los events system que han sido implementados hasta ahora en [Sistemas de Eventos Implementados](https://github.com/anijs/anijs/tree/master/src/events_system). Si usted crea su propio EventSystem, usted puede ponerlo ahi y asi compartirlo con la comunidad.
