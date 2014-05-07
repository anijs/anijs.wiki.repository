Handling Animations
==========================

Animations can be managed directly from statements in the HTML page elements. Or using [JavaScript](https://github.com/anijs/anijs/wiki/Handling-Animations-Using-JavaScript).

A declaration is composed by one or many sentences, each sentence ends with (;) and is formed by one or many definitions.

```
Declaration -> Sentence 1; ... ; Sentence n
Sentence    -> Definition, ... , Definition n
Definition  -> if | on | do | to | before | after | helper  
```

Examples:
```xml
<header data-anijs="if: click, do: wobble; if: scroll, on: window, do: swing">
<!-- ... -->
</header>
```

```xml
<div class="demo-square demo1" data-anijs="if: click, do: flipInY, to: .container-box"></div>
```

```xml
<input id="name" type="text" data-anijs="if: focus, do: wobble, to: p">
```
