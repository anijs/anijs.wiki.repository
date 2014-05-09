Registering new Helpers
==========================

A helper is a static class that contains the functions that can be invoked through the **before** and **after** definition.

AniJS includes a helper by default with some useful functions, such as [[Remove animation after function]]. The implementation code looks like this:

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

You can add more functions to this helper by accessing it through the function **getHelper** and passing it no parameters. You may see a few examples of this in [[Writing before and after functions]].

In complex applications it may be necessary to register several helpers for more encapsulation.

```javascript
var validationAnimationHelper = {
	beforeFormValidation : function(e, contextAnimation){
		if( App.validate(App.Forms) ){
			contextAnimation.run();
		}
	}
}
AniJS.registerHelper('validationAnimationHelper', validationAnimationHelper);
```

Your customized helper always is executed every time you specify it in the definition. 

Example:

```xml
<button data-anijs="if: click, do: bounceIn, to: 'success-alert', before: beforeFormValidation, helper: validationAnimationHelper"><button/>
```
