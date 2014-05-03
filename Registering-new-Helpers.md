Registering new Helpers
==========================

Un helper es una clase estatica que contiene las funciones que pueden ser invocadas a traves de los parametros **before** y **after**.

Por defecto AniJS incluye un helper con la implementacion de algunas funciones utiles like [[Remove animation after function]]. The implementation code look like this:

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

Usted puede agregar funciones a este helper accediendo al mismo mediante la funcion **getHelper** sin ningun parametro. Usted puede ver algunos ejemplos de esto en[[Writing before and after functions]].

En aplicaciones complejas puede que sea necesario registrar varios helpers para tener un mayor encapsulamiento.

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

Your custom helper always se ejecutara cada vez que se ponga.

```xml
<button data-anijs="if: click, do: bounceIn, to: 'success-alert', before: beforeFormValidation, helper: validationAnimationHelper"<button/>
```
