Handling Animations Using JavaScript
=====================================

You can create animation directamente en JavaScript mediante la funcion **createAnimation**.

```javascript

	//When click in footer anim header with bounceIn animation.
    AniJS.createAnimation([{
        event: 'click',
        eventTarget: 'footer',
        behaviorTarget: 'header',
        behavior: 'bounceIn',
        before: function(e, animationContext){
			if( someVariable ){
				//Run the animation
				animationContext.run()
			}
    	}
    }]);

```
