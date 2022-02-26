# TIPOS DE SELECTORES: BÁSICOS Y COMBINADORES

![](../images/img21.png)

Los selectores de Tipo solamente se coloca el nombre de la etiqueta, es de tener cuidado porque el estilo se va  aplicar a todos los div que esten en el HTML. De clase son selectores que crea la unión con el HTML por el nombre que se le haya dado. El selector ID funciona de la misma forma que el de clase pero lo prioriza mas. De atributo se une por medio de un href y por último el universal, que es el selector que aplica el estilo CSS a todo el HTML.

~~~HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <!-- La etiqueta style permite escribir en CSS dentro de un 
    archivo HTML -->
    <style>
        div{
            background: pink;
        }
    </style>
</head>
<body>
    <div>Hola</div>
    <div>Mundo</div>
</body>
</html>
~~~

Para el código se agrega solamente un selector de tipo dentro de la etiqueta style que va a aplicar a todas las etiquetas div, mostrando como resultado:

![](../images/img22.png)

Con selectores de clase primero se crea el nombre de la clase para despues copiarlo dentro de la etiqueta style

~~~html
<head>
    <style>
        div{
            background: pink;
        }
        .titulo{
          color: blueviolet;  
        }
    </style>
</head>
<body>
    <div class="titulo">Hola</div>
    <div>Mundo</div>
</body>
</html>
~~~

![](../images/img23.png)

En selectores de id se referencia por medio de un hashtag

~~~html
<head>
    <style>
        div{
            background: pink;
        }
        .titulo{
          color: blueviolet;  
        }
        #titulo2{
            color: brown;
        }
    </style>
</head>
<body>
    <div class="titulo">Hola</div>
    <div id="titulo2">Mundo</div>
</body>
~~~

![](../images/img24.png)

El selector de atributos toma en cuenta el href que se le coloca a la etiqueta ancla

~~~html
<head>
    <style>
        div{
            background: pink;
        }
        .titulo{
          color: blueviolet;  
        }
        #titulo2{
            color: brown;
        }
        a[href="https://platzi.com/home"]{
            color: blue;
        }
    </style>
</head>
<body>
    <div class="titulo">Hola</div>
    <div id="titulo2">Mundo</div>
    <a href="https://platzi.com/home">platzi</a>
</body>
~~~

![](../images/img25.png)

El selector universal aplica los estilos a todo el HTML

~~~html
<head>
    <style>
        *{
            background: papayawhip;
        }
        div{
            background: pink;
        }
        .titulo{
          color: blueviolet;  
        }
        #titulo2{
            color: brown;
        }
        a[href="https://platzi.com/home"]{
            color: blue;
        }
    </style>
</head>
<body>
    <div class="titulo">Hola</div>
    <div id="titulo2">Mundo</div>
    <a href="https://platzi.com/home">platzi</a>
</body>
~~~

![](../images/img26.png)

![](../images/img27.png)

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div p{
            color: lime;
        }
    </style>
</head>
<body>
    <div>
        <p>Platzi</p>
        <p>Es</p>
        <p>Increíble</p>
    </div>
</body>
</html>
~~~

![](../images/img28.png)

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* Descendientes */
        div p{
            color: lime;
        }
        /* Hijo Directo */
        div > div{
            background: plum;
        }
        /* Clase */
        .es {
            background: red;
        }
        /* Elemento Adyacente */
        div + section{
            background: palevioletred;
        }
        /* General de Hermanos */
        div ~ p{
            color: powderblue;
        }
    </style>
</head>
<body>
    <div>
        <div>
            <p>Platzi</p>
            <div class="es">Es</div>
        </div>
    </div>
    <div>
        Master
    </div>
    <p>Clase de Selectores</p>
    <p>Clase de Selectores</p>
    <section>
        Es lo mejor
    </section>
</body>
</html>
~~~

![](../images/img29.png)