
>[DIAPOSITIVAS](S3-recursos/formularios.pdf)

---

Bienvenidos a esta tercera sesión del prework. A lo largo de esta sesión:

- Seguiremos trabajando con HTML, explicando los formularios
- Trabajaremos con el terminal y explicaremos los comandos básicos
- Veremos una introducción a GIT, así como los comandos básicos
- Subiremos a GitHub nuestra primera web

## FORMULARIOS

Casi cualquier página web tiene formularios. Estos nos sirven para que el usuario pueda hacernos llegar una cierta información, ya sean:

- Sus datos para inscribirse a un curso
- Un email para suscribirse a una newsletter
- Nombre y apellidos para apuntarse a un correo….

Para crear un formulario usaremos la etiqueta form:

```html
<form>
  <!-- Aquí va todo el contenido del formulario -->
</form>
```

 

Para que el usuario pueda introducir información usamos las etiquetas input (igual que la de img, no hay apertura cierre). Con la etiqueta label damos información al usuario del contenido que tiene que meter dentro de ese input:

```html
<form>
  <label>
    Nombre
    <input>
  </label>
</form>

<!--  OTRA OPCIÓN -->

<form>
  <label for="nombre"> Nombre </label>
  <input id="nombre">
</form>
```

 

Todo campo input tiene que tener el atributo **name** que hace referencia a la información que enviaremos con el objetivo de poder identificar todos los inputs que mandemos dentro del formulario:

```html
<input name="nombre">
```

Para ayudar al usuario a entender la información que debe introducir en los campos tenemos el atributo **placeholder**

```html
<input name="nombre" placeholder="Introduce tu nombre..."/>
```

A la hora de validar la información que tienen que introducir el usuario en el input utilizaremos el atributo **type** que nos ayudará a controla el tipo de información que se introduce:

```html
<!-- Información de tipo texto -->
<input name="nombre" type="text" placeholder="Introduce tu nombre..."/>

<!-- Información de tipo numérico -->
<input name="edad" type="number" placeholder="Introduce tu edad..."/>

<!-- Información de tipo email -->
<input name="email" type="email" placeholder="Introduce tu email..."/>

<!-- Información de tipo password -->
<input name="email" type="password" placeholder="Introduce tu contraseña..."/>

<!-- Opción: Checkbox -->
<input name="opcion" type="checkbox">

<!-- Opción única: Radio -->
<input name="opcion" type="radio">

<!-- Archivos: File -->
<input name="opcion" type="file">
```

Por último, y cabe remarcarlo por separado, tenemos el tipo **submit** que nos va a permitir enviar toda la información del formulario

```html
<input type="submit">Enviar formulario</input>
```

¿Cómo se envía toda esa información al servidor? Con un atributo dentro del form que es action y que nos indicará la url de destino de ese formulario. A lo largo del máster entraremos en profundidad en este atributo.

```html
<form action="/">
```

Cuando queremos enviar una observación o un campo de texto largo, utilizamos la etiqueta **textarea** en vez de input. Los atributos **cols** y **rows** nos permite cambiar el tamaño por defecto del textarea.

```html
<label>
    Observaciones
    <textarea placeholder="Observaciones" name="observaciones" cols="30" rows="10"></textarea>
</label>
```

A la hora de desarrollar, es muy frecuente que el input tipo submit sea un botón, utilizaremos esta etiqueta ya que nos dará muchas más posibilidades de personalización.

```html
<button type="submit">Enviar formulario</button>
```

En este atributo tenemos la propiedad **reset** que nos borrará la información de todo el formulario.

```html
<button type="reset">Borrar información del formulario</button>
```
