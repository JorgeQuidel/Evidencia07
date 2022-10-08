# Evidencia07

<h2>Análisis Clases</h2>

Las clases identificadas en este problema son la clase Calculadora y la clase CarroCompra. La clase Calculadora está destinada a realizar operaciones de suma y multiplicación entre dos números. La clase CarroCompra simula la funcionalidad de un carrito de compras, con una lista de productos y un monto total.


<h2>Análisis Atributos y Métodos</h2>

<h3>Clase Calculadora</h3>

La clase Calculadora tiene dos atributos privados llamados n1 y n2, los cuales representan números enteros. Cuenta con dos constructores, uno para instanciar un objeto inicializando los atributos en cero y el otro para instanciar un objeto entregando dos números enteros como parámetros para inicializar los atributos con el valor de dichos números. Los métodos de la clase son sumar, multiplicar, setN1 y setN2. 

Los métodos públicos sumar y multiplicar llaman a los atributos del objeto y retornan el valor de la suma y multiplicación entre ellos respectivamente.

Los métodos públicos setN1 y setN2 reciben ambos como parámetros un número entero para asignar directamente el valor recibido al atributo respectivo.

<h3>Clase CarroCompra</h3>

La clase CarroCompra tiene un atributo privado llamado productos, siendo un arreglo de números enteros de 2 x 5 el cual representa una fila para la cantidad de un producto y otra para el precio de un producto, con un máximo de 5 productos. Cuenta con un único constructor el cuál no recibe parámetros, dentro del constructor el arreglo se llena de la siguiente forma: todos los elementos de la primera fila valen 1 (cantidad producto), y todos los elementos de la segunda fila valen 1000 (precio producto). Los métodos de la clase son calcularTotal, subTotal y mostrarTotal.

El método privado subTotal recibe como parámetros un entero para la cantidad y otro para el precio, luego instancia un objeto de la clase Calculadora y llama al método multiplicar, de esta forma retorna un entero resultado de multiplicar el precio de un producto por su cantidad. En este método podemos ver un caso de implementación de dependencia entre la clase Calculadora y CarroCompra, de la forma CarroCompra depende de Calculadora.

El método privado calcularTotal itera 5 veces llamando al método subTotal para calcular el costo total de la compra, entregando como parámetros un elemento de la fila que representa la cantidad de productos en la posición i y un elemento de la fila que representa el precio del producto en la posición i, retornando la suma del costo de cada producto por su cantidad.

El método público mostrarTotal imprime en pantalla el resultado del método calcularTotal.

