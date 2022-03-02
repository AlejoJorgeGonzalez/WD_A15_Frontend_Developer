# CASCADA Y ESPECIFICIDAD EN CSS

![](../images/img32.png)

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=s, initial-scale=1.0">
    <title>Document</title>
    <!-- Estilos en CSS -->
    <style>
        h1 {
            color:red;  
        }
        h1 {
            color:blue;  
        }
        /* En el método de cascada el orden en que se colocan 
        las instrucciones importan, como por ejemplo con
        estas dos instrucciones, primero se coloca la letra
        de color rojo pero despues pasa a ser azul, que por 
        ser la ultima instrucción queda de este color */
    </style>
</head>
<body>
    <h1>Platzi</h1>
</body>
</html>
~~~

![](../images/img33.png)

![](../images/img34.png)
![](../images/img35.png)
![](../images/img36.png)
![](../images/img37.png)
![](../images/img38.png)
![](../images/img39.png)

Se escribe el siguiente código

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* se llama un id con # */
        #platzi {
            color: red;
        }
        /* Se llama la clase con . */
        .master{
            color: springgreen;
        }
    </style>
</head>
<body>
    <!-- Etiqueta que contiene tanto id como clase -->
    <div id="platzi" class="master">Platzi</div>
</body>
</html>
~~~

![](../images/img40.png)

Por especificidad un id va a ser mas importante que una clase, por tanto aparece la letra en color rojo

## Enlaces Externos

[Calculadora de Especificidad](https://specificity.keegan.st/)

[Colores en Html](https://htmlcolorcodes.com/)