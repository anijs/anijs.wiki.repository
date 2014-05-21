Hold animation after function
===============================

Sometimes it's necessary to hold the classes that defines the animations after these ones are executed. For this matter AniJS provides a default helper with the function **holdAnimClass**. This function can be specified by the **after** definition. 

Example: 

```xml
    <!-- If click on header do swing animation to header after hold the swing animation from the element. -->
    <header data-anijs="if: click, do: swing, after: holdAnimClass">
    <!-- ... -->
    </header>
```
