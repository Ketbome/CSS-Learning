# CSS

## Tipos de aplicación de CSS

Idealmente no utilizarla

```html
<body style="color: red"></body>
```

Dentro del documento html

```html
<style>
  body {
    color: red;
  }
</style>
```

En un estilo aparte, en primer lugar referenciar en el html

```html
<link rel="stylesheet" href="style.css" />
```

## Selectores

Para las id se utiliza #

```css
#titulo {
  color: red;
}
```

Para las clases se utiliza el .

```css
.texto {
  color: slateblue;
}
```

Todas las etiquetas de p pero que solo tengan la clase texto

```css
p.texto {
  color: slateblue;
}
```

Siempre la ultima instrucción es la que se utilice o predomine sobre otros

### Hijos padres etc

Ahora todas las etiquetas de p que se encuentran dentro de un div

```css
div p {
  color: aquamarine;
}
```

Para varios

```css
div h2,
div h3 {
  color: brown;
}
```

### Selector universal

Este selector solo aplica a las propiedades que no han sido definidas anteriormente, en el siguiente caso se aplica el font pero no el color dado que fueron definidos anteriormente

```css
* {
  font-size: 24px;
  color: black;
}
```

## Colores

Hexagecimal

```css
.color {
  color: #0f0; // verde
  color: #00f; // Azul
  color: #f00; // Rojo
}
```

Para una mayor combinación de colores

```css
.color {
  color: #f00000; // Rojo
  color: #fe0000; // Se regula la intensidad del rojo
}
```

Para rgb se utiliza

```css
.color {
  color: rgb(0, 255, 0);
}
```

### Tipos de pintado

```css
.color {
  border: 5px red inset;
  /* 
    dotted
    dashed
    solid
    double
    3D -
      groove
      ridge
      inset
      outset
    none
    hidden
  */
}
```

## Background y color transparente

El 4to valor es el de transparencia donde 1 es el color sin opacidad y 0 siendo un 100% opaco

```css
#fondo {
  background-color: rgba(0, 0, 0, 0.3);
}
```

Se hace el agregado de una miagen y el alto con sus respectivas proporciones, tambien modificacndo sus repeticiones

```css
#fondo {
  background-color: rgba(0, 0, 0, 0.3);
  background-image: url("img.jpg");
  height: 200px;
  background-size: 200px 100px; /* contains cover */
  background-repeat: no-repeat; /* repeat-x repeat-y no-repeat */
  background-position: center bottom;
}
```

También se puede simplificar

```css
#fondo {
  background: #f00 url("img.jpg") repeat-y center bottom;
  height: 200px;
  background-size: 200px 100px;
}
```

## Margen

```css
.margen {
  background-color: chocolate;
  margin: 15px 20px 25px 30px; /* Fuera del elemento */
  padding: 20px 15px 30px 25px; /* Dentro del elemento */
  border: solid 1px black;
  height: 100px;
  width: 50px;
  overflow: scroll; /* hidden lo que esta afuera del elemento lo oculta, por defecto viene en visible, Tambien se puede poner un scroll*/
  outline: 1px solid red; /* un borde pero mas alla del border */
}
```

## Texto

```css
.text {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  text-align: justify; /* center, left, right */
  text-decoration: overline; /* Una linea arriba del texto entre otras combinaciones */
  text-shadow: 3px 5px 5px blue; /* Una copia detras de las letras, la 3ra variable es un difuminado */
}
```

## Links y estados

Si se quieren poner 2 a la vez para un mismo elemento se debe hacer tambien en el mismo orden que se muestran

```css
a:link {
  color: blueviolet;
}

a:visited {
  color: gray;
}

a:hover {
  color: yellow;
}

a:active {
  color: red;
}
```

## Listas

```css
ul {
  background-color: cyan;
  list-style-type: none;
  padding-left: 0;
  /* list-style-position: inside; */
}
```

## Tablas

```css
table {
  width: 100%;
  border-collapse: collapse;
}

th,
td {
  border: solid 1px #eee;
  padding: 5px;
}

th {
  background-color: tomato;
  color: white;
  text-align: left;
}

tr:nth-child(odd) {
  /* odd o even */
  /* Hace saltos en orden */
  background-color: #ff0;
}

tr:hover {
  background-color: #aaa; /* Si se pasa mouse por encima cambia de color el fondo */
  cursor: pointer; /* Cambio de cursor */
}
```

## Display, max width, position

Para ocultar se puede utilizar display y visibility

```css
span {
  /* display: none; */ /* Este oculta al igual que el visibility hidden */
  /* visibility: hidden; */
}
```

### Max width

max-width se adapta al ancho de la pagina

```css
span {
  display: block;
  max-width: 300px;
  background-color: #f00;
}
```

### Position

En posición normalmento todos vienen con static.
Relative cambia de posición como se necesite

```css
#position {
  position: relative;
  left: 20px;
}
```

En cambio fixed se mueve con uno

```css
#position {
  position: fixed;
  left: 20px;
}
```

Absolute se posiciona relativamente con el elemento padre que tenga

```css
#position {
  position: absolute;
  left: 20px;
}
```

sticky es una combinación entre static y fixed

```css
#position {
  position: sticky;
  left: 20px;
  top: 25px;
}
```

## Float

Posiciona un elemento tanto a izquierda como a derecha el contenido que quede lo posiciona a su lado

```css
.left {
  float: left;
  width: 200px;
}

.right {
  float: right;
}
```

## Inline block

```css
.inline-block {
  display: inline-block; /* Al ser inline block podemos darle se le puede asignar width y height */
  height: 55px;
}
```
