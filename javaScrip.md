# JavaScriptFreeCodeCamp

curso de freeCodeCamp aprender JavaScript

- JavaScript no se instala en el equipo, este se intala en el browser. Una alternativa para ejecutarlo es usar **Visual Studio code**.

- Para esto se crea una archivo **index.html** y se agrega,

```
<script>
  consola.log("Hola mundo!");
</script>
```

- Los tipos de datos son.

  - undefined: indefinido cuando no esta asibnado el valor.
  - null: objeto que no existe.
  - boolean: Boleano.
  - string: caracteres.
  - symbol: no lo usaremos.
  - number: para números.
  - object: Para representar objetos, son estructuras que nos permitiran definir caracteristicas y comportamientos según ese objeto..

- Para nombrar las variables se recomienda usar la convención camelCase.

- Hay tres artecnativas para declarar variables, las cuales son **let**, **const** y **var**, cada una tiene sus diferencias y las veremos luegio.

```
var a = 5; /* Se asigna el valor 5 a **a** */
var b = a; /* Se asigna a **b** el valore de **a** */
b=a /* Asi es otra forma*/
```

- Declarar una variable es simplemente crear el nombre de la variable, inicializarla es asignarle un valor.

```
var b; /* Se inicializa  **b** */
var a = 5; /* Se asigna el valor 5 a **a** */
var moIdioma; /* Se usa la nomenclatura camelCase */
```

- Al declarar una variable podemos definir el tipo de dato que tendran estas variables.

- Java Script es sencible a mayúsculas y minúsculas. Esto en igles se denomina **case-Sencitive**

### Operaciones aritmeticas.

- Importantes:
  - El resto se obtiene con el operador **%**
  - Para incrementar el valor de una variable en una unidad usamos.
    1. x = x + 1;
    2. x++;
  - Para incrementar una cantidad cualquiera o actualizar su valor usamos.
    - x = x+y
  - Para reducir el valor es analogo pero usamos en la segunda opción los simbolos **x--**
  - Para aumentar o reducir el valor de una variable en cualquier cantidad podemos usar.
    - x += cantidad;
    - x -= cantidad;
  - Escribir de forma analoga la multiplicación y la división.
    - x \*= y;
    - x /= y;

### Operaciones aritmeticas.

- Importantes:

  - Hay caracteres especiales causan problemas al momento de escribirlo, para esto necesitamos caracteres de escape. Por ejemplo tenemos.

    - La barra invertida. "Soy una \"cadena de caracteres con comillas\" "
    - Para que sea mas facil de leer podemos usar comillas simple para declarar la variables y asi podemos usar las otras comillas sin el caracter de escape y viceversa.
      - "Soy una 'cadena de caracteres con comillas' "
      - 'Soy una "cadena de caracteres con comillas" '
    - Secuencia de escape.

      | Código | Resultado        |
      | ------ | ---------------- |
      | \ \'   | comilla simple   |
      | \ \"   | comilla Doble    |
      | \ \\   | Varra invertida  |
      | \ \n   | Nueva linea      |
      | \ \r   | Retorno de Carro |
      | \ \t   | Tabulacion       |
      | \ \b   | Retroceso        |
      | \ \f   | Salto de Página  |

  - Concatenar.
    - Se usa el operador de suma **+**.
  - Longitud.
    - Para saber la longitud de una cadea uamos la propiedad **length**.
  - Subcadena o notacion de corchetes.

    - Cada caracter de una cadena tiene una posición y se comienza a contar desde cero.

    Por ejemplo. miCadena[0]. Obtenemos el primer carater.

  - Las cadenas son inmutables, no podemos cambiar un caracter de la cadena, tendremos que reasipnar el valor de la cadena completamene.

### Arreglos.

- Los arreglos son estructuras de datos que nos permiten almacenar multiples valores.

  ```
  var miArreglo = ["Jonh", 28];
  /*Arreglos anidados*/
  var miOtroArreglo = [["a", "b", "c"], [1, 2, 3]]
  ```

- ¿Como acceder a los arrglos?
  Los arreglos se ordenan con indices comenzando desde el cero y podemos acceder a ellos usando la notación de corchetes.

  ```
  var miOtroArreglo = [["a", "b", "c"], [1, 2, 3]]
  miOtroArreglo[0]
  ```

- Modificar datos de un arreglo.

  ```
  var miOtroArreglo = [["a", "b", "c"], [1, 2, 3]]
  miOtroArreglo[0] = "aa"
  ```

- Acceder a arreglos multidimencionales

  ```
  var miOtroArreglo = [["a", "b", "c"], [1, 2, 3]]
  console.log(miOtroArreglo[0][1])
  ```

- Agregar elementos a un arreglo.

  Usamos el metodo **push** para agregar un elemento al final del arreglo.

  ```
  var agregarAlAreglo = [["a", "b", "c"], [1, 2, 3]]
  agregarAlAreglo.push(["alpha", "Beta", "Gamma"])
  console.log(agregarAlAreglo)
  ```

- Remover ultimo elemento de un arreglo, usamos el metodo **pop**, este metodo elimina el ultimo elemento del arreglo y tembien lo retorna.

  ```
  var quitarAlAreglo = [["a", "b", "c"], [1, 2, 3]]
  console.log(quitarAlAreglo)
  var seElimino;
  seElimino = quitarAlAreglo.pop()
  console.log(quitarAlAreglo)
  console.log(seElimino)
  ```

- Remover primer elemento de un arreglo, usamos el metodo **shift**, este metodo elimina el primer elemento del arreglo y tembien lo retorna.

  ```
  var quitarPrimerAreglo = [["a", "b", "c"], [1, 2, 3]]
  console.log(quitarPrimerAreglo)
  var seElimino;
  seElimino = quitarPrimerAreglo.shift()
  console.log(quitarPrimerAreglo)
  console.log(seElimino)
  ```

- Agregar elemento al principio del arreglo. Para esto usamos el metodo **unshift**

  ```
  var agregarPrincipioArregle = [["a", "b", "c"], [1, 2, 3]]
  console.log(agregarPrincipioArregle)
  agregarPrincipioArregle.unshift(["Gamma", "Beta", "Alfa"])
  console.log(agregarPrincipioArregle)
  ```

### Funciones.

- Como crear funciones.

  Las funciones se definen de la siguiente forma:

  ```
  function mostrarMensaje(){

  }
  ```

  Las funciones pueden retornar valores y recibir argumentos. Veamos como se asignan argumentos y como retornan valores.

  ```
  function sumar(a, b){ /*a y b son parametros de entrada*/
    var suma = a + b;
    console.log("El resultado de "+ "a" + " + " "b" + " es: " + suma)
  }
  ```

  ```
  function sumar(a, b){ /*a y b son parametros de entrada*/
    return a + b; /*Valor que se retornara*/
  }
  ```

  El valor retornado se puede asignar a una variable o se puede usar de forma directa para usar de las forma que sea posible.

  Las funciones pueden no retornar un valor, en este caso retornara un valor por defecto el cual sera undefined.

- Ambito global.

  Hay dos tipos de variables, **Globales** y **Locales**

  - Las variables **globales** son las que estan definidas de forma que se puede acceder a ellas desde cuarquier parte de algoritmo, estan definidas en el entorno global del algoritmo.

  - Las variables **locales** se definen de forma local, en una función por ejemplo, estas variables solo se pueden usar o acceder desde el entorno local donde se creo.

  - Si se tienen dos variables con el mismo nobre, pero una **local** y otra **global**, al llamar a la variable en el entorno local, la variable **local** tiene prioridad y si se llama a la variable fuera del entorno **local** se le da prioridad a la variable **global**.

### Operadores Lógicos.

- Operador **==**.

  Este operador compara si dos elementos son iguales y retorna **true** o **false** según sea el caso.

  **Nota** Con este operador no se deben comparar arreglos ya que en este caso compara si estos tienen el mismo valor en memoria y no como elemento.

  Si comparamos un **número** y un **string** esto puede dar problemas por que en caso de comparar \n **9 == "9"** el resultado sera **true** esto es por convertira los datos a un tipo común, para ser mas estricto y evitar que se convierta a un tipo de dato común se debe usar la igualdad estricta **===**.

- Operador de desigualdad. **!=**

Tambien tenemos el mismo comportamiento que el caso con la igualdad en torno a la comparación **1 != "1"**, así usamos el operador de desigualdad estricta **!==**

**Nota** con los arreglos sucede analogo al caso del uso de **==**

- Operadores relativos.

  - **>**
  - **<**
  - **<=**
  - **>=**

  - Las cadenas son comparadas según su orden alfabetico. Si una tiene más caracteres que otra la mayor sera la que tiene mas caracteres.

- Operadores lógicos.

  Los operados lógicos se escriben de la siguiente forma.

  - El **Y (and)** lógico es **&&**
  - El **O (or)** lógico es **||**
  - El **Not (negado)** lógico es **!**

### Condicionales.

- El condicional **si**, se escribe como **if**.

  ```
  if (condicion){

  }
  ```

  tenemos formas anidadas del **if** las cuales se escriben

  ```
  if (condicion){

  } else {

  }
  ```

  ```
  if (condicion){

  }else if (condicion){

  }else if (condicion){

  }...{

  }else{

  }

  ```

- El clasificador **Switch**
  Este condicional su usa de la siguiente forma.

  ```
    switch (valor){
      case <comparador1>:
        codigo;
        break;
      case <comparador2>:
       codigo;
        break;
      ...
      case <comparadorn>:
       codigo;
        break;

    }
  ```

  Hay una opción predeterminada en caso de que el valor de la condición no sea igual a ninguno de los valores de la comparación.

  ```
    switch (valor){
      case <comparador1>:
        codigo;
        break;
      case <comparador2>:
       codigo;
        break;
      ...
      case <comparadorn>:
       codigo;
        break;

      default: /* es la opción por defecto*/
        codigo;
        break;
    }
  ```

  Hay otra variación y ejecutar un codigo especifico para varios valores.

  ```
    switch (valor){
      case <comparador1>:
        codigo;
        break;
      case <comparador2>: /*Se colocan los casos segiodos*/
      case <comparador3>: /*luego va el codigo*/
       codigo;
        break;
      ...                 /*Se puede repetir cuantas
                            veces necesario*/
      case <comparadorn>:
       codigo;
        break;

      default: /* es la opción por defecto*/
        codigo;
        break;
    }
  ```

### Retornar valores booleanos de forma concisa.

    ~~~
     function esMenorQue(a, b){
        return a < b;
      }
    ~~~

### Patron de retorno anticipado.

Podemos retornar un valor en una función antes de otras lineas de codigo, por ejemplo si cumple cierta condición y asi no se ejecuta o se consulta el resto del codigo.

    ~~~
    function calcularRaizCuadrada(num){
      if (num < 0){
       return undefined;
      }
      return Math.sqrt(num);
    }
    ~~~

### Creación de objetos.


- Un objetos nos permite guardar una secuencia o propiedades que son propias de nuestro obejo, un carro, una casa o cualquier otro abstracto.

  Se declaran de la siguiente forma.

  ```
    var miPerro = {
     "nombre": "Gino",
     "edad" : 5,
     "peso": 6,
      "raza": "Beagle"
    };
  ```

   ```
    var miPerro = {
      1:{
        p1: "p1",
        p2: "p2",
        p3: "p3"
      },
      2:{
        p1: "p1",
        p2: "p2",
        p3: "p3"
      }
    };
  ```

- Al valor de la izquierda se le llama propiedad del objeto y al de  la derecha el valor que tiene esta propiedad. Para acceder a la propiedad del objeto usamos la siguiente notación.

  ```
    miPerro.peso;
    miPerro.edad;
   ...
  ```

- Alternativamente podemos usar la notación de corchetes.

  ```
    miPerro["peso"];
    miPerro["edad"];
    ...
  ```

- Podemos actualizar propiedades de un objeto.

  ```
    var miObjeto = {
     "nombre": "Gino",
     "edad" : 5,
      "peso": 6,
      "raza": "Beagle"
    };

    /*Actualizamos una propiedad.*/
    miObjeto.peso = 8; Actualiza de **6** a **8**
  ```

- Podemos agregar nuevas propiedades a un objeto en javaScript.

  ```
    var miObjeto = {
      "nombre": "Gino",
      "edad" : 5,
      "peso": 6,
     "raza": "Beagle"
   };

    /*Actualizamos una propiedad.*/
   miObjeto.peso = 8; Actualiza de **6** a **8**
  ```
- Podemos también agregar una nueva propiedad a nuestro objeto.
  
  ~~~
    var miObjeto = {
      "nombre": "Gino",
      "edad" : 5,
      "peso": 6,
     "raza": "Beagle"
    };
    miObjeto.estatura = 65;
  ~~~

- Podemos también eliminar una propiedad a nuestro objeto.
  
  ~~~
    var miObjeto = {
      "nombre": "Gino",
      "edad" : 5,
      "peso": 6,
     "raza": "Beagle"
    };
    delete miObjeto.estatura;
  ~~~

### Usar objetos para busqueda.

  ~~~
  function buscarElementoQuimico(simbolo){
    var simbolosQuimicos = {
      "Al"  : "Aluminio",
      "S"   : "Azufre",
      "Cl"  : "Cloro",
      "He"  : "Helio",
      "B"   : "Boro",
      "Li"  : "Litio",
    };
    return simbolosQuimicos[simbolo];
  };
  ~~~

### Verificar propiedades.
  Podemos verificar si un objeto tiene o no una propiedad, para esto usamos el metodo hasOwnProperty();.
  ~~~
  var simbolosQuimicos = {
    "Al"  : "Aluminio",
    "S"   : "Azufre",
    "Cl"  : "Cloro",
    "He"  : "Helio",
    "B"   : "Boro",
    "Li"  : "Litio",
  };
  
  simbolosQuimicos.hasOwnProperty("Cl");
  simbolosQuimicos.hasOwnProperty("Na");

  function verificarPropiedad(obj, propiedad){
    if (obj.hasOwnProperty(propiedad)){
      return "Propiedad: " + obj[propiedad];
    } else {
      return "El objeto no tiene esta propiedad"
    }
  }  
~~~

### Objetos complejos.
  ~~~
    var ordenesDePizzas = [
      {
        "tipo": "margarita",
        "tamaño": "individual",
        "precio": 5.67,
        "toppings":[
          "extra queso",
          "champiñones",
          "piña"
        ]
        "paraLlevar": true
      },
      {
        "tipo": "cuatro quesos",
        "tamano": "familiar",
        "precio": 18.34,
        "toppings":[
          "extra queso",
          "pimenton"
        ]
        "paraLlevar": false
      }
    ];
  ~~~

  - Accedemos de forma analoga a como lo haciamos con arreglos.
  ~~~
    ordenesDePizzas[0]
    ordenesDePizzas[1]
    /*Para acceder a cada tipo en cada objeto accedemos igual que en los objetos.*/
    ordenesDePizzas[0].tipo
    ordenesDePizzas[1].tamano
  ~~~

  - Objetos anidados.

  ~~~
    var miReceta = {
      "descripcion": "mi postre favorito",
      "costo": 15.6,
      "ingredientes": {
        "masa": {
          "harina" : "100 grs",
          "sal": "1 cucharadita",
          "agua": "1 taza"
        },
        "cobertura": {
          "azucar": "120 grs",
          "chocolate": "4 cucharadas",
          "mantequilla": "200 grs"
        }
      }
    };
  ~~~

  ¿Como accedemos a sus elementos?

  ~~~
    miReceta.descripcion;
    miReceta.cobertura.chocolate
    masaMiReceta = miReceta.masa
    masaMiReceta.harina
    masaMiReceta.sal
    masaMiReceta.agua
    /*Tambien podemos usar la notación de corchetes*/
  ~~~

### Arreglos anidados.

  ~~~
    var misPlantas = [
      {
        tipo : "flores",
        lista : [
          "rosas", 
          "tulipanes",
          "dientes de leon"
        ]
      },
      {
        tipo : "árboles",
        lista : [
          "abeto",
          "pino",
          "abedul"
        ]
      }
    ];
  ~~~   
  ¿Como accedemos?
  ~~~
    misPlantas[0].lista[0];
    misPlantas[1].lista[2];
  ~~~

### Ciclos o bucles (Loop).

  - Ciclo while.

    Se usa cuando no tenemos un numero especifico de iteraciones.

    ~~~
      while (i <= 3) { 
        console.log("Hola, mundo");
        i++
      }
      /*Cuando la condición es verdadera sigue ejecutando el ciclo, cuando es falsa se detiene.*/
    ~~~

    ~~~
      var miArreglo = [];
      var i = 0;

      while (i < 10) { 
        miArreglo.push(i);
        i++
      }
      /*Cuando la condición es verdadera sigue ejecutando el ciclo, cuando es falsa se detiene.*/

      console.log(miArreglo);
    ~~~

  - Ciclo while.      

    Se usa cuando tenemos un numero especifico de iteraciones.

    ~~~
      var miArreglo = [];

      for (var i = 0; i < 10; i++){
        miArreglo.push(i);
      }
      console.log(miArreglo)
    ~~~

    Ejemplos de **for** anidados.

    ~~~
      var miArreglo = [[1,2,3], [4,5,6],[7,8,9]];

      for (var i = 0; i < miArreglo.length; i++){
        var arregloAnidado = miArrego[i];
        for (var j = 0; j < arregloAnidado.length; j++){
          console.log(arregloAnidado[j])
        }
        
      }
    ~~~

### Ciclo do While (Hacer mientras).
  A diferenvia del **While** el **doWahile** ejecuta el codigo primero y luego evalua la sentencia.
  ~~~
    do {
      console.log(x);
      x++;
    } while (x < 10);
  ~~~

### Numeros aleatorios.

  Usamos la librería **Math**

  ~~~
    function generarNumerosAleatorios(){
      return Math.random();
    }
  ~~~

  - Para números aletrios enteros usamos **floor()**
  ~~~
    Math.floor(Math.random()*20); 
    /*obtenemos entero entre 0-20*/
  ~~~

  - Podemos generar numeros aleatorios en un rango inferior y superior.

  ~~~
    function rangoAleatorio(lInf, lSup){
      return Math.floor(Math.random()*(lSup - lInf + 1)) + lInf;
    }
  ~~~

### Conversión de tipos.

  - Cadenas a number.
    - De **string numerico** a **entero** usamos la función **parseInt("-5")**
    - De **decimal** a **entero** usamos la función **parseInt("83.15")**
    - Si convertimos un **string no numerico** nos da **NAN**
    - **string** en otro sistema numerico, por ejemplo, comberción de binario a **entero**. **parseInt("110111", 2)** lo convierte a su equivalente en **entero**.
    - **binario** a **entero**, **parseInt(110111, 2)**.
    - **hexadecimal** a **decimal**, solo se puieden representar como cadenas estos numeros. **parseInt("3E0A", 16)**.

### Operador condiccional ternario.

  - Nos permite compactar un condicional en una linea.

    ~~~
      return x < y ? x : y;
      /*si x < y es true return x si no return  y */
      x < y ? x : y;
    ~~~
  
  - Multiples operadores ternarios.

    ~~~
      function compararNumeros(a, b){
        return x == y ? "a y b son iguales" 
            : x > b ? "a es mayor que b"
            : "b es mayor que a";
      }
    ~~~

### var vs let.

 - Cuando declaramos una variable con **var**, la podemos declarar mas de una vez, cuando usamos **let** no podemos declarar la variable mas de una ves.

 - Ambito de **let** y **var**.
  
  - Con **var** podemos usar la variable global en cualquier parte del programa y podemos definir variables dentro de una función solo que no las podremos usar fuera de la función.

  - Cuando usamos **let** para declarar una variable, su ambito esta restringido al bloque donde se define. Por ejemplo si usamos un iterador **i** de un ciclo, este iterador si lo declaramos con let, no lo podremos llamar fuera del ciclo, pero con **var** si se puede.

  - Si tenemos un bloque de codigo **if** y declaramos una variable con **let**, no podremos acceder a esta variable fuera de ese bloque de codigo.

### Opcion const.

  - Si se declara una variable con **const** no podremos modificar el valor de esa variable una ves que sea declarada, ademas esta al momento de ser declarada se le debe asignar su valor, estas variables se declaran con letras mayusculas y se separan las palabras con giones bajos.

  ~~~
    const PI = 3.14;
  ~~~

  - Cuando se declara una variable con **const**, no podemos resignar otro valor nuevo a esa variable, pero si podemos cambiar su valor. Por ejemplo un arreglo.

  ~~~
    const Mi_ARREGLO = [9, 8, 7, 6];
    Mi_ARREGLO[0] = 1;
    Mi_ARREGLO[1] = 2;
    Mi_ARREGLO[2] = 3;
    Mi_ARREGLO[3] = 4;
  ~~~

  - ¿Como crear un objeto inmutable?

    Ejemplo.
    ~~~
      let colores = {
        "verde" : "#10e04b"
        "azul" : "1b50e0"
        "negro" : "#000000"
        "blanco" : "#ffffff"
      }
      object.freeze(colores) /*congela al objeto en ese estado*/
    ~~~

### Funciones flecha.

  - Son un tipo mas compacto de funciones, se usa mas que todo cuando queremos crear funciones anonimas.

    ~~~
      const fecha = () => new Date();
      /*Esta función retorna un objeto del tipo Date*/
    ~~~

  - Agregar parametros a funciones flecha.
    ~~~
      const sumarTres = (x) => x +3;

      const concatenarArreglos = (arr1, arr2) => arr1.concat(arr2);
    ~~~
  
  - **Si la función tiene mas de una linea tenemos que mantener las llaves.**

    ~~~
     const sumar = (a, b) => {
      let num = 6;
      return a + b + num;
     };
     console.log(sumar(1, 1)) 
    ~~~

### Valores por defecto para parametros para cualquier función. 

  - Esto es util cuando queremos permitir que se onita un parametro.

    ~~~
      const incrementar = (num, valor = 1) => num + valor;
      console.log(incrementar(5))
      console.log(incrementar(5, 3))
    ~~~

### Operador rest.

  - Este operador permite pasar cualquier número de argumentos a una función y estos se agrupen en un arreglo. Consiste en escribir tres puntos y la palabra args **(...args)**

  ~~~
    function miFuncion(...args){
      console.log(args)
    }
  ~~~
  **Ejemplo**
  ~~~
    const sumar = (...args) => {
      return args.reduce((a, b) => a + b, 0 );
      /*reduce con estos argumentos, suma los elementos del arreglo y retorna el resultado.
      Pasamos una función flecha como argumento.*/

    }
  ~~~
  
### Operador spret.

  - Hace lo contrario que rest. Recibe como parametro un arreglo y los desglosa en orden asignando a cada parametro su valor.

  ~~~
    const numeros = [1,2,3]
    function sumar(x, y, z){
      return x + y + z;
    }
    console.log(sumar(...numeros))
  ~~~

### Sintaxis de desestructuración.
  
  - Nos permite asignar las propiedades de un objeto a variables.

  ~~~
    const usuario = {
      nombre: "Gino Smith",
      edad: 34
    }
    const {nombre, edad} = usuario;
    
    var coordenadas = {
      x:4,
      y:6,
      z:12
    };

    var {x, y, z} = coordenadas;
  ~~~

  - Forma mas elevorada por ejemplo si tenemos objetos anidados.

   ~~~
    const usuario = {
      johnDoe: {
        edad:27,
        correo: "johnDoe@freecodecamp.com"
      }
    };
    
    const {johnDoe:{edad, correo}} = usuario;
    /*Para asignar un nombre nuevo usamos*/
    const {johnDoe:{edad:edadDelUsuario, correo:correoDelUsuario}} = usuario;
  ~~~

### Sintaxis de desestructuración Arreglos.
  
  - Nos permite asignar los valores de un arreglo a variables.

  ~~~
    var a;
    var b;
    var c;
    [a, b, c] = [1,2,3,4,5,6] /*Se asignan los dos primeros*/
    [a,b, , ,c] = [1,2,3,4,5,6] /*Se asignan los dos primeros y el quinto elemento en el indice 4*/
  ~~~

  - Intercambiar valores.

  ~~~
    var a = 8;
    var b = 6;
    [b, a] = [a, b];
  ~~~

### Sintaxis de desestructuración con el operador rest.

  ~~~
    var a;
    var b;
    var arr;
    [a, b, ... arr] = [1,2, 3, 4, 5, 6, 7];
    /*A la variable arr se le asigna el arrego [3,4,5,6,7]*/
  ~~~

  ~~~
    const arregloInicial = [1, 2, 3, 4, 5, 6, 7, 8];
    function removerTresPrimerosElementos(arreglo){
      var nuevoArreglo;
      const [ , , ,...neuvoArreglo] = arreglo;
      return nuevoArreglo;
    }
    const arregloFinal = removerTresPrimerosElementos(arregloInicial);
    console.log(arregloFinal);
  ~~~

### sintaxis de Desestructuración: Pasar Objeto como Argumento.

  ~~~
    var nuevoPerfilCliente = {
      nombre: "Jane Doe",
      edad: 24,
      nacionalidad: "española",
      ubicacion: "España"
    };
    const actualizarPerfil = ({nombre, edad, nacionalidad, ubicacion}) => {
      console.log(nombre);
      console.log(edad);
      console.log(nacionalidad);
      console.log(ubicacion);
    };
    actulizarPerfil(nuevoPerfilCliente);

    const estadisticas = {
      max: 56.78,
      desviacionEstandar: 4.34,
      mediana: 34.54,
      moda: 23.87,
      min: -0.75,
      promedio: 35.85
    };
    // const puntoMedio = (estadistica) => (e.max + e.min)/2.0;
    const mitad = ({max, min}) => (max + min)/2.0;
    console.log(mitad(estadisticas));
  ~~~


### Plantillas literales o plantillas de cadenas.

  - Características:
    - Se usa el acento invertido (backtick) ` en lugar de comillas.
    - Pueden contener comillas simples y dobles.
    - Las líneas se preservan como se escriben en el código.
    - Para reemplazar una variable se escribe ${variable}.
    - Dentro de ${} también puedes escribir expresiones.


    ~~~
      var a = 6;
      console.log(`El valor de a es ${a}.`);

      var nombre  = "Nora";
      var edad = 6;
      console.log(`Mi nombre es ${nombre} y tengo ${edad} años.`);

      var miArreglo = [1, 2, 3, 4];
      console.log(`El arreglo es: ${JSON.stringify(miArreglo)}`);

      // Ejemplo con objeto

      const persona = {
        nombre: "Gino Cass",
        edad: 10
      };
  
      const saludo = `¡Hola! Mi nombre es ${persona.nombre} 
      y tengo ${persona.edad} años.`;
  
      console.log(saludo);
    ~~~

### Crear objetos de forma concisa.

  ~~~
    // Inicialmente

    const crearPersona = (nombre, edad, idioma) => {
      return {
        nombre: nombre,
        edad: edad,
        idioma: idioma
      };
    };

    console.log(crearPersona("Gino Smith", 28, "Español"));

    // Alternativa más concisa

    const crearPersona = (nombre, edad, idioma) => ({nombre, edad, idioma});

    console.log(crearPersona("Gino Smith", 28, "Español"));   
  ~~~
  
### Metodos en Java Script.


  - Podemos declarar funciones dentro de los objetos que se crean en los programas.


  ~~~
    // Versión ES5

    const persona = {
      nombre: "Isabel",
      presentarse: function() {
        return `¡Hola! Mi nombre es ${this.nombre}.`;
        /* this se refiere al objeto con el que se esta trabajando, en este caso al 
        objeto persona */
      }
    };

    console.log(persona.presentarse()); /*Se denomina metodo si el valor de la propiedad 
    es una función como presentarse()*/

    // Versión ES6

    const persona = {
      nombre: "Isabel",
      presentarse() {
        return `¡Hola! Mi nombre es ${this.nombre}.`;
      }
    };

    persona.presentarse();
~~~


### Crea una clase en JavaScript.

  - Una clase es simplemente algo parecido a un plano que noss permite crear distintos objetos de la misma clase.


  ~~~
    class TransbordadorEspacial { /*UPPER CAMEL CASE*/
      /*El objeto TransbordadorEspacial tendra una propiedad llamada planeta*/
      constructor(planeta) {
        this.planeta = planeta;
      }
    }

    var zeus = new TransbordadorEspacial('Júpiter');
    console.log(zeus.planeta);

    var apolo = new TransbordadorEspacial('Marte');
    console.log(zeus.planeta);

    // Ejemplo

    class Mascota {
      constructor(nombre, edad) {
        this.nombre = nombre;
        this.edad = edad;
      }
    }

    var miMascota = new Mascota("Nora", 5);

    console.log(miMascota.nombre);
    console.log(miMascota.edad);

    var tuMascota = new Mascota("Gino", 2);
  ~~~

### Getters y Setters.

  - Getters:
  - Setters:
  ~~~
    class Libro {
      constructor(autor) {
      this._autor = autor; /*_autor Proteje la data como si fuera privada, es una 
      convension que se usa*/
    }

    // Getter accedemos al valor de forma directa.
    get autor() {
      return this._autor;
    }

    // Setter Otorgamos o actualizamos un nuevo valor al objeto.
    set autor(nuevoAutor) {
      this._autor = nuevoAutor;
      }
    }

    const libro = new Libro("anónimo");
    console.log(libro.autor);

    libro.autor = "Gino Smith";
    console.log(libro.autor);
  ~~~

