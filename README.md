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





# CSS

Los `id` se seleccionan en CSS con `#`

ejm:

```html
#intro {
	...
}
```

Las `clases` se seleccionan con `.`

ejemplo:

```html
.movie {
	...
}
```

**Nota: El mismo nombre de la clase se puede dar a múltiples elementos**



## Variables en CSS

### Creación de variables en CSS

Las variables se crean de la siguiente manera:

```css
:root {
	--nombreVariable: #13c1cd;
}
```

Lo ideal es trabajar el color en hexadecimal

El orden de los archivos es el siguiente:

![archivoscss](D:\Descargas_si\archivoscss.jpeg)

### Importar archivos CSS dentro de otro CSS:

Se usa la siguiente sintaxis:

```css
@import url(______);
```

Dentro de los paréntesis va **el nombre del archivo**

Ejemplo:

```css
body {
	background: var(--colorPrimary);
}
```

**Reseteo universal por móvil:**

En variables:

```css
* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}
```



## Modelo en caja

Adaptar el fondo a un párrafo:

### Display in-line:

`display: inline;` Este respeta el display. Se usa cuando una caja hereda a otra

`display: inline-block;` Respeta el display en bloque

`margin:   ;` Afecta a la caja en sí

`padding:   ;` Separa el contenido que está dentro de la caja

### Texto en CSS

#### Cambiar tamaño de texto:

`font-size:   ;`

**Se debe trabajar en unidades `rem` esto mejora el menú responsivo**.

#### Alinear texto:

`text-align: ;`

Se indica al programa hacia dónde se quiere alinear el texto

Unidades que se pueden emplear:

​	`center` centra el texto

​	`right` alínea el texto hacia la derecha

​	`left` alínea el texto hacia la izquierda

​	`justify` Justifica el texto

#### Decoración en el texto:

Se puede añadir texto decorativo usando `text-decoration:___;`

Se pueden usar los siguientes comandos:

​	`underline` subraya el texto

​	`overlined` traza una línea sobre el texto

​	`line-through` Traza una línea tachando el texto

​	`underline overline` traza una línea superior e inferior en el texto

#### Transformar texto

Para transformar el texto se usa `text-transform:___;` con las siguientes propiedades:

​	`capitalize` Convierte el texto a mayúsculas iniciales

​	`uppercase` Convierte el texto a mayúscula 

​	`lowercase` Convierte el texto todo a minúscula

Ejemplo:

```css
clase {
	text-transform: capitalize;
}
```

#### Sombras en textos

Las sombras se añaden usando `text-shadow`:

```css
p {
	text-shadow: ___px ___px;
}
```

Se da un desplazamiento horizontal y seguidamente uno vertical, desplazándolo en pixeles.

#### Tipo de fuente

Para cambiar el tipo de fuente se emplea `font-family:___;`

#### Estilos de listas

##### Controlar tipos de marcadores

`list-style-type` controla el tipo de marcadores

Se puede usar los siguientes atributos:

​	`square`

​	`inside`

​	`url(____)`

`list-style-position` controla la posición de los marcadores

Se puede usar los siguientes atributos:

​	`inside`

​	`outside`

`list-style-image` añade imágenes personalizadas como marcadores

Se puede usar los siguientes atributos:

​	`url("_____")`

### Box-model

Cada elemento tiene:

- Contenido
- Padding
- Borde
- Margin

Cada elemento HTML es una caja rectangular con 4 capas.

El contenido es la más interna y contiene texto e imágenes.

#### Elementos de bloque

Ocupan todo el ancho de la página

#### Elementos en línea

Sólo ocupan el ancho de su contenido



## FlexBox

En esta herramienta se usa el atributo `display` el cual anula comportamientos predeterminados de los elementos en línea y de nivel de bloque.

`display: block;` Hace que un elemento se comporte como uno de bloque

`display: inline;` Hace que un elemento se comporte como uno de línea

`display: flex;` Crea un contenedor flexible

Para organizar los elementos secundarios automáticamente dentro de un contenedor principal, se necesita aplicar `display: flex;` al contenedor padre

Algunos atributos que se pueden usar son:

​	`flex-direction: ___;` Permite organizar los elementos dentro de un contenedor Flex, en una dirección específica. Se puede usar con:

- ​		`row`
- ​		`row-reverse`
- ​		`column`
- ​		`column-reverse`

​	`flex-wrap: wrap;` Los elementos flex son colocados en varias líneas

​	`flex-wrap: nowrap;` Los elementos flex son distribuidos en una sola línea, lo cual puede llevar a que se desborde el contenedor flex

​	`flex-wrap: wrap-reverse;` Ajusta los elementos y los invierte



con `flex-grow:___;`permite que un elemento crezca proporcional al espacio disponible dentro del contenedor. En este se pone un número después de los dos puntos.

Con `flex-shrink:___;`se adapta el diseño a pantallas más pequeñas. En este se pone un número después de los dos puntos.



## Posicionamiento

Se busca dar una posición exacta a un elemento.

### Absolute

Aplicar la propiedad `absolute` le quita la propiedad estática, haciendo que no tenga en cuenta el contenedor padre del elemento. 

ejemplo:

```css
button {
	position: absolute;
}
```

Se pueden asignar las siguientes coordenadas:

`left`, `top`, `right`, `button`

ejemplo:

```css
button {
	position: absolute;
    position: right;
}
```

### Fixed

Mantiene en el mismo lugar un elemento, incluso si se desplaza de página.

**ESTE SE USA PARA HACER QUE LOS MENÚS SE QUEDEN QUIETOS AL HACER SCROLL**

Ejemplo:

```css
button {
	position: fixed;
    top: 0;
}
```

### Relative

Se establece la posición estática (predeterminada) del elemento, haciendo que esta sea la nueva referencia. Esta propiedad se aplica al elemento padre para dar una ubicación específica a los elementos hijos dentro de este.

El hijo debe establecerse en `position: absolute;`

### Justify-content

En flex se usa `justify-content` para distribuir los elementos de una forma específica. Los atributos que lo componen son: 

`justify-content: flex-end;` alinea elementos al lado derecho del contenedor

`justify-content: flex-center;` alinea elementos en el centro del contenedor

`justify-content: space-between;` Muestra elementos con la misma distancia entre ellos

`justify-content: space-around;` Muestra elementos con la misma separación alrededor de ellos

### Align Items

En flex se una `align-items` para distribuir los elementos de forma específica en el eje vertical

`align-items: flex-end;` Alinea elementos en la parte inferior del contenedor

`align-items: center;` Alinea elementos en el centro verticalmente

`align-items: baseline;` Alinea elementos en la línea base del contenedor

`align-items: stretch;` estira los elementos para que se ajusten al contenedor

### Flex Direction

Con `flex-direction` se establece la dirección que toma el contenido, bien sea columnas o filas.

Tiene las siguientes propiedades:

`flex-direction: row;`

`flex-direction: row-reverse;`

`flex-direction: column;`

`flex-direction: column-reverse;`

**Para modificar un elemento específico se puede usar `align-self`**

### Align Content

Ajusta las líneas dentro de un contenedor flex cuando hay espacio extra en el eje transversal.

Toma los siguientes atributos:

`align-content: flex-start;`

`align-content: flex-end;`

`align-content: center;`

`align-content: space-between;`

`align-content: space-around;`

`align-content: stretch;`

