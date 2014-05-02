Registering new Helpers
==========================

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

<button data-anijs="when: click, what: 'success-alert', how: bounceIn, before: beforeFormValidation, helper: validationAnimationHelper"<button/>
