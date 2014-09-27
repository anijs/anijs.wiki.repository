More helpers functions:
===================================

##How use the main helpers?

* _[remove](#remove)_
* _[clone](#clone)_
* _[parent](#parent)_
* _[ancestors](#ancestors)_
* _[closest](#closest)_
* _[find](#find)_
* _[children](#children)_
* _[emit](#emit)_

###1. First, include ...

```xml
  <!--The core library-->
  <script src="anijs-min.js"></script>

  <!-- Main helpers library -->
  <script src="anijs-helper-dom-min.js"></script>
```

###2. Then inside the anijs sentence...

* You can add the following functions to any of the clauses 'do:', 'after:' or 'before:' behavior:

  - remove<a name="remove"></a>

  _Removes element or elements from html. This function can take one or more parameters separated by "|" as follows: param1 | param2 | paramN ..._

   * Examples: *

```xml
  <!-- Remove current element.-->
    <div data-anijs="if: click, do: $remove"> </div>
  <!-- Remove HTML elements with class name .remove -->
    <div data-anijs="if: click, do: $remove .remove"> </div>
  <!-- Remove HTML element with id remove -->
    <div data-anijs="if: click, do: $remove #remove"> </div>
  <!-- Remove HTML elements with tag name p -->
    <div data-anijs="if: click, do: $remove p"> </div>
  <!-- Remove all HTML elements that contain class name remove or id remove o tag name p -->
    <div data-anijs="if: click, do: $remove .remove | #remove | p"> </div>
```

  - clone<a name="clone"></a>

    _Clones element or elements from html. This function can take one or more parameters separated by "|" as follows param1 | param2 | paramN ..._

    * Examples: *

```xml
  <!-- Clone current HTML element and append in same parent. -->
    <div data-anijs="if: click, do: $clone"> </div>
  <!-- Clone current HTML element and append other parent. -->
     <div data-anijs="if: click, do: $clone, to: #otherParent"> </div>
  <!-- Clone HTML element and append other parent. -->
     <div data-anijs="if: click, do: $clone #clone, to: #otherParent"> </div>
  <!-- Clone HTML element and append in same parent. -->
     <div data-anijs="if: click, do: $clone #clone"> </div>
```

* Selector fuctions

  - parent<a name="parent"></a>

    _Returns element's parent, this function takes one parameter at most_

    * Examples: *

```xml
  <!-- The div parent is removed -->
    <div data-anijs="if: click, on: li, do: $remove, to: $parent"> </div>
  <!-- The parent of li that fire event is removed -->
    <div data-anijs="if: click, on: li, do: $remove, to: $parent target"> </div>
  <!-- Remove all parents of elements that css class is .primary -->
    <div data-anijs="if: click, on: li, do: $remove, to: $parent .primary"> </div>
```

  - ancestors<a name="ancestors"></a>

    _Returns element's ancestors, this function takes at most two parameters_

    * Examples: *

```xml
  <!-- The div ancestors are removed -->
    <div data-anijs="if: click, on: li, do: $remove, to: $ancestors"> </div>
  <!-- Remove ancestors of div with css class .red-ancestors -->
    <div data-anijs="if: click, on: li, do: $remove, to: $ancestors .red-ancestors"> </div>
  <!-- Remove ancestors with css class .red-ancestors of li that dispatch the event -->
    <div data-anijs="if: click, on: li, do: $remove, to: $ancestors target | .red-ancestors"> </div>
  <!-- Remove ancestors with css class .red-ancestors of elements with css class primary -->
    <div data-anijs="if: click, on: li, do: $remove, to: $ancestors .primary | .red-ancestors"> </div>
```

  - closest<a name="closest"></a>

    _Returns the closest ancestor of the omitted or specified element, optionally filtered by a selector, this function takes at most two parameters_

    * Examples: *

```xml
  <!-- Remove ancestor more closets of div -->
      <div data-anijs="if: click, on: li, do: $remove, to: $closest"> </div>
  <!-- Remove ancestor more closets of li -->
      <div data-anijs="if: click, on: li, do: $remove, to: $closest target"> </div>
  <!-- Remove ancestor more closets of div with css class .primary -->
      <div data-anijs="if: click, on: li, do: $remove, to: $closest .primary"> </div>
```

  - find<a name="find"></a>

    _Returns descendants elements each element in the current set of matched elements, optionally filtered by a selector, this function takes at most two parameters_

    * Examples: *

```xml
  <!-- Remove all descendants elements of div -->
      <div data-anijs="if: click, on: li, do: $remove, to: $find"> </div>
  <!-- Remove all descendants elements of li -->
      <div data-anijs="if: click, on: li, do: $remove, to: $find target"> </div>
  <!-- Remove all descendants elements of div with css class is primary -->
      <div data-anijs="if: click, on: li, do: $remove, to: $find .primary"> </div>
```

  - children<a name="children"></a>

    _Function that return the children that matched elements, optionally filtered by a selector, this function takes at most two parameters_

    * Examples: *

```xml
  <!-- Remove all children of div -->
      <div data-anijs="if: click, on: li, do: $remove, to: $children"> </div>
  <!-- Remove all children of li -->
      <div data-anijs="if: click, on: li, do: $remove, to: $children target"> </div>
  <!-- Remove all children of div with css class is primary -->
      <div data-anijs="if: click, on: li, do: $remove, to: $children .primary"> </div>
```

  - emit<a name="emit"></a>

    _Fire custom event_

    * Examples: *

```xml
  <!-- Fire dummyEvent event of customEventNotifier -->
    <div data-anijs="if: click, do: fadeIn animated, to: #container, after: emit customEventNotifier.dummyEvent"> </div>
    <div data-anijs="if: dummyEvent, on: $customEventNotifier, do: $addClass hidden,  to: $children #container | div"> </div>
```
