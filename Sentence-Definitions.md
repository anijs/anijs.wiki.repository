Sentence Definitions
==========================

For managging an animation correctly the following parameters must be stablished in some of the HTML elements.

##### If
Indicates the event trigger for the animation. You may check a detailed list of events [here](https://developer.mozilla.org/en-US/docs/Web/Reference/Events).

Some of the events are shown below as guide examples:

- click
- focus
- scroll
- DOMContentLoaded

Example:

```xml
<!-- If click on footer do swing animation to header. -->
<header data-anijs="if: click, on: footer, do: swing">
<!-- ... -->
</header>
<!-- If mouseover on header do bounce animation to footer. -->
<footer data-anijs="if: mouseover, on: header do: bounce">
 <!-- ... -->
</footer>
```

##### On
Stablish the trigger animation elements that waits for the event defined in the [if]. If [On] is not specified the element that holds the declaration owns it. To get the elements a CSS selector is defined. 

Specifying the trigger animation element example:

```xml
<!-- If click in footer animate header. -->
<header data-anijs="if: click, on: footer, do: swing">
<!-- ... -->
</header>
<footer>
 <!-- ... -->.
</footer>
```

Trigger animation element with out specification example:

```xml
<!-- If click on header animate footer. -->
<header data-anijs="if: click, do: swing, to: footer">
<!-- ... -->
</header>
<footer>
 <!-- ... -->
</footer>
```

```xml
<!-- If click on header animate header. -->
<header data-anijs="if: click, do: swing">
<!-- ... -->
</header>
<footer>
 <!-- ... -->
</footer>
```

##### Do
Animation type (behavior) that is going to be executed, it is given by the CSS class name that represents the animation. We strongly recomend you to use the amazing [animate.css library](http://daneden.github.io/animate.css/) as starting point, this library provides beautiful animations. Also, you can define your own animations.  

Example:
```xml
<!-- If click on header animate footer with bounceIn animation. -->
<header data-anijs="if: click, do: bounceIn, to: footer">
<!-- ... -->
</header>
<footer>
 <!-- ... -->
</footer>
```

##### To
Elements that will be animated.  If [To] is not specified the element that holds the declaration owns it. To get the elements a CSS selector is defined. 

Example:
```xml
<!-- If click on header do swing animation to footer.-->
<header data-anijs="if: click, do: swing, to: footer">
<!-- ... -->
</header>
<footer>
 <!-- ... -->
</footer>
```

##### before
Name of the function that will be executed before the animation starts. With this function the animation execution can be controlled throw the object [[Animation Context | Animation Context Object]]. Read [[Writing before and after functions]] for more information.

Example:
```xml
<!-- if click on header execute beforeAnimationFunction and do bounceIn animation-->
<header data-anijs="if: click, do: bounceIn, before: beforeAnimationFunctionName">
<!-- ... -->
</header>
```

##### after
Name of the function that will be executed after the animation ends. See [[Writing before and after functions]].

Example:
```xml
<!-- if click on header animate it with bounceIn animation and execute afterAnimationFunction -->
<header data-anijs="if: click, do: bounceIn, after: afterAnimationFunctionName">
<!-- ... -->
</header>
```

##### helper
Name of the helper that contains the after and before function declarations. If it is not specified the 'default' helper is used. The default helper  contains some useful functions, such as [[removeAnim | Remove animation after function]] which allows to eliminate the animation asociated classes when the animation ends.

Examples:
```xml
<!-- If click on header do bounceIn animation to header and execute afterAnimationFunction -->
<header data-anijs="if: click, do: bounceIn, after: afterAnimationFunctionName, helper: animationHelperInstanceName">
<!-- ... -->
</header>
```
