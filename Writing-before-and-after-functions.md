Writing before and after functions
==================================

Las funciones **before** y **after** son utiles cuando se quieren ejecutar acciones antes o despues de ejecutada una animacion.

Estas reciben two params

- **e** The [event object](https://developer.mozilla.org/en-US/docs/Web/API/Event) that trigger the animation.

- **animationContext** The [[Animation Context Instance | Animation Context Object]].

```javascript
var someBeforeOrAfterFunction = function(e, animationContext){
	
	//The event that trigger the animation
	console.log(e);

	//The Animation Context Instance
	console.log(animationContext);
}
```

En el caso de la funcion before, usted tiene el poder de ejecutar o no, la animacion, mediante el objeto animationContext.

```javascript
	//Obtaining the default helper
	var animationHelper = AniJS.getHelper();

	//Defining afterAnimationFunction
	animationHelper.beforeAnimationFunctionName = function(e, animationContext){
		if( someVariable ){
			//Run the animation
			animationContext.run()
		}
	}
```

Despues de implementar las funciones after y before, estas deben ser registradas en un helper. Por defecto AniJS tiene un empty helper cuyo nombre es default. Se puede acceder al mismo llamando a la funcion **getHelper** sin ningun parametro.

```javascript
	//Obtaining the default helper
	var animationHelper = AniJS.getHelper();

	//Defining afterAnimationFunction
	animationHelper.afterAnimationFunctionName = function(e, animationContext){
		console.log('Running afterAnimationFunction');
		console.log('Event triggered');
		console.log(e);
	}
```

Si lo desea usted puede crear sus propios helpers. Leer mas [[Registering new Helpers]].
