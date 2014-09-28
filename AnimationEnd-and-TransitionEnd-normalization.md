AnimationEnd and TransitionEnd normalization
============================================

The AnimationEnd and TransitionEnd events varies depending on the browser.

| Agent   | AnimationEnd Event | TransitionEnd Event |  
| ----    | -----------------  | ------------------- |  
| W3C     | animationend       | transitionend        |  
| Mozilla | mozAnimationEnd    | mozTransitionEnd     |  
| Webkit  | webkitAnimationEnd | webkitTransitionEnd  |  
| Opera   | oanimationend      | otransitionEnd	 |  

AniJS is ruled by the W3C standard (**animationend** and **transitionend**).


Animationend Event example: 

```xml
<header data-anijs="if: animationend, on: footer, do: bounceIn">
<!-- ... -->
</header>
<footer data-anijs="if: click, do: hinge">
 <!-- ... -->
</footer>
```

Transtitionend Event example: 

```xml
<header data-anijs="if: transtitionend, on: footer, do: bounceIn">
<!-- ... -->
</header>
<footer data-anijs="if: click, do: hinge">
 <!-- ... -->
</footer>
```
