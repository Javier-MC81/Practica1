# Practica1
-¿Qué comando utilizaste en el paso 11?¿Por qué?
git reset --hard HEAD~1  Porque es la forma de volver al commit anterior perdiendo los cambios en el working copy. 
-¿Qué comando o comandos utilizaste en el paso 12?¿Por qué?
git reflog (para rastrear el ID del cmmit donde está modificado el archivo )
git reset 9103c94 ( vuelvo con HEAD  y la rama styled al commit del archivo modificado para rehacer el commit ).
-El merge del paso 13, ¿Causó algún conflicto?¿Por qué?
No. Realmente no hace nada porque la rama styled ya disfruta del commit de la rama main y no tiene que hacer nada.
-El merge del paso 19, ¿Causó algún conflicto?¿Por qué?
Sí. Se produce porque el merge que se hace es no fast forward ya que el mismo archivo git-nuestro de las dos ramas htmlify y styled tienen diferencias. 
Git no sabe con cuál de los dos quedarse. Se procede a resolver el conflicto quedándonos con la versión del commit de la rama styled.
-El merge del paso 21, ¿Causó algún conflicto?¿Por qué?
No. Se trata de un merge fast forward. Se mueve HEAD con el puntero de la rama master al comit donde está la rama styled y así puede disfrutar de los commits que se ven desde styled. 
No crea ningún commit nuevo ni lo necesita hacer.
-¿Qué comando utilizaste en el paso 25?
git log --graph
-El merge del paso 26, ¿Podría ser fast forward?¿Por qué?
Sí. Porque no hubiera perdido ningún commit si HEAD y la rama main se hubieran movido al commit donde está la rama title. 
Hubiera bastado con mover HEAD/Main a ese commit de la rama title. Si no lo hubiera forzado a ser "no fast forward", se hubiera ahorrado el commit nuevo.
-¿Qué comando o comandos utilizaste en el paso 27?¿Por qué?
git reset HEAD~1. Para volver al commit padre anterior que lo reconoce como aquel donde estaba antes la rama main y no perder los cambios del working copy. 
Con un hard los hubiéramos perdido y con un HEAD~2 se hubiera ido a la rama del title.
-¿Qué comando o comandos utilizaste en el paso 28?¿Por qué?
git restore git-nuestro.md. Para que restaure el archivo en su último estado guardado en ese commit.
-¿Qué comando o comandos utilizaste en el paso 29?¿Por qué?
git branch -D title. Porque si lo hacemos -d, se pierde el commit donde se encuentra esa rama y no se puede alcanzar desde ninguna otra. 
-¿Qué comando o comandos utilizaste en el paso 30?¿Por qué?
git reflog (para rastrear el ID del cmmit donde está el merge )
git reset  a33e667( vuelvo con HEAD  y la rama main al commit del merge).
git restore git-nuestro.md . Para restaurar el archivo con el título tal y como estaba antes en ese commit.
-¿Qué comando o comandos utilizaste en el paso 32?¿Por qué?
git reflog (para rastrear el ID del commit donde creé el git-nuestro )
git reset  122e079 (vuelvo con HEAD  y la rama main al commit inicial).
-¿Qué comando o comandos utilizaste en el paso 33?¿Por qué?
git reflog (para rastrear el ID del commit del merge entre las ramas main y title )
git reset  a33e667 (vuelvo con HEAD  y la rama main a ese commit).
