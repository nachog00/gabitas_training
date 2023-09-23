# Agregando estilos

En este capitulo vamos a aprender a agregar estilos a nuestra pagina web.

## Que es CSS?

CSS es un lenguaje de estilos, significa Cascading Style Sheets.

## Como se usa?

Es muy sencillo. Para aplicar estilos hacen falta dos cosas:
* un selector de elementos
* una lista de propiedades y valores
  
Por ejemplo, si queremos cambiar el color de fondo de nuestra pagina web, podemos hacerlo de la siguiente manera:

```css
body {
    background-color: red;
}
```

En este caso el selector es `body` y la propiedad es `background-color`. El valor de la propiedad es `red`.

## Como se agrega?

Para agregar estilos a nuestra pagina web, una forma es agregar un elemento `style` dentro del elemento `head` de nuestro documento HTML.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    ...
    <style>
        body {
            background-color: red;
        }
    </style>
</head>
<body>
    ...
</body>
</html>
```

Pero esto hace que nuestro index sea muy largo y dificil de leer. Por eso, lo que vamos a hacer es crear un archivo CSS y agregarlo a nuestro documento HTML.

Para eso, vamos a crear un archivo llamado `styles.css` dentro de la carpeta `styles`. Luego, vamos a agregar el siguiente elemento `link` dentro del elemento `head` de nuestro documento HTML.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    ...
    <link rel="stylesheet" href="./styles/styles.css">
</head>
<body>
    ...
</body>
</html>
```

## Como se seleccionan los elementos?

Hay varias formas de seleccionar elementos. La mas sencilla es por nombre de etiqueta. Por ejemplo, si queremos seleccionar todos los elementos `p` de nuestro documento HTML, podemos hacerlo de la siguiente manera:

```css
p {
    color: red;
}
```

### Por clase

Tambien podemos seleccionar elementos por clase. Para eso, tenemos que agregar un atributo `class` a nuestro elemento HTML. Por ejemplo, si queremos seleccionar todos los elementos `p` que tengan la clase `red`, podemos hacerlo de la siguiente manera:

```html
<p class="red">Este parrafo es rojo</p>
```

```css
p.red {
    color: red;
}
```

### Por id

Tambien podemos seleccionar elementos por id. Para eso, tenemos que agregar un atributo `id` a nuestro elemento HTML. Por ejemplo, si queremos seleccionar el elemento `p` que tenga el id `red-text`, podemos hacerlo de la siguiente manera:

```html
<p id="red-text">Este parrafo es rojo</p>
```

```css
#red-text {
    color: red;
}
```

### Como se seleccionan elementos anidados?

Para seleccionar elementos anidados, tenemos que separar los selectores por un espacio. Por ejemplo, si queremos seleccionar todos los elementos `p` que esten dentro de un elemento `div`, podemos hacerlo de la siguiente manera:

```css
div p {
    ...
}
```

###  Elementos uno al lado del otro

Para seleccionar elementos que esten uno al lado del otro, tenemos que separar los selectores por un signo `+`. Por ejemplo, si queremos seleccionar todos los elementos `p` que esten uno al lado del otro, podemos hacerlo de la siguiente manera:

```css
p + p {
    ...
}
```

###  Elementos uno debajo del otro

Para seleccionar elementos que esten uno debajo del otro, tenemos que separar los selectores por un signo `~`. Por ejemplo, si queremos seleccionar todos los elementos `p` que esten uno debajo del otro, podemos hacerlo de la siguiente manera:

```css
p ~ p {
    ...
}
```

### Elementos que tengan un atributo

Para seleccionar elementos que tengan un atributo, tenemos que agregar corchetes al final del selector. Por ejemplo, si queremos seleccionar todos los elementos `input` que tengan un atributo `checked`, podemos hacerlo de la siguiente manera:

```html
<input type="checkbox" checked>
```

```css
input[checked] {
    ...
}
```

## Que son las propiedades?

Las propiedades son los estilos que queremos aplicar a los elementos. Por ejemplo, si queremos cambiar el color de texto de todos los `p`, podemos hacerlo de la siguiente manera:

```css
p {
    color: red;
}
```

## Que son los valores?

Los valores son los valores que queremos aplicar a las propiedades. Por ejemplo, si queremos cambiar el color de texto de todos los `p` a rojo, podemos hacerlo de la siguiente manera:

```css
p {
    color: red;
}
```

## Algunas propiedades y sus posibles valores

### color
> color de texto
* red
* blue
* green
* rgb(255, 0, 0)
* #ff0000
  
### background-color

> color de fondo

mismos valores que `color`

### font-size
> tamaño de texto

* 10px
* 1em
* 1rem
* 1%
* 1vw

### font-family
> tipo de letra

* Arial
* Helvetica
* sans-serif
* cursive
* fantasy

### text-align
> alineacion de texto

* left
* right
* center
* justify
* start

Cuando estas aprendiendo CSS, es muy util tener a mano una lista de propiedades y valores. Podes encontrar una lista completa [aqui](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference).

## Como se combinan los selectores?

Los selectores se pueden combinar de varias formas. Por ejemplo, si queremos seleccionar todos los elementos `p` que esten dentro de un elemento `div` y que tengan la clase `red`, podemos hacerlo de la siguiente manera:

```css
div p.red {
    ...
}
```

Si por ejemplo queremos seleccionar todos los elementos `span` que esten dentro de un elemento `div` con clase `question` y que tengan la clase `red`, podemos hacerlo de la siguiente manera:

```css
div.question span.red {
    ...
}
```


## Ejercicios

### Cambiar el color de fondo de la pagina

Para cambiar el color de fondo de la pagina, tenemos que seleccionar el elemento `body` y cambiar la propiedad `background-color`.

en el archivo `styles.css` vas a ver que ya puse algunos estilos, incluyendo una regla para body. Vas a agregar `background-color: #f5f5f5;` a esa regla. Podes cambiar el color a cualquier otro que te guste. Algunas opciones: `green` `blue` `red` `#ff0000` `#00ff00` `#0000ff` `#f5f5f5` `#ffffff` `#000000`

### Resaltar algunas palabras

En el `index.html`, en la seccion `main`, vas a agregar lo siguiente:

```html
      <p id="parrafo-danger">
        Lorem ipsum dolor sit amet <span class="danger">consectetur</span> adipisicing elit. Saepe deleniti ea incidunt labore accusamus quos <span class="danger">temporibus</span> earum perferendis esse, neque unde, minus inventore nobis necessitatibus fugit <span class="danger">maxime</span> quasi suscipit? Asperiores.
      </p>
```

En el `styles.css`, vas a agregar lo siguiente:

```css
#parrafo-danger {
    font-size: 1.5rem;
}

.danger {
    color: red;
}
```

Esto va a hacer que algunas palabras se vean en rojo.

Intenta hacer que algunas se vean en rojo, otras en verde con una clase de `success`, y otras en azul con una clase de `info`.


