Remove animation after function
===============================

En diversas ocasiones se hace necesario eliminar las clases que definen las animaciones luego de que son ejecutadas. Para esto AniJS provee un default Helper con la function **removeAnim**. La cual puede ser invocada a traves del parametro **after de una sentencia**.

Ejemplo:
```xml
    <!-- If click on header animate this and after remove the Anim Classes from element. -->
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
