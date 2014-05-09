Using AMD
=========================================

The Asynchronous Module Definition (AMD) format is an API for defining reusable modules that can be used across different frameworks. AMD was developed to provide a way to define modules such that they could be loaded asynchronously using the native browser script element-based mechanism.[1](http://www.sitepen.com/blog/2012/06/25/amd-the-definitive-source/) 

You can read more about AMD [here](http://requirejs.org/docs/whyamd.html#amd).


Example: 

```xml
<script type="text/javascript" src="libs/require.js/2.1.11/require.js" data-main="/js/app" ></script>
```

Example: 

```javascript
require(["anijs"], function(AniJS) {
	console.log(AniJS);
});
```

You can see a [Basic example where is used AniJS with RequireJS and Total.js(NodeJs web  framework)](https://github.com/anijs/examples/tree/gh-pages/anijs-requirejs-totaljs) created by [@gallegogt](https://github.com/gallegogt).
