Test Cases
============================================

##Define animations declaratively

###Bad Declaration Sintax

###Define a trigger event for the animation (if).
- Define empty event.
**Expected behavior**

- Define events that do not exist.
**Expected behavior**

- Define 3 events random. 
**Expected behavior**

###Define the elements from which the trigger event is launched (on).
- Define empty selector.
- Define selector of an element that does not exist.
- Define selector with rare characters. 

###Animation behavior definition.(do)
- Define empty animation.
- Define an animation that does not exist. 

###Animation elements target definition.(to)
- Define empty selector.
- Define selector of an element that does not exist.
- Define selector with rare characters.

###Execute a function before animation run.
- Create an empty function.
- Create a function that it is not registered in the helper.
- Create in the a variable with the same name of the function.

###Stop animation execution before running it.
- Stop the animation.
- Do not stop the animation.


###Execute a function after animation run.
- Create an empty function.
- Create a function that it is not registered in the helper.
- Create in the a variable with the same name of the function.

###Helpers instance definition.
- Define a null helper.
- Definir a helper to be a function.
- Register empty helper.

###animationEnd and transitionEnd normalization.
- Set animations in, at least 3 HTML elements of the page.
- Set tansitions listener in, at least 3 HTML elements of the page.

###Attach events from window and document objects
- Define an event that do not exist in the window.
- Define an event that do not exist in the document.

###Running AniJS repeatedly.
- Run AniJS at least 10 times .
- See if RAM goes up.

###Change the root DOM scope.
- Change root scope, to one that do not exist.
- Pass as argument empty selector.

###Manage animations using JavaScript.
- Create an animation with empty event.

- Create an animation with event that does not exist.

- Create an animation with an event object.

- Create an animation with empty eventTarget.

- Create an animation with null eventTarget.

- Create an animation with an objeto eventTarget.

- Create an animation with empty behaviorTarget.

- Create an animation with null behaviorTarget.

- Create an animation with behaviorTarget object.

- Create an animation with empty behavior.

- Create an animation with null behavior.

- Create an animation with behavior object.

- Create an animation with empty after.

- Create an animation with after that does not exist.

- Create an animation with after object.

- Create an animation with empty before .

- Create an animation with before that does not exist.

- Create an animation with an object before.

- Create an animation with empty helper.

- Create an animation with a helper that does not exist.

- Create an animation with object helper.


###Purge events from any node.

- Attach several events to a node.
- Remove several events from a node.

###Register new helpers.

- Register a null helper.
- Register a helper that it's a function.
- Register a helper with the same name of one existent.(e.g Default)

###Attach new functions to the helpers.
- Add a function to a helper.
- Overwrite a function in the helper.

###removeAnim Default helper function.
- Run an animation and observe if it's removed.
