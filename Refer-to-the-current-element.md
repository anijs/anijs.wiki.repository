####How refer to the current element?

Using the word: ***target*** like the next example:

> "if click, on some li, do addClass hidden, to the clicked li"
```html
<ul data-anijs="if: click, on: li, do: $addClass hidden, to: target" >
  <li>Hidden me</li>
  <li>Hidden me</li>
</ul>
```





Inside anijs sentence, you can refer to the element that triggered the event (A kind of "this" in respect of the event...) by using the word: ***target***