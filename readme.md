-> ¿Qué comando utilizaste en el paso 11? ¿Por qué?

git reset --hard HEAD~1. 

De esta manera, he desecho el último commit y lo que había en el working copy para que quedase como antes.



-> ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?  

Primero he usado el comando git reflog para para ver el histórico de los cambios y el id que ha ido asignando a cada uno de ellos. A continuación he usado el paso al que queremos volver y crearemos un código con el comando git reset --hard añadiendo al final el id del paso al que queremos volver. En mi caso quedaría así:

git reset --hard 0fcac7d



-> El merge del paso 13, ¿Causó algún conflicto? ¿Por qué? 

Despues de comprobar que nos encontramos en la rama styled, he usado el comando Git merge master. De esta manera styled absorbe la rama master



-> El merge del paso 19, ¿Causó algún conflicto? ¿Por qué? 

Ejecuto el comando git merge htmlify y muestra el siguiente error:

Auto-merging git-nuestro.md
CONFLICT (content): Merge conflict in git-nuestro.md
Automatic merge failed; fix conflicts and then commit the result.

El conflicto es debido a que dos archivos han sido editados en la misma línea en dos ramas diferentes. Lo editamos para quedarnos con los valores de la rama styled.

Ejecutamos un git add del archivo y realizamos el commit indicando como hemos solucionado la incidencia.



-> El merge del paso 21, ¿Causó algún conflicto? ¿Por qué? 

He usado el comando Git checkout master para ir a la rama maste y a continuación el comando git merge styled.

Ha hecho un merge de tipo fast-forward pero no juraría que no ha dado ningún conflicto.



-> ¿Qué comando o comandos utilizaste en el paso 25? 

git log --graph --decorate --pretty=oneline



-> El merge del paso 26, ¿Podría ser fast forward? ¿Por qué? 

Lo he intentado y en principio no me ha dado ningún problema. Entiendo que las dos posibilidades son factibles.



-> ¿Qué comando o comandos utilizaste en el paso 27? 

Git reset HEAD~1



-> ¿Qué comando o comandos utilizaste en el paso 28? 

Despues del anterior paso, el archivo git-nuestro.md volvió a llamarse como su versión inicial, con lo que hice un git add y posteriormente un commit.



-> ¿Qué comando o comandos utilizaste en el paso 29? 

git branch -D title



-> ¿Qué comando o comandos utilizaste en el paso 30? 

Después de hacer un reflog he buscado cual era el id al que teníamos que volver y he usado el siguiente comando: git reset --hard 11b48b1



-> ¿Qué comando o comandos usaste en el paso 32? 

He usado el comando git log para buscar el id completo del comit inicial y a continuación: git reset --hard 760cbc44db06be103140cce3c0099dc0e46ec8a0



-> ¿Qué comando o comandos usaste en el punto 33?

Al igual que el anterior, pero usando el id del último commit realizado: git reset --hard 8a30ef9
