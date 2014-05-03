AnimationEnd and TransitionEnd normalization
============================================

Los eventos AnimationEnd and TransitionEnd are differentes en dependencia del browser.Por ejemplo:

| Agent   | AnimationEnd Event | TransitionEnd Event |  
| ----    | -----------------  | ------------------- |  
| W3C     | animationend       | animationend        |  
| Mozilla | mozAnimationEnd    | mozAnimationEnd     |  
| Webkit  | webkitAnimationEnd | webkitAnimationEnd  |  
| Opera   | oanimationend      | oanimationend		 |  

AniJS se rige por el estandar de la W3C,**animationend** and **transitionend**.

In AniJS animation event trigger definition use only **animationend** or **transitionend**.

Ejemplo Animationend Event:
```xml
    <header data-anijs="if: animationend, on: footer, do: bounceIn">
    <!-- ... -->
    </header>
    <footer data-anijs="if: click, do: hinge">
     <!-- ... -->
    </footer>
```

Ejemplo Transtitionend Event:
```xml
    <header data-anijs="if: transtitionend, on: footer, do: bounceIn">
    <!-- ... -->
    </header>
    <footer data-anijs="if: click, do: hinge">
     <!-- ... -->
    </footer>
```
