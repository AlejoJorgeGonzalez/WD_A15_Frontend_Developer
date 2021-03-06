# TIPOS DE DISPLAY MÁS USADOS: BLOCK, INLINE E INLINE-BLOCK

![](../images/img41.png)

![](../images/img42.png)

![](../images/img43.png)

En htmlreference.io muestra las etiquetas que se utilizan en HTML y el tipo de display en el cual funciona, por ejemplo la etiqueta article funciona en display de bloques.

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* Se elimina el borde de la página  */
        body {
            margin: 0;
        }
        /* estilos de una etiqueta de bloque, estos ocupan
        todo el ancho de la página a menos que se le de un 
        ancho definido */
        div {
            /* Color al bloque */
            background-color: salmon;
            /* ancho del bloque */
            width: 200px;
            /* Alto del bloque */
            height: 200px;
            /* Margen del bloque */
            margin: 20px;
        }
        /* Estilos de una etiqueta inline, estos solamente 
        ocupan el espacio del contenido del texto, es de 
        anotar que en estas etiquetas no sirven las 
        propiedades de width ni height, en el caso de margin
        solo se aplica a los lados izquierdo y derecho, no 
        funciona para arriba y abajo */
        a {
            background: skyblue;
            /* No se aplica el ancho */
            width: 200px;
            /* No se aplica la altura */
            height: 200px;
            /* Aplica solamente los lados izquierda y derecha */
            margin: 20px;
        }
        /* Estilos de una etiqueta inline-block estos tienen
        las caracteristicas de inline con la posibilidad de 
        agregarles propiedades de block como el ancho y alto */
        button {
            background: slateblue;
            width: 200px;
            height: 200px;
        }

    </style>
</head>
<body>
    <!-- div es un elemento de bloque -->
    <div>bloque</div>
    <!-- a es un elemento inline -->
    <a href="/">inline</a>
    <!-- Button es un elemento inline-block -->
    <button>inline block</button>
</body>
</html>
~~~

![](../images/img44.png)