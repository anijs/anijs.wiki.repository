Test Cases
============================================

##Define animations declaratively

###Define a trigger event for the animation (if).
- Definir el evento vacío.
**Comportamiento esperado**

- Definir eventos que no existan.
**Comportamiento esperado**

- Definir 3 eventos al azar. 
**Comportamiento esperado**

###Define the elements from which the trigger event is launched (on).
- Definir el selector vacío.
- Definir selector de un elemento que no exista.
- Definir selector con caracteres raros. 

###Animation behavior definition.(do)
- Definir animacion vacia.
- Definir animacion que no exista. 

###Animation elements target definition.(to)
- Definir el selector vacío.
- Definir selector de un elemento que no exista.
- Definir selector con caracteres raros.

###Execute a function before animation run.
- Crear una funcion vacía.
- Crear una funcion que no este registrada en el helper.
- Crear en el helper una variable con el mismo nombre de la función.

###Stop animation execution before running it.
- Detener la animacion.
- No detener la animacion.


###Execute a function after animation run.
- Crear una funcion vacía.
- Crear una funcion que no este registrada en el helper.
- Crear en el helper una variable con el mismo nombre de la función.

###Helpers instance definition.
- Definir un helper nulo.
- Definir un helper que sea una function.
- Registrar helper vacio.

###animationEnd and transitionEnd normalization.
- Poner listener animaciones en al menos 3 elementos HTML de la página.
- Poner listener trancisiones en al menos 3 elementos HTML de la página.

###Attach events from window and document objects
- Definir un evento que no exista en el window.
- Definir un evento que no exista en el document.

###Running AniJS repeatedly.
- Correr AniJS al menos 10 veces seguidas.
- Ver si la RAM sube.

###Change the root DOM scope.
- Cambiar root scope, a uno que no exista.
- Pasar el selector vacío.

###Manage animations using JavaScript.
- Crear una animacion con el event vacío.

- Crear una animacion con un event que no exista.

- Crear una animacion con un objeto evento.

- Crear una animacion con el eventTarget vacío.

- Crear una animacion con un eventTarget que no exista.

- Crear una animacion con un objeto eventTarget.

- Crear una animacion con el behaviorTarget vacío.

- Crear una animacion con un behaviorTarget que no exista.

- Crear una animacion con un objeto behaviorTarget.

- Crear una animacion con el behavior vacío.

- Crear una animacion con un behavior que no exista.

- Crear una animacion con un objeto behavior.

- Crear una animacion con el after vacío.

- Crear una animacion con un after que no exista.

- Crear una animacion con un objeto after.

- Crear una animacion con el before vacío.

- Crear una animacion con un before que no exista.

- Crear una animacion con un objeto before.

- Crear una animacion con el helper vacío.

- Crear una animacion con un helper que no exista.

- Crear una animacion con un objeto helper.


###Purge events from any node.

- Atachar varios eventos a un nodo.
- Quitar varios eventos de un nodo.

###Register new helpers.

- Registrar un helper nulo.
- Registrar un helper que es una function.
- Registrar un helper con el mismo nombre de uno que yan exista.(Default por ejemplo)

###Attach new functions to the helpers.
- Agregar una function a un helper.
- Sobreescribir una function que ya exista en el helper.

###removeAnim Default helper function.
- Correr una animación y ver si se quita.
