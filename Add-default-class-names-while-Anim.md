Add default class names while Anim
==================================

Sometimes it can be necesary to add class names to know if an object it's being animated. In case of [animate.css library](http://daneden.github.io/animate.css/) the class name used is **animated**.

```xml
    <div class="bounce animated"></div>
```

It would be bothersome add in the behaviors these class names.

```xml
    <div data-anijs="if: click, do: animated bounce"></div>
```

That's why AniJS has an attribute **classNamesWhenAnim** that can be change through the method **setClassNamesWhenAnim**.

```javascript
    //Put #container as root travel scope
    AniJS.setClassNamesWhenAnim('animated');
```

From now on, every time you need to animate an object with AniJS you will use this class too.
