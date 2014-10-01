The AniJS Language
==========================

The basic anijs sentence its like this general form:

**If** <u> *some event(click, scroll, [etc](https://developer.mozilla.org/en-US/docs/Web/Events))* </u>, **On** <u> *any element (css selector)* </u>, **Do** <u> *some behavior(animation, $addClass, $remove, [etc](#))* </u>, **To**  <u> *(any element)* </u>.

Example:

```xml
<div data-anijs="if: click, do: $toggleClass red, to: .box">If you click me, </div>
```

Every time the user clicks on the element with this sentence written, the red color will be switched in the elements with the "box" class established.

###Formal language definition

```
data-anijs  -> Sentence 1; ... ; Sentence n
Sentence    -> Definition, ... , Definition n
Definition  -> if | on | do | to | before | after | helper
```

A **data-anijs** is composed by one or many **sentences**, each sentence ends with (;) and is formed by one or many **definitions**.

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

> ***But*** we encourage you to take a closer look to it, clause by clause... maybe... you can find around here more sparkling details...
