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
