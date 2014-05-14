Custom Events Listening
============================================
This feature it's available in [v0.3.0](https://github.com/anijs/anijs/tree/v0.3.0)

The documentation is not completely ready yet :(


AniJS permite ejecutar las animaciones a partir de eventos personalizados. Usted puede crear sus propios eventos y subscribir las animaciones a los mismos.

You can see a [Codepen Example](http://codepen.io/darielnoel/pen/KzsFn?editors=001) after read bellow.

#####Ventajas

- Cross-browser events.
- Integrate touch gestures.
- More Looseling Coupeling.

**EventProvider**

Un EventProvider, es un objeto cuyos eventos son escuchados por las animaciones gestionadas por AniJS. Si hay alguna animación cableada con alguno de estos, la misma será ejecutada.

Creemos que se pueden lograr cosas interesantes usando esta filosofia. Be creative and share your custom events providers with the comunity.

**Declaring EventProviders**

You can declare an event provider using **$** chart en el principio del valor de una definicion **on**.  
El tipo de evento se especifica en la definition **if**.

Example:
```xml
<header data-anijs="if: Double-tap, on: $GestureEventProvider, do: wobble animated">
<!-- ... -->
</header>
```

#####Obteniendo el EventProvider Object

After AniJS running, you can obtain the EventProvider a traves del metodo **getEventProvider**, el cual recive como parametro el ID del event provider, que es el mismo de la definicion.



Example: 

```javascript
MyApp.GestureEventProvider = AniJS.getEventProvider('GestureEventProvider');
```

#####Disparando eventos

Usted puede usar el metodo **dispatchEvent** para disparar cualquier evento que halla sido declarado previamente.

Example: 

```javascript
MyApp.GestureEventProvider.dispatchEvent('Double-tap');
```

#####Other usefull methods

- addEventListener
	
	Register an event handler of a specific event type on the EventTarget.

- removeEventListener
	
	Removes an event listener from the EventTarget.

- dispatchEvent
	
	Dispatch an event to this EventTarget.


The AniJS event system, usa the same names of the standar implementation. However you can use another event systems, like [[JQuery Events System]]. Or create el tuyo propio, read more about it in [[Creating Events Systems]].
