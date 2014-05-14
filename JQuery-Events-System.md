JQuery Events System
============================================
This feature it's available in [v0.3.0](https://github.com/anijs/anijs/tree/v0.3.0)

The documentation is not completely ready yet :(


The JQuery Events System is a concrete implementation of the [[Events System Interface | Creating Events Systems]].

**Use**

- Include Scripts

```xml

<body>
	<!-- Include JQuery -->
	<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/2.1.1/jquery.js"></script>

	<!-- Include AniJS -->
	<script src="anijs-min.js"></script>

	<!-- Include AniJS JQuery Events System-->
	<script src="event_systems/jquery/anijs-jquery-event-system-min.js"></script>
</body>

```

- Run AniJS again

```javascript

AniJS.run();

```

Despues de esto AniJS gestiona los eventos mediante la implementacion provista por JQuery. Usando los metodos:

- **trigger**

	Execute all handlers and behaviors attached to the matched elements for the given event type.

- **on**
	
	Attach an event handler function for one or more events to the selected elements.

- **off**

	Remove an event handler.

En sus [[EventProvider Object | Creating Events Systems]] usted podria hacer por ejemplo:

```javascript

//Using the JQuery Events System
MyApp.GestureEventProvider.trigger('Double-tap');

//Using the default AniJS Event System
//MyApp.GestureEventProvider.dispatchEvent('Double-tap');

```

Si usted esta usando JQuery en su aplicacion, emplear the JQuery Event System le brinda una mayor coherencia a su codigo, ademas de brindar una mejor cross-browser implementation.
