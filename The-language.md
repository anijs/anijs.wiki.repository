The AniJS Language
==========================

The basic anijs sentence its like this general form:

**If** -  some event(click, scroll, [etc](https://developer.mozilla.org/en-US/docs/Web/Events)), **On** any element (css selector), **Do** -  some behavior(animation, $addClass, [etc](#)), **To**  - (any element).

Example:

```xml
<div data-anijs="if: click, do: $toggleClass red, to: .box"></div>
```

###The formal language definition

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

> ***But*** we encourage you to take a closer look to it, clause by clause... maybe... you can find

> there more sparkling details...