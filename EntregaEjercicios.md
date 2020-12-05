# 1. Creación y actualización de repositorios

## Ejercicio 1

Configuramos el nombre de usuario:

`git config --global user.name "ALBERTO VICENTE"`

Configuramos el email:
`git config --global user.email "alberto.vicente.bernad@gmail.com"`

Activa el coloreado de salida:

`git config --global color.ui auto`

Esta linea de codigo activa los colores que estan por defecto en git.
`auto` Intenta usar colores en las terminales que lo permitan.
`color.ui` Es la configuracion que incluye todos los colores de los que dispone git por defecto.

Con `git config --list` comprobamos que todo lo anterior esta correcto.

## Ejercicio 2

Vamos con el comando cd a la ruta que deseemos y ahi se creara el repositorio con el siguiente comando.

`git init apuntes` Creara el repositorio con el nombre de 'apuntes'.

Con el comando `ls` o `dir` podemos ver el contenido de la carpeta en la que estamos. En este caso solo aparecera apuntes

## Ejercicio 3

 1. Accedemos a la carpeta con cd apuntes/ y utilizamos `git status ` 
 2. `vim indice.txt` y se nos abrira un editor de texto. Editamos el archivo y lo guardamos usando `:w` y salimos con `:q`. Para comprobarlo usamos `cat indice.txt`
 3. Comprobar el estado de nuevo `git status ` y nos dice que se hay untracked files y que utilicemos git add 'file'.
 4. utilizamos `git add indice.txt`
 5. Utilizamos `git status` Nos muestra como hay cambios que todabia no hemos hecho commit.
   
## Ejercicio 4

Realizar commit.

`git commit --m "Añadido índice de los apuntes."` 

Comprobar el status 

`git status`

Nos dice que no hay nada que commitear y que estamos en la rama master.

## Ejercicio 5

 1. Con el comando `vim indice.txt` accedemos al archivo y realizamos los cambios.
 2. `git status` se muestran los cambios 
 3. `git add indice.txt` y luego `git commit --m "Modificar indice.txt"` esto creara un segundo commit.
   
## Ejercicio 6

 1. Utilizamos `git log --patch` muestra los cambios respecto al ultimo commit.
 2. Con `git commit --amend "Añadido tema 3 sobre gestión de ramas"` modificamos el mensaje del ultimo commit.
 3. `git log --patch`

&nbsp;
___

# 2. Historial de cambios

## Ejercicio 1

 1. Mostrar historial `git log`
 2. `mkdir temas` creara la carpeta `cd temas/` accedemos a ella `vim tema1.txt` y escribimos, confirmamos con `:w` y salimos con `:q` 
 3. `git add tema1.txt` añadimos el archivo.
 4. `git commit --m "Añadido tema 1."` hacemos commit.
 5. Volvemos a ver el historial `git log`

## Ejercicio 2

 1. `cat > tema2.txt` creamos el archivo y escribimos dentro de el el texto
 2. `git add tema2.txt`
 3. `git commit --m "Añadido el tema2."` commiteamos
 4. `git diff HEAD~2..HEAD` mostrara las diferencias entre la ultima y las 2 anteriores

## Ejercicio 3

 1. `cat > temas/tema3.txt` y pegamos el texto. Para salir control + c
 2. `git add .` 
 3. `git commit -m "Añadido tema 3."`
 4. `git diff 605d6..HEAD` y mostrara la diferencia

## Ejercicio 4
 1. `echo "Tema 5: Conceptos avanzados" >> indice.txt` crea el archivo y lo edita añadiendo esa frase.
 2. `git add .`
 3. `git commit -m "Añadido el tema 5 al indice.`
 4. `git annotate indice.txt` Muestra quien ha hecho los cambios sobre el fichero. 
 
# 3. Deshacer cambios

## Ejercicio 1

 1. `nano indice.txt` y eliminamos la ultima fila del archivo
 2. `git status` comprobamos el estado
 3. `git checkout -- indice.txt` desacemos los cambios
 4. `git status` 

## Ejercicio 2

 1. `nano indice.txt` y eliminamos la ultima fila del archivo
 2. `git add .` 
 3. `git status`
 4. `git reset indice.txt` quitar de add
 5. `git status` Volvemos a comprobar los cambios 
 6. `git checkout -- indice.txt` deshacemos los cambios 
 7. `git status`

## Ejercicio 3

 1. `nano indice.txt` Borramos la ultima linea otra vez
 2. `rm temas/tema3.txt` 
 3. `touch temas/tema4.txt` creamos el nuevo archivo
 4. `git add .`
 5. `git status`
 6. `git reset`
 7. `git status`
 8. `git checkout --` y `git clean -f` para deshacer
 9. `git status`

## Ejercicio 4

 1. `nano indice.txt` borramos la ultima linea
 2. `rm temas/tema3.txt` borramos el archivo
 3. `git add .`
 4. `git status`
 5. `git reset --soft HEAD~1` Manteniendo los cambios de la zona de trabajo 
 6. `git status` y `git log`
 7. `git commit -m "Borrado Accidental"`
 8. `git reset --hard HEAD~1` Sin mantener los cambios 
 9. `git status` y `git log` comprobamos.
 
&nbsp;
___

