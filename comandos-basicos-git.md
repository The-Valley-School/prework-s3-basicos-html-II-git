Vamos a llevar ahora a la práctica todo el flujo de trabajo que hemos aprendido en la sesión anterior. Lo primero que hacemos es crear un proyecto ejemploGit en nuestro VSC y abrir la terminal posicionándonos en nuestro directorio.

Tras esta primera fase toca comunicar que el control de versiones va a a estar gestionado por GIT, para ello usamos el comando:

 

```bash
git init
```

 

Este comando crea una carpeta git oculta, con una serie de contenido a nivel de implementación que nos permiten gestionar las versiones.

Tras el **git init** vamos a lanzar nuestro segundo comando, **git status** que nos indica si se ha realizado algún cambio. 

  

```bash
git status
```

  

Cuando yo creo un fichero1.txt en mi proyecto y vuelvo a hacer un git status nos indicará que se ha añadido un nuevo fichero, para añadirlo tendremos que utilizar el comando git add

  

```bash
git add fichero.txt

// Podemos indicar que nos añadan todos los ficheros txt (git add .txt)
// Podemos indicar también que nos añadan todos los ficheros (git add .)
```

  

Ya tendríamos entonces un nuevo fichero en fase stage susceptible de ser subido a nuestro repositorio local. 

Es importante que si después de subir a fase stage un archivo lo modificamos, seamos conscientes de que estos últimos cambios no se van a subir a menos que volvamos a hacer un **git add**

Una vez tenemos los ficheros que queramos subir en fase stage, hacemos nuestro commit, incluyendo un mensaje con los cambios que hemos realizado:

  

```bash
git commit -m "Nuestro primer commit del proyecto"
```

  

Os va a parecer raro, pero si queremos eliminar un fichero, tendremos que incluir con **git add**  ese cambio de eliminación de fichero. Con el comando **git restore** volveríamos atrás y se desharía la eliminación del fichero, descartando los cambios.
