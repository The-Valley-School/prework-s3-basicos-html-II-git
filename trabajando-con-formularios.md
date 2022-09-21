Vamos ahora a trabajar con un ejemplo de formulario. Tras crear nuestra estructura HTML y ver los campos que nos piden, empezamos a trabajar.

Creamos el formulario. Introducimos también el atributo action, aunque de momento no le hagamos mucho caso :

```html
<form action="/">
  <!-- Todo nuestro formulario -->
</form>
```

El primer y el segundo campo son el ‘Nombre’ y el ‘Apellido’, campos de tipo numérico que quedaría de esta forma:

 

```html
<label>
  <p>1) Nombre</p>
  <input type="text" name="nombre"/>
</label>
<br>
<label>
  <p>2) Apellidos</p>
  <input type="text" name="apellidos"/>
</label>
```

 

Tras estos campos de tipo **text** viene un campo de tipo numérico que es la edad:

```html
<label>
    <p>3) Edad</p>
    <input type="number" name="edad"/>
</label>
```

Llega el momento de la pregunta ‘¿Cómo te gusta el café?’. En este caso, y como la idea es seleccionar una única opción, usaremos **radio-buttons**. Tendremos que introducir un input por opción.

```html
<label>
    <p>4) ¿Cómo te gusta el café?</p>
    <input type="radio" name="comdida" value="solo"/> Solo
    <input type="radio" name="comdida" value="leche"/> Con leche
    <input type="radio" name="comdida" value="nada"/> No me gusta el café
</label>
```

La siguiente pregunta ‘¿Dónde ves las series?’ tiene la intención de que podamos seleccionar varias opciones, por lo tanto, utilizaríamos **checkbox** 

```html
<label>
    <p>5) ¿Dónde ves las series?</p>
    <input type="checkbox" name="comdida" value="hbo"/> HBO
    <input type="checkbox" name="comdida" value="netflix"/> Netflix
    <input type="checkbox" name="comdida" value="amazon"/> Amazon
</label>
```

Por último, tendríamos un campo grande que parece un **textarea**

```html
<label>
  <p>6) Cuéntanos más sobre ti</p>
  <textarea name="textarea" cols="40" rows="5" placeholder="Escribe lo que más te apasiona..."></textarea>
</label>
```

Nos queda el botón de enviar información y el limpiar el formulario:

```html
<button type="submit">
    Enviar información
</button>
<button type="reset">
    Limpiar formulario
</button>
```

¡Ya lo tendríamos! Quedaría probar que toda la información se esté enviando correctamente y listo. Os dejamos el resultado final:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Cúales son tus gustos?</title>
</head>
<body>
    <h1>¿Cúales son tus gustos?</h1>
    <hr>
    <form action="/">
        <label>
            <p>1) Nombre</p>
            <input type="text" name="nombre"/>
        </label>
        <br>
        <label>
            <p>2) Apellidos</p>
            <input type="text" name="apellidos"/>
        </label>
        <br>
        <label>
            <p>3) Edad</p>
            <input type="number" name="edad"/>
        </label>
        <br>
        <label>
            <p>4) ¿Cómo te gusta el café?</p>
            <input type="radio" name="comdida" value="solo"/> Solo
            <input type="radio" name="comdida" value="leche"/> Con leche
            <input type="radio" name="comdida" value="nada"/> No me gusta el café
        </label>
        <label>
            <p>5) ¿Dónde ves las series?</p>
            <input type="checkbox" name="comdida" value="hbo"/> HBO
            <input type="checkbox" name="comdida" value="netflix"/> Netflix
            <input type="checkbox" name="comdida" value="amazon"/> Amazon
        </label>
        <label>
          <p>6) Cuéntanos más sobre ti</p>
          <textarea name="textarea" cols="40" rows="5" placeholder="Escribe lo que más te apasiona..."></textarea>
        </label>
        <br>
        <button type="submit">
            Enviar información
        </button>
        <button type="reset">
            Limpiar formulario
        </button>
    </form>
</body>
</html>
```
