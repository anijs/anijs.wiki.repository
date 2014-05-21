Remove animation after function
===============================

By default AniJS remove the classes that defines the animations after these ones are executed. If you want to hold it, you may use the function **holdAnimClass**.Read more about [[Hold animation after function]].

The description below is for the older versions of anijs. Using the removeAnim function is no longer necessary since [v0.4.0](https://github.com/anijs/anijs/releases/tag/v0.4.0). However previous versions are supported.

--------------------------------------------
Sometimes it's necessary to eliminate the classes that defines the animations after these ones are executed. For this matter AniJS provides a default helper with the function **removeAnim**. This function can be specified by the **after** definition. 

Example: 

```xml
    <!-- If click on header do swing animation to header after remove the swing animation from the element. -->
    <header data-anijs="if: click, do: swing, after: removeAnim">
    <!-- ... -->
    </header>
```

```javascript
var defaultHelper = {
    /**
     * Remove the animation class added when animation is created
     * @method removeAnim
     * @param {} e
     * @param {} animationContext
     * @return
     */
    removeAnim: function(e, animationContext) {
        animationContext.nodeHelper.removeClass(e.target, animationContext.behavior);
    }
}
```
