Changing travel scope
==========================

By default AniJs takes as its travel scope from the **document**. To change it, call the **.setDOMRootTravelScope** and [[run AniJS again | Running-AniJS-repeatedly]].

```javascript
//Put #container as root travel scope
AniJS.setDOMRootTravelScope('#container');

//Runnig AniJS again
AniJS.run();
```
