# TIPOS DE DISPLAY MÁS USADOS: FLEXBOX Y CSS GRID

![](../images/img45.png)

La ventaja del flexbox es que se tiene un contenedor, dentro del cuales se tienen los items que son los contenedores hijos, lo que permite que los items se puedan mostrar como filas o como columnas, alinearlos a las izquierda, a la derecha o centrado.

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* En las etiquetas que van a funcionar como 
        contenedores debe escribirse el display flex, tener
        cuidado de colocarlo en las etiquetas que van a ser
        los items*/
        .container {
            display: flex;
            background: papayawhip;
        }
        .item {
            width: 30px;
            height: 30px;
            background: purple;
        }

    </style>
</head>
<body>
    <!-- Se crea el contenedor para el flexbox -->
    <div class="container">
        <!-- Se crea los items para el flexbox -->
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
    </div>
</body>
</html>
~~~

![](../images/img46.png)

Se le agrega el justificado del contenido al container del flexbox

~~~html
.container {
    display: flex;
    background: papayawhip;
    justify-content: space-between;
}
~~~

![](../images/img47.png)
 
Para centrar los elementos dentro del container, se agrega align-items 

~~~html
<style>
        .container {
            display: flex;
            background: papayawhip;
            justify-content: center;
            align-items: center;
            height: 200px;
        }
        .item {
            width: 30px;
            height: 30px;
            background: purple;
        }
        .container .item:nth-child(2n + 1){
            background: cyan;
        }
    </style>
~~~

![](../images/img48.png)

Para convertir los items de filas a columnas, se agrega la linea de flex-direction: column
~~~html
<style>
        .container {
            display: flex;
            background: papayawhip;
            justify-content: center;
            align-items: center;
            height: 200px;
            flex-direction: column;
        }
        .item {
            width: 30px;
            height: 30px;
            background: purple;
        }
        .container .item:nth-child(2n + 1){
            background: cyan;
        }
    </style>
~~~

![](../images/img49.png)

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .container {
            /* dentro del que va a ser el contenedor se 
            agrega el display grid */
            display: grid;
            width: 400px;
            height: 400px;
            background: papayawhip;
            /* Arreglo del grid en filas y columnas en este 
            caso de 4x4 */
            grid-template-columns: 1fr 1fr 1fr 1fr;
            grid-template-rows: 1fr 1fr 1fr 1fr;
        }
        .item {
            background: pink ;
        }
        .container .item:nth-child(1){
            /* En el grid column se coloca desde que elemento 
            empieza y hasta cual termina */
            grid-column: 1 / 2;
        }
        .container .item:nth-child(2){
            grid-column: 2 / 3;
            grid-row: 2 / 3;
        }
        .container .item:nth-child(3){
            grid-column: 3 / 4;
            grid-row: 3 / 4;
        }
        .container .item:nth-child(4){
            grid-column: 4 / 5;
            grid-row: 4 / 5;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
    </div>
</body>
</html>
~~~

![](../images/img50.png)