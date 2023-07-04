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
