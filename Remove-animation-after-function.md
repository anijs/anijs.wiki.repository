Remove animation after function
===============================

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
