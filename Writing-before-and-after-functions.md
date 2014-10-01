Writing before and after functions
==================================

The **before** and **after** definitions are useful when you want to execute actions before or after the action specified in **do** ends.  

These functions may be initialized by passing two params to them, although it is no mandatory and could be no parameters at all.

- **e** The [event object](https://developer.mozilla.org/en-US/docs/Web/API/Event) that triggers the action or animation.

- **animationContext** The [[Animation Context Instance | Animation Context Object]].

```javascript
var someBeforeOrAfterFunction = function(e, animationContext){
	
	//The event that triggers the animation
	console.log(e);

	//The Animation Context Instance
	console.log(animationContext);
}
```

In the case of the **before** function, you are able to execute or not the animation through the **animationContext** object.

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

The **Before** and **After** function's definition have to be registered in a helper. AniJS has default empty helper called Default. You can access to it calling the **getHelper** function with no parameters.

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

However, if it is your desire you can create your owns helpers. Read more [[Registering new Helpers]].
