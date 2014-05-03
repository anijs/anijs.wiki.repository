Animation Context Object
============================================

Animation Context Object fue creado con el objetivo de poder controlar los parametros de ejecucion de una animacion, y la ejecucion de la animacion misma de manera asincrona. 

Esto resulta de mucha utilidad en las funciones [[before| Writing before and after functions]] y [[after | Writing before and after functions]] sobre todo, ya que en depencia de determinadas condiciones podemos ejecutar la animacion o no, ademas de tener el control de los parametros de la misma antes y despues de ser ejecutada.

Using AnimationContext we can lograr amazing things, be creative and [tell us](https://github.com/anijs/anijs/issues) about it.

Ejemplo implementacion de una function before:
```javascript

//beforeAnimSomething function implementation
defaultHelper.beforeAnimSomething: function(e, animationContext) {

	if(Balloon === 'red'){
		//Se ejecuta la animation
		animationContext.run();
	}

	//La animacion no se ejecuta
}

```

Ejemplo implementacion de una function after:
```javascript
//AniJS removeAnim implementation en default Helper
defaultHelper.removeAnim: function(e, animationContext) {
    //Clear the animation classes que vienen en el behavior
    animationContext.nodeHelper.removeClass(e.target, animationContext.behavior);
}
```

Los atributos y metodos de Animation Context Object are:

- **behaviorTargetList**  
Lista de elementos que seran animados.
	
- **nodeHelper**  
	DOM manipulation helper class. 

- **animationEndEvent**  
	Animation End Event Prefix correctamente normalizado segun el browser.

- **behavior**  
	Clases css que se le agregaran al elemento.

- **after**  
	Function after que se ejecutara despues de terminada la animacion.

- **run()**  
	La animacion se ejecuta.

Si usted quiere saber mas acerca de esto, please go to the [source code](https://github.com/anijs/anijs/blob/master/src/anijs.js)
