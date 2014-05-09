Animation Context Object
============================================

Animation Context Object is the object that can control the execution arguments of an animation, and the animation execution itself asynchronously. 

This is very useful mainly in the functions [[before| Writing before and after functions]] and [[after | Writing before and after functions]], because, depending of certain conditions we can execute the animation or not and have the control of its arguments before and after being executed.

With AnimationContext we can accomplish amazing things, be creative and [tell us](https://github.com/anijs/anijs/issues) about it.

Example of a function before: 

```javascript

//beforeAnimSomething function implementation
defaultHelper.beforeAnimSomething: function(e, animationContext) {

	if(Balloon === 'red'){
		//Animation execute
		animationContext.run();
	}

	//The animation is not executed
}

```

Example of a function after: 

```javascript
//AniJS removeAnim implementation in default Helper
defaultHelper.removeAnim: function(e, animationContext) {
    //Clear the animation classes from the behavior
    animationContext.nodeHelper.removeClass(e.target, animationContext.behavior);
}
```

The attributes and methods from Animation Context Object are:

- **behaviorTargetList**  
List of elements to be animated.
	
- **nodeHelper**  
	DOM manipulation helper class. 

- **animationEndEvent**  
	Animation End Event Prefix correctly normalized according to the browser.

- **behavior**  
	Css class that can be added to the element.

- **after**  
	after Function that is executed after the animation finished.

- **run()**  
	Run the animation.

If you want to know more, please go to the [source code](https://github.com/anijs/anijs/blob/master/src/anijs.js)
