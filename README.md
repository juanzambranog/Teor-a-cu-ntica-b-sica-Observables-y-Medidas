# Teoría cuántica básica, Observables y Medidas

### En este repositorio se encuentra la solucion a la serie de problemas propuestos correspondientes a la teoría cuántica básica, observables y medidas.

## Simule el primer sistema cuántico descrito en la sección 4.1.

#### La solucion propuesta define una clase SistemaCuantico en Python para calcular probabilidades en sistemas cuánticos. La clase tiene métodos para calcular la probabilidad de encontrar el sistema en una posición específica y la probabilidad de transición entre estados cuánticos.

### Explicacion de los metodos:

- __init__(self, num_posiciones, vector_ket):

Método constructor que inicializa la clase. Recibe el número de posiciones posibles y un vector que representa el estado cuántico del sistema.

- calcular_probabilidad(self, posicion):

Calcula la probabilidad de que el sistema se encuentre en una posición específica. Verifica que la posición sea válida y devuelve el cuadrado del valor absoluto del elemento correspondiente en el vector ket.

- calcular_probabilidad_transicion(self, vector_ket_final):

Calcula la probabilidad de transición entre el estado actual y un estado final dado. Verifica que el vector final tenga la misma longitud que el vector ket inicial y utiliza el producto escalar para determinar la probabilidad de transición.

## Complete los retos de programación del capítulo 4.

#### Esta solucion define una clase SistemaCuantico para simular y analizar sistemas cuánticos. La clase proporciona métodos para calcular la amplitud de transición, la media y varianza de una observable, la comprobación de si una matriz es hermitiana, el cálculo de valores propios, la probabilidad de transición y el estado final después de una serie de operaciones unitarias.

### Explicacion de los metodos:

- amplitud_transicion(self, vector1, vector2):
  Calcula la amplitud de transición entre dos vectores.
  
- calcular_media_varianza(self, matriz_observable, vector_ket):
  Calcula la media y varianza de una observable en un estado cuántico.
  
- es_hermitiana(self, matriz):
  Comprueba si una matriz es hermitiana.
  
- calcular_valores_propios(self, matriz_observable):
  Calcula los valores propios y vectores propios de una matriz observable.
  
- calcular_probabilidad_transicion(self, vector_ket, vectores_propios):
  Calcula la probabilidad de transición entre un estado inicial y un conjunto de vectores propios.
  
- calcular_estado_final(self, estado_inicial, matrices_un):
  Calcula el estado final después de aplicar una serie de operaciones unitarias a un estado inicial.


  ## EJERCICIOS

  ### Ejercicio 4.3.1

  #### Este código resuelve el ejercicio 4.3.1, que consiste en aplicar la operadora de giro Sx a un estado de giro inicial y calcular la probabilidad de permanecer en ese estado.

    1. Se definen los estados de giro inicial (spin_up) y final (spin_down) como vectores en un espacio de Hilbert de dos dimensiones.
    2. Se define la operadora de giro Sx como una matriz 2x2 que representa la operación de giro en el eje x.
    3. Se aplica la operadora Sx al estado de giro inicial (spin_up) mediante el producto matricial np.dot(Sx, spin_up), lo que produce un nuevo estado (resulting_state).
    4. Se calcula la probabilidad de permanecer en el estado de giro inicial (spin_up) mediante el producto escalar np.dot(spin_up, resulting_state) y elevando al cuadrado el resultado

  ### Ejercicio 4.3.2

  #### Este código resuelve el ejercicio 4.3.2, que consiste en graficar la distribución de probabilidad de los valores propios de un sistema cuántico.

    1. Definición de valores propios y probabilidades:
      Se definen dos valores propios (eigenvalues) como 0.5 y -0.5, y sus respectivas probabilidades (probabilities) como 1.0 y 0.0. Esto indica que el primer valor propio tiene una probabilidad total de 1,       mientras que el segundo no tiene probabilidad.

    2. Creación del gráfico:
      Se utiliza plt.bar() para crear un gráfico de barras que representa la distribución de probabilidad de los valores propios. Los valores propios se colocan en el eje x y las probabilidades en el eje y.
      Se añaden etiquetas a los ejes (xlabel, ylabel) y un título al gráfico (title).
      Se ajustan las marcas del eje x para que correspondan a los valores propios y se establece el límite del eje y de 0 a 1.1.
      Mostrar el gráfico:
      
    3. Finalmente, se utiliza plt.show() para mostrar el gráfico en pantalla.
 
  ### Ejercicio 4.4.1

  #### Este código resuelve el ejercicio 4.4.1, que consiste en comprobar si dos matrices son unitarias y verificar si sus productos también son unitarios.

    1. Se definen dos matrices u1 y u2. La matriz u1 es la matriz de intercambio, y u2 es una matriz que se construye utilizando la raíz cuadrada de 2.
    2. Se utiliza la función matrizUnitariaComprobacion() para verificar si u1 es unitaria. El resultado se almacena en bool1, y se imprime si la matriz es unitaria o no, se repite el proceso para u2,       
       almacenando el resultado en bool2.
    3. Se multiplican las matrices u1 y u2 y se almacenan los resultados en mult1 (U1 * U2) y mult2 (U2 * U1) utilizando la función productoDeMatrices()
    4. Se verifica si el producto mult1 es unitaria utilizando matrizUnitariaComprobacion() y se imprime el resultado.
Se realiza la misma verificación para el producto mult2. 


  ### Ejercicio 4.4.2

  #### Este código resuelve el ejercicio 4.4.2, que se centra en la evolución de un estado cuántico a través de una matriz de transición en varios pasos de tiempo.
 
   1. Se define tp como 1/Sqrt(2), que se utilizará en la matriz de transición. estadoI es un vector que representa el estado inicial del sistema cuántico, donde solo el primer elemento tiene una amplitud diferente de cero.
   2. A es una matriz 4x4 que describe cómo el estado cuántico evoluciona a través de interacciones. Cada elemento de la matriz puede contener números complejos, representando amplitudes de probabilidad.
   3. a función click(A, 3) se utiliza para aplicar la matriz de transición A al estado cuántico inicial estadoI durante 3 pasos. El resultado se almacena en cli, que representa la matriz de transición tras 3 interacciones.
   4. Se imprime la matriz cli que muestra cómo ha evolucionado la matriz de transición después de 3 pasos de tiempo.
   5. Se utiliza la función productoMatrizVector(cli, estadoI) para calcular el nuevo vector de estado resultante tras aplicar la matriz cli al estado inicial estadoI. Este vector representa las probabilidades de encontrar el sistema en diferentes estados.
   6. Se imprime el vector de probabilidades resultante y se calcula y muestra la probabilidad de encontrar la "bola cuántica" en el tercer punto del vector resultante.


  ## Lenguaje usado para hacer la libreria.
    * Python

  ## Instalaciòn y ejecucion del proyecto
     Descargue el repositorio lo puede realizar de tres formas:
    * Clonando el codigo con uno de los siguientes enlaces: 
    * HTTPS: https://github.com/juanzambranog/Complejos.git
    * SSH: git@github.com:juanzambranog/Complejos.git
    * GitHub CLI: gh repo clone juanzambranog/Complejos
    * Descargando el repositorio en formato .zip
    * Abrir el repositorio con GitHub Desktop
    

  ## Archivos
  
  Se encontraran un archivo:
  * Teoría_Cuantica_Basica_Observables_Y_Medidas.ipynb
    * Este archivo es un cuaderno de Jupyter, en el cual se encontraran las soluciones a los ejercicios propuestos.

