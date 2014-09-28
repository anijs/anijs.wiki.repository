Helper functions for selecting
===================================

##Which helpers you can use auxiliary for selecting html elements?

* _[parent](#parent)_
* _[ancestors](#ancestors)_
* _[closest](#closest)_
* _[find](#find)_
* _[children](#children)_

##How use them?

###1. First, include ...

```xml
  <!--The core library-->
  <script src="anijs-min.js"></script>

  <!-- Main helpers library -->
  <script src="anijs-helper-dom-min.js"></script>
```

###2. Then inside the anijs sentence...

##### parent #####

_Returns element's parent, this function takes one parameter at most_

<u>Examples:</u>


```xml
  <!-- Removes the parent of the 'actual' div tag -->
    <div data-anijs="if: click, on: li, do: $remove, to: $parent"> </div>
    
  <!-- Removes the parent of the li tag that fired the click event -->
    <div data-anijs="if: click, on: li, do: $remove, to: $parent target"> </div>
    
  <!-- Removes all parents of the elements which have .primary class name -->
    <div data-anijs="if: click, on: li, do: $remove, to: $parent .primary"> </div>
```


##### ancestors #####

_Returns element's ancestors, this function takes at most two parameters_

<u>Examples:</u>


```xml
  <!-- Removes ancestors of the 'actual' div tag -->
    <div data-anijs="if: click, on: li, do: $remove, to: $ancestors"> </div>
    
  <!-- Removes ancestors of the 'actual' div tag. Specifically the ancestors with class name: .red-ancestors  -->
    <div data-anijs="if: click, on: li, do: $remove, to: $ancestors .red-ancestors"> </div>
    
  <!-- Removes ancestors of the li tag which dispatch the event. Specifically ancestors with class name: .red-ancestors -->
    <div data-anijs="if: click, on: li, do: $remove, to: $ancestors target | .red-ancestors"> </div>
    
  <!-- Removes ancestors of those having class names: red-ancestors and primary  -->
    <div data-anijs="if: click, on: li, do: $remove, to: $ancestors .primary | .red-ancestors"> </div>
```


##### closest #####

_Returns the closest ancestor of the omitted or specified element, optionally filtered by a selector, this function takes at most two parameters_

<u>Examples:</u>


```xml
  <!-- Removes the closest ancestor of the 'actual' div tag. -->
      <div data-anijs="if: click, on: li, do: $remove, to: $closest"> </div>
      
  <!-- Removes the ancestor more close to the li tag that fired the click event -->
      <div data-anijs="if: click, on: li, do: $remove, to: $closest target"> </div>
      
  <!-- Removes 'actual' div tag closest ancestor having the class name: .primary -->
      <div data-anijs="if: click, on: li, do: $remove, to: $closest .primary"> </div>
```

##### find #####

_Returns descendant elements, each element in the current set of matched elements optionally filtered by a selector, this function takes at most two parameters_

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

_Returns the childrens, optionally filtered by a selector, this function takes at most two parameters_

<u>Examples:</u>


```xml
  <!-- Removes all children of the 'actual' div tag. -->
      <div data-anijs="if: click, on: li, do: $remove, to: $children"> </div>
      
  <!-- Removes all childrens of the li tag that fired the click event. -->
      <div data-anijs="if: click, on: li, do: $remove, to: $children target"> </div>
      
  <!-- Removes childrens of the 'actual' div tag. Specifically those having the class name: primary -->
      <div data-anijs="if: click, on: li, do: $remove, to: $children .primary"> </div>
```

