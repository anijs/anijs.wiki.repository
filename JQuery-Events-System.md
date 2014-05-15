JQuery Events System
============================================


The JQuery Events System is a concrete implementation of the [[Events System Interface | Creating Events Systems]].


You can see a [Codepen Example](http://codepen.io/darielnoel/pen/nltiL?editors=001) you must read bellow first.

#####Use

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

After this AniJS manage the events through the JQuery Events System implementation using the methods:

- **trigger**

	Execute all handlers and behaviors attached to the matched elements for the given event type.

- **on**
	
	Attach an event handler function for one or more events to the selected elements.

- **off**

	Remove an event handler.


On its [[EventProvider Object | Custom Events Listening]] you may do for instance:

```javascript
//Using the JQuery Events System
MyApp.GestureEventProvider.trigger('Double-tap');

//Using the default AniJS Events System
//MyApp.GestureEventProvider.dispatchEvent('Double-tap');
```

If you are using JQuery on your application, using the JQuery´s Events System gives your code more coherence. Besides it provides a better cross-browser implementation.