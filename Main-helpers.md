More helper functions
===================================

##Which other helpers you can use for modifying html elements?

* _[remove](#remove)_
* _[clone](#clone)_
* _[parent](#parent)_
* _[ancestors](#ancestors)_
* _[closest](#closest)_
* _[find](#find)_
* _[children](#children)_
* _[emit](#emit)_

##What they do and how use them?

###1. First, include ...

```xml
  <!--The core library-->
  <script src="anijs-min.js"></script>

  <!-- Main helpers library -->
  <script src="anijs-helper-dom-min.js"></script>
```

###2. Then inside the anijs sentence...

* You can define when these behaviors will be execute by adding the following functions to any of the clauses _'do:'_, _'after:'_ or _'before:'_

  - **remove<a name="remove"></a>**

  _Removes an element or elements from html page. This function can take one or more parameters separated by "|" as follows: param1 | param2 | paramN ..._

   <u>Examples:</u>

```xml
  <!-- Removes current element.-->
    <div data-anijs="if: click, do: $remove"> </div>
    
  <!-- Removes HTML elements having the class name .remove -->
    <div data-anijs="if: click, do: $remove .remove"> </div>
    
  <!-- Removes HTML element with remove id-->
    <div data-anijs="if: click, do: $remove #remove"> </div>
    
  <!-- Removes HTML elements with tag name p -->
    <div data-anijs="if: click, do: $remove p"> </div>
    
  <!-- Removes all HTML elements with the class name remove, or the remove id, or the tag name p -->
    <div data-anijs="if: click, do: $remove .remove | #remove | p"> </div>
```

  - **clone<a name="clone"></a>**

    _Duplicates html elements. This function can take one or more parameters separated by "|" as follows: param1 | param2 | paramN ..._

    <u>Examples:</u>

```xml
  <!-- Clones current HTML element and append it in the same parent. -->
     <div data-anijs="if: click, do: $clone"> </div>
    
  <!-- Clones the HTML element with id "clone" and append it in the same parent. -->
     <div data-anijs="if: click, do: $clone #clone"> </div>
    
  <!-- Clones current HTML element and append it as child of the element with id "otherParent". -->
     <div data-anijs="if: click, do: $clone, to: #otherParent"> </div>
     
  <!-- Clones the HTML element with the id "clone" and append it as child of the element with id "otherParent". -->
     <div data-anijs="if: click, do: $clone #clone, to: #otherParent"> </div>
```

* Selector fuctions

  - **parent<a name="parent"></a>**

    _Returns element's parent, this function takes one parameter at most_

    <u>Examples:</u>

```xml
  <!-- Removes the parent of the div tag which contains the present anijs sentence -->
    <div data-anijs="if: click, on: li, do: $remove, to: $parent"> </div>
    
  <!-- Removes the parent of the li tag that fired the click event -->
    <div data-anijs="if: click, on: li, do: $remove, to: $parent target"> </div>
    
  <!-- Removes all parents of the elements which have .primary class name -->
    <div data-anijs="if: click, on: li, do: $remove, to: $parent .primary"> </div>
```

  - **ancestors<a name="ancestors"></a>**

    _Returns element's ancestors, this function takes at most two parameters_

    <u>Examples:</u>

```xml
  <!-- Removes ancestors of the div tag which contains the present anijs sentence -->
    <div data-anijs="if: click, on: li, do: $remove, to: $ancestors"> </div>
    
  <!-- Removes ancestors of the div tag which contains the present anijs sentence. 
    Specifically ancestors with .red-ancestors class name  -->
    <div data-anijs="if: click, on: li, do: $remove, to: $ancestors .red-ancestors"> </div>
    
  <!-- Removes ancestors with css class .red-ancestors of li that dispatch the event -->
    <div data-anijs="if: click, on: li, do: $remove, to: $ancestors target | .red-ancestors"> </div>
  <!-- Removes ancestors with css class .red-ancestors of elements with css class primary -->
    <div data-anijs="if: click, on: li, do: $remove, to: $ancestors .primary | .red-ancestors"> </div>
```

  - **closest<a name="closest"></a>**

    _Returns the closest ancestor of the omitted or specified element, optionally filtered by a selector, this function takes at most two parameters_

    <u>Examples:</u>

```xml
  <!-- Removes ancestor more closets of div -->
      <div data-anijs="if: click, on: li, do: $remove, to: $closest"> </div>
  <!-- Removes ancestor more closets of li -->
      <div data-anijs="if: click, on: li, do: $remove, to: $closest target"> </div>
  <!-- Removes ancestor more closets of div with css class .primary -->
      <div data-anijs="if: click, on: li, do: $remove, to: $closest .primary"> </div>
```

  - **find<a name="find"></a>**

    _Returns descendants elements each element in the current set of matched elements, optionally filtered by a selector, this function takes at most two parameters_

    <u>Examples:</u>

```xml
  <!-- Removes all descendants elements of div -->
      <div data-anijs="if: click, on: li, do: $remove, to: $find"> </div>
  <!-- Removes all descendants elements of li -->
      <div data-anijs="if: click, on: li, do: $remove, to: $find target"> </div>
  <!-- Removes all descendants elements of div with css class is primary -->
      <div data-anijs="if: click, on: li, do: $remove, to: $find .primary"> </div>
```

  - **children<a name="children"></a>**

    _Function that return the children that matched elements, optionally filtered by a selector, this function takes at most two parameters_

    <u>Examples:</u>

```xml
  <!-- Removes all children of div -->
      <div data-anijs="if: click, on: li, do: $remove, to: $children"> </div>
  <!-- Removes all children of li -->
      <div data-anijs="if: click, on: li, do: $remove, to: $children target"> </div>
  <!-- Removes all children of div with css class is primary -->
      <div data-anijs="if: click, on: li, do: $remove, to: $children .primary"> </div>
```

  - **emit<a name="emit"></a>**

    _Fire custom event_

    <u>Examples:</u>

```xml
  <!-- Fire dummyEvent event of customEventNotifier -->
    <div data-anijs="if: click, do: fadeIn animated, to: #container, after: emit customEventNotifier.dummyEvent"> </div>
    <div data-anijs="if: dummyEvent, on: $customEventNotifier, do: $addClass hidden,  to: $children #container | div"> </div>
```
