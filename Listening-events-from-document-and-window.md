Listening events from document and window
=========================================

If you want to execute some action, for example, an animation, when any **document** event is triggered such as DOMContentLoaded you just need to put in the **on** definition the reserved word "document".

Example: 

```xml
<!-- If  DOMContentLoaded then animate header with bounceIn animation-->
<header data-anijs="if: DOMContentLoaded, on: document, do: bounceIn">
<!-- ... -->
</header>
```

If you want to execute some action, for example, an animation, when any **window** event is triggered, such as "scroll" you just need to put the **on** definition the reserved word "window". 

Example: 

```xml
<!-- If  scroll then animate header with bounceIn animation-->
<header data-anijs="if: scroll, on: window, do: bounceIn">
<!-- ... -->
</header>
```
#onRunFinished Event

Added since v0.5.0 version.

Note that the **load** or **DOMContentLoaded**, events are executed before AniJS run. If you want to execute an action or run an animation loaded immediately after the page you should use the default event **onRunFinished**.

Example: 

```xml
<!-- If  scroll then animate header with bounceIn animation-->
<header data-anijs="if: onRunFinished, on: $AniJSEventProvider, do: swing">
<!-- ... -->
</header>
```
