Helper functions for selecting
===================================

##Which helpers you can use for selecting html elements?

* _[parent](#parent)_
* _[ancestors](#ancestors)_
* _[closest](#closest)_
* _[find](#find)_
* _[children](#children)_

##How use them?

_You can use them as part of the AniJS sentence, inside the "**to:** " definition. They can receive as parameter a CSS Selector or the word [[target | Refer-to-the-current-element]]. Here you can find several examples for each case._

###1. First, include ...

```xml
  <!--The core library-->
  <script src="anijs-min.js"></script>

  <!-- Helpers library -->
  <script src="anijs-helper-dom-min.js"></script>
```

###2. Then inside the anijs sentence...

##### parent #####

_Returns an element's parent. This function takes one parameter at most. As parameter you can use a CSS Selector or the word [[target | Refer-to-the-current-element]]._

<u>Examples:</u>


```xml
  <!-- Removes the parent of the 'actual' div tag 
       when the user clicks on the element with id: eraseButton -->
    <div data-anijs="if: click, on: #eraseButton, do: $remove, to: $parent"> </div>
    
  <!-- Animate the parent of the li tag that fired the click event -->
    <div data-anijs="if: click, on: li, do: flash animated, to: $parent target"> </div>
    
  <!-- Clones the parent of all elements which have .primary class name -->
    <div data-anijs="if: click, on: .tab, do: $clone, to: $parent .primary"> </div>
```


##### ancestors #####

_Returns element's ancestors of the omitted or specified element, optionally filtered by a selector. This function takes at most two parameters._

<u>Examples:</u>


```xml
  <!-- Running swing animation over the ancestors of the 'actual' div tag 
        when the user clicks on any li tag -->
    <div data-anijs="if: click, on: li, do: swing animated, to: $ancestors"> </div>
    
  <!-- Adding css class .big to all ancestors of the elements with class name: .red-ancestors  -->
    <div data-anijs="if: click, on: #wave, do: $addClass .big, to: $ancestors .red-ancestors"> </div>
    
  <!-- Removes ancestors of the li tag which dispatch the event. 
        Specifically ancestors with class name: .red-ancestors -->
    <div data-anijs="if: click, on: li, do: $remove, to: $ancestors target | .red-ancestors"> </div>
    
  <!-- Removes ancestors of those having class names: red-ancestors and primary  -->
    <div data-anijs="if: click, on: li, do: $remove, to: $ancestors .primary | .red-ancestors"> </div>
```


##### closest #####

_Returns the closest ancestor of the omitted or specified element, optionally filtered by a selector, this function takes at most two parameters_

<u>Examples:</u>


```xml
  <!-- Clones the 'actual' div tag and moves the cloned element 
        as child of the closest ancestor from the 'actual' div tag -->
      <div data-anijs="if: click, on: li, do: $clone, to: $closest"> </div>
      
  <!-- Removes the ancestor more close to the li tag that fired the click event -->
      <div data-anijs="if: click, on: li, do: $remove, to: $closest target"> </div>
      
  <!-- Removes 'actual' div tag closest ancestor having the class name: .primary -->
      <div data-anijs="if: click, on: li, do: $remove, to: $closest .primary"> </div>
```

##### find #####

_Returns descendant elements, of the omitted or specified element, optionally filtered by a selector, this function takes at most two parameters_

<u>Examples:</u>

```xml
  <!-- Removes all descendants elements of the 'actual' div tag. -->
      <div data-anijs="if: click, on: li, do: $remove, to: $find"> </div>
      
  <!-- Removes all descendants elements of the li tag that fired de click event. -->
      <div data-anijs="if: click, on: li, do: $remove, to: $find target"> </div>
      
  <!-- Removes descendants elements of div tag. Specifically those having class name primary -->
      <div data-anijs="if: click, on: li, do: $remove, to: $find .primary"> </div>
```

##### children #####

_Returns the childrens, of the omitted or specified element, optionally filtered by a selector, this function takes at most two parameters_

<u>Examples:</u>


```xml
  <!-- Removes all children of the 'actual' div tag. -->
      <div data-anijs="if: click, on: li, do: $remove, to: $children"> </div>
      
  <!-- Removes all childrens of the li tag that fired the click event. -->
      <div data-anijs="if: click, on: li, do: $remove, to: $children target"> </div>
      
  <!-- Removes childrens of the 'actual' div tag. Specifically those having the class name: primary -->
      <div data-anijs="if: click, on: li, do: $remove, to: $children .primary"> </div>
```

