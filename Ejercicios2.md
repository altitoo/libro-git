# 4. Ramas

## Ejercicio 1

`git branch bibliografia` Creamos la rama bibliografia.
`git branch -av` para mostrar las ramas.

## Ejercicio 2

 1. `cat > temas/tema4.txt` y escribimos `En este capítulo veremos cómo usar GitHub para alojar repositorios en remoto.`
 2. `git add .`
 3. `git commit -m "Añadido tema 4.` Comiteamos
 4. `git log --graph --all --oneline` Historia del repo incluyendo ramas.

## Ejercicio 3

 1. `git checkout bibliografia` Cambiamos a la rama bibliografia.
 2. `cat > bibliografia.txt` Creamos el archivo y añadimos `- Scott Chacon and Ben Straub. Pro Git. Apress.` 
 3. `git add .` Añadimos 
 4. `git commit -m"Añadida primera referencia bibliografica"` Comiteamos
 5. Mostramos historial `git log --graph --all --oneline`