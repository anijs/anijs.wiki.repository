Writing before and after functions
==================================

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