Custom Events Listening
============================================


AniJS allows to execute the animations using customized events as a trigger. You can create your own events and attach the animations to them.

You can see a [Codepen Example](http://codepen.io/darielnoel/pen/KzsFn?editors=001) you must read bellow first.

#####Advantages

- Cross-browser events.
- Integrate touch gestures.
- More Looseling Coupeling.

**EventProvider**

An EventProvider is an interface that allows AniJS to listen complex events. From now on you can run animations when a complex event is triggered. 

We strongly believe that interesting things can be achieved using this philosophy. Be creative!.


**Declaring EventProviders**

You can declare an EventProvider using **$** chart at the begining of the **on** definition.  

The event type must be specified on the **if** definition.

Example: 

```xml
<header data-anijs="if: Double-tap, on: $GestureEventProvider, do: wobble animated">
<!-- ... -->
</header>
```

#####Getting the EventProvider Object


After AniJS has ran, you can obtain an specific EventProvider through the **getEventProvider** method, that use the EventProvider ID as a parameter(the same that was stablished on the definition).


Example: 

```javascript
MyApp.GestureEventProvider = AniJS.getEventProvider('GestureEventProvider');
```

#####Triggering events


You can use the **dispatchEvent** method to trigger any previously specified event.

Example: 

```javascript
MyApp.GestureEventProvider.dispatchEvent('Double-tap');
```

#####Other useful methods

- addEventListener
	
	Register an event handler of a specific event type on the EventTarget.

- removeEventListener
	
	Removes an event listener from the EventTarget.

- dispatchEvent
	
	Dispatch an event to this EventTarget.


The AniJS event system uses the same names of the standar implementation. However you can use another event system, such as [[JQuery Events System]] or you can even create your own, read more about it in [[Creating Events Systems]].
