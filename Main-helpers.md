More helper functions
===================================

##Which other helpers you can use for modifying html elements?

* _[remove](#remove)_
* _[clone](#clone)_


##What they do and how use them?

###1. First, include ...

```xml
  <!--The core library-->
  <script src="anijs-min.js"></script>

  <!-- Main helpers library -->
  <script src="anijs-helper-dom-min.js"></script>
```

###2. Then inside the anijs sentence...

* ...You can add them into any of the clauses _'do:'_, _'after:'_ or _'before:'_

##### remove #####

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

##### clone #####

    _Duplicates html elements. This function can take one or more parameters separated by "|" as follows: param1 | param2 | paramN ..._

    <u>Examples:</u>

```xml
  <!-- Clones current HTML element and append it as child of the same element's parent. -->
     <div data-anijs="if: click, do: $clone"> </div>
    
  <!-- Clones the HTML element with id "clone" and append it as child of the same element's parent. -->
     <div data-anijs="if: click, do: $clone #clone"> </div>
    
  <!-- Clones current HTML element and append it as child of the element with id "otherParent". -->
     <div data-anijs="if: click, do: $clone, to: #otherParent"> </div>
     
  <!-- Clones the HTML element with the id "clone" and append it as child of the element with id "otherParent". -->
     <div data-anijs="if: click, do: $clone #clone, to: #otherParent"> </div>
```
