# TIPOS DE SELECTORES: PSEUDOCLASES Y PSEUDOELEMENTOS

![](../images/img30.png)

Las Pseudoclases permite llegar a las acciones que realiza el usuario, por ejemplo al hacer clic sobre un botón, este puede cambiar de color, de estilo con :active. Otro ejemplo es el cambio de estilos al pasar el puntero por encima de un sector por medio de :hover.

Los pseudoelementos, son los que permiten acceder a elementos que con clases y pseudoclases no se puede acceder, como por ejemplo la primera letra de un texto, agregar texto al inicio o texto al final de este.

Los pseudoclases se escriben con : mientras los pseudoelementos se escribe con ::

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <!-- Se agregan los estilos en CSS -->
    <style>
        /* Estilo inicial */
        p {
            color: salmon;
        }
        /* El pseudoelemento ::first-letter permite cambiar 
        el estilo de la primera letra */
        p::first-letter {
            color: teal;
        }
        /* El Pseudoelemento ::before permite escribir antes 
        de cualquier texto */
        p::before {
            content: "✨";
        }
        /* El Pseudoelemento ::after permite escribir despues 
        de cualquier texto */
        p::after {
            content: "😊";

        }
        /* :hover permite cambiar estilos al pasar el mouse 
        por encima */
        p:hover {
            color: skyblue;
        }
        /* primero se busca el p que este dentro de div, y 
        dentro de este con nth-child se selecciona el hijo 
        al cual se le va a realizar el cambio*/
        div p:nth-child(2) {
            color: violet;
        }
        /* ::Placeholder permite hacer cambios en la etiqueta 
        que se llama */
        ::placeholder {
            color: tomato;
        }
    </style>
</head>
<body>
    <p>Hola</p>
    <div>
        <p>Platzi</p>
        <p>Master</p>
        <p>Lo mejor</p>
    </div>
    <input type="text" placeholder="name">
</body>
</html>
~~~

![](../images/img31.png)

Enlaces Externos

[PseudoElements](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements)

[PseudoClass](https://css-tricks.com/pseudo-class-selectors/)