Listening events from document and window
=========================================

If you can execute a animation when any **document** event was triggered, like DOMContentLoaded you just put the document in a **on** definition.

Ejemplo:
```xml
	<!-- If  DOMContentLoaded animate header with bounceIn animation-->
    <header data-anijs="if: DOMContentLoaded, on: document, do: bounceIn">
    <!-- ... -->
    </header>
```

If you can execute a animation when any **window** event was triggered, like scroll you just put the window in a **on** definition.

Ejemplo:
```xml
	<!-- If  DOMContentLoaded animate header with bounceIn animation-->
    <header data-anijs="if: scroll, on: window, do: bounceIn">
    <!-- ... -->
    </header>
```
