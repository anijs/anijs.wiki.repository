Helpers functions
====================

### **How put or remove classes to the html elements?**

**1- First, include ...**

```html
<!--The core library-->
<script src="anijs-min.js"></script>

<!--The dom manipulation helper-->
<script src="anijs-helper-dom-min.js"></script>

```
**2- Then inside the anijs sentence...**

You can use the reserved words:

 * $addClass
 * $removeClass
 * $toggleClass

Like the next examples:

- Single Class
```html
<input data-anijs="if: click, on: .tab, do: $toggleClass active, to: .navbar">
```

Every time the user clicks on any htlm object with the "tab" class settled, the additional class "active" will be applied to the elements with the "navbar" class established. if the elements to modify, (in this case, the elements with the "navbar" class added) already has the "active" class settled, then the "active" class will be removed.


- Multiple Classes
```html
<div data-anijs="if: click, on: .tab, do: $addClass open primary-color, to: modal"></div>
```

- Check a real world example on [codepen](http://codepen.io/darielnoel/full/FvCbx/)
