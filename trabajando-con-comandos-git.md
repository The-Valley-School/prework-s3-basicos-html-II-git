Vamos a asentar conocimientos de comandos básicos GIT.  Nos piden:

 


1)  Crea una carpeta de proyecto desde la terminal.
2)  Haz un git init para empezar a trabajar con git 
    en el proyecto.
3)  Haz un git status
4)  Crea un fichero, comprueba el estado, añádelo a 
    fase stage y haz un commit on el mensaje ‘Mi primer
    commit’
5)  Crea el fichero 2 y 3
6)  Añade a fase stage el fichero 2
7)  Haz un commit con fichero 2
8)  Añande a fase stage el fichero 3 y haz un nuevo 
    commit
9)  Elimina el fichero 3
10) Commitea el cambio
11) Elimina el fichero 2
12) Haz un git restore para recuperarlo.


  

Vamos poco a poco. 

1) Para crear la carpeta  usaremos el comando mkdir. Una vez creada, entraremos al proyecto

 

```bash
mkdir proyecto
cd proyecto
```

  

2 y 3) Hacemos el git init que se indica y posteriormente un git status para verificar

 

```bash
git init
git status
```

  

4) Creamos el fichero, comprobamos que está pendiente de añadir, lo agregamos y comiteamos

```bash
touch fichero1.txt
git status
git add fichero1.txt
git status
git commit -m "Mi primer commit"
```

  

5) Creamos los dos ficheros que nos piden

```bash
touch fichero2.txt
touch fichero3.txt
git status
```

6 y 7) Añadimos a fase stage el fichero dos y lo comiteamos

  

```bash
git status
git add fichero2.txt
git status
git commit -m "Añadimos fichero2"
```

  

8) Hacemos lo mismo con el fichero 3

  

```bash
git status
git add fichero3.txt
git status
git commit -m "Añadimos fichero3"
```

  

9) Eliminamos el fichero 3 y comiteamos

   

```bash
git status
rm fichero3.txt
git status
git add fichero3.txt
git status
git commit -m 'Eliminamos fichero3'
```

   

10 y 11) Eliminamos el fichero2 y hacemos un git restore para revertir los cambios.

   

```bash
git status
rm fichero2.txt
git status
git restore fichero2.txt
git status
```
