En este archivo está contenido todo lo que concierne a los apuntes de HTML y CSS seguidamente. Estos apuntes ya se encontraban en mi cuaderno de notas, donde he consignado todo lo referente a este módulo.



# HTML

## Secciones de la página web:

| Header  |       |
| :-----: | :---: |
|   nav   |       |
| section | aside |
| article |       |
| footer  |       |



### Encabezado:

se define con la etiqueta 

```html
<header></header>
```

En esta van íconos, logos, entre otros.



### Barra de navegación:

Incluye enlaces o botones que llevan a otras páginas del website, por ejemplo:

```html
<nav>
    <a href="#">link 1</a>
    <a href="#">link 2</a>
</nav>
```

El menú de navegación también puede ser parte del encabezado.



### Contenido Principal

Se define con 

```html
<main></main>
```

Se puede incluir subsecciones representadas con `article` y `section`:

```html
<article></article>
<section></section>
```

- `article` encierra un bloque de contenido. Puede tener diferentes sections

- `section` se puede agrupar una sola parte de la página que constituye una sola pieza de funcionalidad (mapa,conjunto de titulares). **Cada sección se inicia con un título**. 

  

### Otras secciones

`aside` define contenidos que no se relacionan directamente con el contenido principal.

```html
<aside></aside>
```



### Pie de página

Puede contener enlaces, notas de copyright, etc. se crea con:

```html
<footer></footer>
```

Ejemplo:

```html
<footer>
	<p align="center">
        Copyright
    </p>
</footer>
```



## Formularios

Los elementos del formulario se contienen dentro de `form`

```html
<form>
    
</form>
```

Al formulario se le puede añadir entradas usando `input`:

```html
<input type="text"> 
```

`type` define el tipo de elemento de entrada, la cual sería como una caja.

#### Tipos de input:

- email
- text
- tel

Estos hacen que el teclado se distribuya de manera diferente dependiendo del tipo de entrada que se vaya a ingresar

#### Etiquetas:

Se puede añadir etiquetas a los elementos.

ejemplo:

```html
<input type="text" id="name">
```

El **id** es único para cada elemento

#### Asociar elementos:

Se puede hacer de la siguiente manera:

```html
<label for="name">Name</label>
<input type="text" id="name">
```

`for` asocia el label al **id** con el nombre **"name"**

Se vería un texto al lado de la caja de input

#### Placeholder:

Es el texto que ejemplifica lo que se debe ingresar en la entrada.

Ejemplo:

```html
<input type="text" id="name" placeholder="John Smith">
```

Se ve el texto dentro de la caja de entrada, y una vez se ingresan datos, esta se borra

#### Checkboxe:

Se pueden implementar usando la siguiente línea de código:

```html
<input type="checkbox">
```

#### Botones de radio:

Para agrupar varios elementos en selectores de radio, todos deben tener asignado el mismo nombre.

Ejemplo:

```html
<input type="radio" name="tittle" id="mr">
```

En este caso, "title" debe asignarse a todas las demás entradas que se necesite agrupar con el mismo tipo

#### Textarea

Cuando se requiere el ingreso de varias líneas de texto, se puede implementar el siguiente tipo de entrada:

```html
<textarea id="message">

</textarea>
```

#### Drop-down:

Para hacer un drop-down se usa `select`:

```html
<select>
    <option>Red</option>
    <option>Blue</option>
</select>
```



## Insertar audio

Se puede añadir audio a la página web usando `audio src`:

```html
<audio src="" controls>No se puede reproducir el audio</audio>
```

El texto dentro de la etiqueta aparece cuando no se puede reproducir el audio.

`src` hace referencia al source o la dirección donde está el archivo de audio.

`controls` se utiliza para asignarle controles de audio.

**Se puede añadir diferentes fuentes de audio**



## Insertar vídeos:

Se implementa el mismo modelo de audio, pero se utiliza la etiqueta `video`:

```html
<video controls width="500px" heigh="500px"></video>
```

Con `width` y `heigh` se modifica el tamaño del vídeo en horizontal y vertical

#### Insertar vídeos desde Youtube:

1. Se ingresa al vídeo que se quiere incorporar.
2. Click en "Compartir".
3. Click en "Incorporar"
4. Copiar el enlace y pegarlo en el código.



