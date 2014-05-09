Running AniJS repeatedly
==========================

AniJS by default goes through all of the nodes of the document and parse every node with the data-anijs tag. Although you can do directly this by calling  **run**. 

Be aware that all old events subscriptions will be eliminated .

```javascript
//Traveled the DOM scope parsing all nodes with data-anijs tag.
AniJS.run();
```
