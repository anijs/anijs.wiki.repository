Sentence and Definitions
==========================

We call "Definition" to each part of the AniJS sentece: 

- Basic definitions: [If](#If), [On](#On), [Do](#Do), [To](#To)
- And extended definitions: [Before](#Before), [After](#After), [Helper](#Helper), which allows to execute more than one action inside the same sentence.

Keep reading and discover the magic behind those Definitions!

##### If

You must use it to specify in response of which **event** should be the action to execute. You can find a detailed list of events [here](https://developer.mozilla.org/en-US/docs/Web/Reference/Events).

Some of the events are shown below as guide examples: click, focus, scroll, DOMContentLoaded...

**Examples:**

```xml
<!-- If click, removes current element.-->
<p data-anijs="if: click, do: $remove"> If you click here this sentence will be gone!</p>

<!-- If mouseover on header do bounce animation to footer. -->
<footer data-anijs="if: mouseover, on: header do: bounce">
 <!-- ... -->
</footer>
```

##### On

You may use it to specify the owner of the event. The anijs sentence will be used it only if the previous event occurs over the element specify here, with a CSS selector.

If **[On]** is not specified, the element that holds the declaration owns it.

**Examples**

- Specifying the event's owner:

```xml
<!-- If click in footer animate header. -->
<header data-anijs="if: click, on: footer, do: swing">
<!-- ... -->
</header>
<footer>
 <!-- ... -->.
</footer>
```

- Omitting the event's owner:

```xml
<!-- If click on header animate footer. -->
<header data-anijs="if: click, do: swing, to: footer">
<!-- ... -->
</header>
<footer>
 <!-- ... -->
</footer>
```

- Omitting the event's owner and something else:

```xml
<!-- If click on header animate header. -->
<header data-anijs="if: click, do: swing">
<!-- ... -->
</header>
```

##### Do

Here you write the action or animation you want happening once the event occurs. **Which actions and animations can be done?** ***It is limitless.*** From the simplest ones, by plying with CSS classes, removing or cloning html elements, or even more complex executing javascript code.

Just a couple of examples as warming up:

```xml
<!-- If click on header animate footer with bounceIn animation. -->
<header data-anijs="if: click, do: bounceIn, to: footer">
<!-- ... -->
</header>
<footer>
 <!-- ... -->
</footer>
```

```xml
<!-- Clones current HTML element and append it as child of the same element's parent. -->
<div data-anijs="if: click, do: $clone">Click and clone me please, clone me!</div>
```

##### To

It defines the elements affected by the response action or animation. For naming those element you can use a **CSS Selector**, [[a AniJS' Selector|Selecting-html-elements]], or the word [[target|Refer-to-the-current-element]].

If **[To]** is not specified the element that holds the declaration owns it.

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

##### Before
You may use it to specify the name of the function that will be executed before the action or animation (from **do** definition) starts. 

In animation cases, with this function the animation execution can be controlled throw the object [[Animation Context | Animation Context Object]]. Read [[Writing before and after functions]] for more information.

Example:
```xml
<!-- if click on header execute beforeAnimationFunction and do bounceIn animation-->
<header data-anijs="if: click, do: bounceIn, before: beforeAnimationFunctionName">
<!-- ... -->
</header>
```

##### After
You may use it to specify the name of the function that will be executed after the action or animation (from **do** definition) ends. See [[Writing before and after functions]].

Example:
```xml
<!-- if click on header animate it with bounceIn animation and execute afterAnimationFunction -->
<header data-anijs="if: click, do: bounceIn, after: afterAnimationFunctionName">
<!-- ... -->
</header>
```

##### Helper
Name of the helper that contains the after and before function declarations. If it is not specified the 'default' helper is used. The default helper  contains some useful functions, such as [[removeAnim | Remove animation after function]] which allows to eliminate the animation associated classes when the animation ends.

Examples:
```xml
<!-- If click on header do bounceIn animation to header and execute afterAnimationFunction -->
<header data-anijs="if: click, do: bounceIn, after: afterAnimationFunctionName, helper: animationHelperInstanceName">
<!-- ... -->
</header>
```
