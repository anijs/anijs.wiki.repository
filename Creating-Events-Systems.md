Creating Events Systems
============================================


The Events System as a concept describes an event handling interface. Through this concept we can allow  AniJS to manage the events from other libraries, such as JQuery. Take a look to [[JQuery Events System]].

The Default Events System of AniJS, is implemented using the native browser API, and uses the sames names of the standar [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget).

You can create your own Events System overwriting the default AniJS Event System methods:

- isEventTarget

- createEventTarget

- addEventListenerHelper

- removeEventListenerHelper


#####isEventTarget

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

#####createEventTarget

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

#####addEventListenerHelper

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

#####removeEventListenerHelper

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

You can check the events system that have been implemented so far in [Implemented Events Systems](https://github.com/anijs/anijs/tree/master/src/events_system). If you create some Events System you may put it on [Implemented Events Systems](https://github.com/anijs/anijs/tree/master/src/events_system) and share it with the community.
