AnimationEnd and TransitionEnd normalization
============================================

Los eventos AnimationEnd and TransitionEnd are differentes en dependencia del browser.Por ejemplo:

| Agent   | AnimationEnd Event | TransitionEnd Event |  
| ----    | -----------------  | ------------------- |  
| W3C     | animationend       | animationend        |  
| Mozilla | mozAnimationEnd    | mozAnimationEnd     |  
| Webkit  | webkitAnimationEnd | webkitAnimationEnd  |  
| Opera   | oanimationend      | oanimationend		 |  

In AniJS animation event trigger definition use only **animationend**.

Ejemplo:
```xml
    <header data-anijs="when: animationend, where: footer, how: bounceIn">
    <!-- ... -->
    </header>
    <footer data-anijs="when: click, how: hinge">
     <!-- ... -->
    </footer>
```
