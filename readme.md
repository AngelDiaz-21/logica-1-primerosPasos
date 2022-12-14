# Lógica de programación parte 1: Primeros pasos

Para este curso se utilizó el lenguaje de programación JavaScript para comprender el uso de variables, para realizar ciertas funciones, operaciones que JavaScript puede realizar de manera dinámica y también con HTML para poder mostrar ciertos mensajes o el resultado de las operaciones.

## Descripción de los ejercicios realizados

**01-empezandoJS.html**

![Archivo 01-empezandoJS.html](./image/archivo-empezando-js.png "Archivo 01-empezandoJS.html")

En este primer archivo se vieron bastantes cosas, tales como diferencia el código HTML con JavaScript, la creación de funciones con y sin parámetros, llamar una función dentro de otra función, entre otras cosas.

Para empezar, para hacer uso de HTML se debe de hacer uso de etiquetas, por ejemplo, en el archivo se presenta lo siguiente:
```
<h1>Lógica de programación</h1>
<br>
Aquí puedes consultar mucha información <a href="google.com">Google</a>
```

Que es código HTML, lo que se puede visualizar al abrir el navegador y es estático. En cambio, todo lo de JavaScript esta encerrado por la siguiente etiqueta:
```
<script> </script>
```

Como se mencionó anteriorment, JavaScript nos permité realizar diferentes cosas, por ejemplo, declarar variables:
```
let age = 2022;
```

Otra de las cosas que se vio fue el como usar código HTML dentro de JavaScript, esto se consigue con la siguiente sintaxis:
```
document.write("etiqueta")
```

***Nota impotante: El sitio MDN Web Docs (que es una plataforma de aprendizaje para las tecnologías web) recomienda no utilizar este método, sin embargo, para este parte se utilizará en forma de aprendizaje y que no afecta.***

En el archivo se utilizó más para imprimir mensajes y hacer uso de la etiqueta `<br>` para hacer saltos de líneas, e incluso se creo una función denominada "saltarLinea" para este fin, como se muestra a continuación:
```
function saltarlinea(){
    document.write("<br><br><br>");
}
```

Así mismo se implemento otra función con el fin que fuera más fácil de mostrar los mensajes en el HTML, la función que se creo se denomina "imprimir":
```
function imprimir (mensaje){
    document.write(mensaje)
    saltarlinea();
}
```

Otra de las cosas más importantes es que dentro de las funciones se pueden llamar otras funciones, solo es cuestión de poner el nombre de la función y los paréntesis.

También se vio que puede haber concatenación de strings así como una concatenación de un string y un número ya que en automático JS lo hace. Si en dado caso queremos realizar una operación debemos de verificar que todos sean de tipo de number para que se pueda realizar.

Por último, en este ejercicio se vio la utilidad de usar variables y de la misma forma, podemos realizar operaciones usando variables y una de sus ventajas es que si en algún momento se optá por cambiar el contenido de la variable es que se realiza desde un solo lugar al contrario que haríamos sino usáramos variables. Un claro ejemplo es con una tabla de multiplicación, como se muestra en el código, se realiza la tabla del 8, pero si en dado caso quisiéramos saber la tabla de otro número solo bastaría con cambiar el contenido de la variable "numberMultiplicar".

**02-calculo_consumo.html**

Requerimientos:

1. Si un carro tiene un tanque de 40 litros. Usando gasolina y consumiendo todo el tanque se hace un recorrido de 480 kilómetros. ¿Cuál es la eficiencia del carro usando gasolina? o sea, ¿cuántos kilómetros recorre el carro por cada litro de gasolina? Para calcular la eficiencia: divide la distancia recorrida entre la cantidad de litros gastados. Imprime el valor utilizando document.write. Organiza las cuentas en variables.

2. Por otro lado, si el carro usa alcohol como combustible, el mismo tanque de 40 litros hace un recorrido de 300 kilómetros. ¿Cuál es el la eficiencia del carro usando alcohol?

![Archivo 02-calculo_consumo.html](./image/archivo-calculo-consumo.png "Archivo 02-calculo_consumo.html")

Descripción del programa:

Este progama está más enfocado en el uso de variables y poder realizar las operaciones que se necesitan.

Se crean las variables requeridas que sería el tanque del carro, la distancia usando gasolina y la distancia usando gasolina, las cuáles se denominan:
```
let carroTanque       = 40;
let distanciaGasolina = 480;
let distanciaAlcohol  = 300;
```

Para saber el consumo de gasolina solo se divide 480 sobre 40 y para saber el consumo de alcohol se divide 300 entre sobre 40. Usando las variables quedaría de la siguiente manera:
```
let consumoGasolina = distanciaGasolina / carroTanque;
let consumoAlcohol = distanciaAlcohol / carroTanque;
```

Por último, para mostrar un breve mensaje y los resultados en el HTML se hace uso del método `document.write`.

**03-diferenciaEdad.html**

Requerimiento:

¿Cuántos años de diferencia tienes con tu hermano? Escribe un programa que muestre el mensaje ¨Nuestra diferencia de edad es¨, concatenando el resultado de la diferencia de tu edad con la de tu hermano (o de un amigo). La respuesta puede dar negativa, sin duda. No olvides de usar las funciones saltarLinea e imprimir.

![Archivo 03-diferenciaEdad.html](./image/archivo-diferenciaEdad.png "Archivo 03-diferenciaEdad.html")

Descripción del programa:

Primero reutilizamos las funciones saltarLinea y imprimir que se crearon en el primer archivo. La función saltarLinea consiste en generar un salto de línea y mientras la función imprimir recibe un parámetro "resultado", dentro se hace uso del método "document.write" y se utiliza el parámetro recibido para que se pueda mostrar en el HTML.

Después se crean  variables, la primera variable denominada "miEdad", que en este caso contendrá un número, después otra variable llamada edadHermano y por último la variable diferenciaEdad al cuál se le asignará el resultado de la operación.

Por último, se hace uso de la función imprimir para mostrar en el HTML un mensaje y el resultado.

**04-imc.html**

![Archivo 04-imc.html](./image/archivo-imc.png "Archivo 04-imc.html")

Descripción del programa:

Este programa tiene como objetivo calcular el indice de masa corporal (IMC). Para el desarrollo se reutilizo la función saltarLinea e imprimir y se realizó una función nueva llamada calcularImc, como su nombre lo indica nos ayudará a calcular el IMC, la función recibe 2 parámetros: peso y altura.
Adentro de la función se crea la variable "imc" a la cuál se le asigna el resultado de la operación "peso / (altura * altura)" y por último se hace uso de la palabra reservada "return" para devolver el resultado, es decir, para que se pueda utilizar.

Se crean las variables "miPeso", "miAltura" e "imc", en la útima variable se manda a llamar a la función calcularImc y se envían como parámetros las variables anteriormente creadas.

Luego se hace uso de la función imprimir para mostrar el resultado en el HTML.

Sin embargo, otra forma de hacer el programa más interactivo es permitir que el usuario pueda ingresar sus datos como su nombre, peso y altura. Así que para esto se utilizó el método prompt que nos permitirá ingresar datos y guardarlos en sus respectivas variables "name", "pesoInforfmado" y "alturaInformado". Después, nuevamente se hace uso de la función calcularImc para obtener el resultado.

Por último, podemos hacer uso de la condicional if, que dependiendo del resultado del IMC podremos envíar un mensaje, es decir, si su IMC es menor a 18.5 podremos mostrar el siguiente mensaje "IMC abajo de lo recomendado", si el IMC es mayor o igual a 18.5 y si el IMC es menor a 25 se mostrará "IMC está adentro del intervalo recomendado" y si el IMC es mayor o igual 25 se mostrará "IMC considerado como sobrepeso".

## ¿Que se aprendió a lo largo de este curso?
* Conceptos básicos de HTML: Lenguaje de etiquetas.
* Diferenciar HTML de JavaScript.
* Concatenar caracteres (strings).
* Operaciones conjuntas entres textos y números.
* Usar variables para reducir código.
* Diferentes tipos de datos en las variables y fórmulas.
* Crear funciones y usar funciones con parámetros.
* Produndizar en el retorno de funciones.
* Conocer un poco del condicional if.