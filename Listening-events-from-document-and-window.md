Listening events from document and window
=========================================

If you can execute a animation when any **document** event was triggered, you just put the document in a where definition.

Ejemplo:
```xml
	<!-- When  DOMContentLoaded animate header with bounceIn animation-->
    <header data-anijs="when: DOMContentLoaded, where: document, how: bounceIn">
    <!-- ... -->
    </header>
```

If you can execute a animation when any **window** event was triggered, you just put the document in a where definition.

Ejemplo:
```xml
	<!-- When  DOMContentLoaded animate header with bounceIn animation-->
    <header data-anijs="when: scroll, where: window, how: bounceIn">
    <!-- ... -->
    </header>
```
