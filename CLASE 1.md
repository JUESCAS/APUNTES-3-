# Función de transferencia 
## Función de transferencia 
la función de transferencia es una representación matemática en el dominio de la frecuencia obtenida mediante la transformada de Laplace para sistemas continuos o la transformada Z para sistemas discretos que describe la relación entre la salida de un sistema lineal e invariante en el tiempo LTI y su entrada, bajo la suposición de condiciones iniciales cero. En esencia, codifica la dinámica del sistema y cómo este modifica una señal de entrada para producir una señal de salida, facilitando el análisis del comportamiento del sistema, su estabilidad y su diseño de control.
## Clasificación de las funciones de transferencia
Las funciones de transferencia en dinámica de sistemas se pueden clasificar de diversas maneras, atendiendo a diferentes criterios en este caso basandose por la presencia de ceros y polos
### Función de Transferencia Propia
El grado del polinomio del denominador es mayor o igual al grado del polinomio del numerador. Estos sistemas son físicamente realizables.
### Función de Transferencia Estrictamente Propia
El grado del polinomio del denominador es estrictamente mayor que el grado del polinomio del numerador. La salida no depende directamente de la entrada actual.
### Función de Transferencia Impropia
El grado del polinomio del numerador es mayor que el grado del polinomio del denominador. Estos sistemas no son físicamente realizables en su forma pura, aunque pueden aparecer como aproximaciones.
## Ceros de una función de transferencia 
Los ceros de una función de transferencia son los valores específicos de la variable compleja (ya sea 's' para sistemas continuos o 'z' para sistemas discretos) que anulan el polinomio del numerador de dicha función. Para calcularlos, se toma el polinomio que se encuentra en la parte superior de la expresión de la función de transferencia y se iguala a cero. Al resolver esta ecuación polinómica, las raíces obtenidas son precisamente los ceros del sistema. Estos puntos en el plano complejo tienen una influencia significativa en la dinámica del sistema, particularmente en su respuesta transitoria, afectando aspectos como el sobreimpulso y el tiempo de asentamiento, así como en su comportamiento en el dominio de la frecuencia.
## Polos de una función de transferencia 
Los polos de una función de transferencia son los valores de la variable compleja 's' (para sistemas continuos) o 'z' (para sistemas discretos) que hacen que el denominador de la función de transferencia sea igual a cero, provocando que la magnitud de la función de transferencia tienda a infinito. En otras palabras, son las raíces del polinomio característico del sistema, que se obtiene al igualar a cero el denominador de la función de transferencia.
## Grado de una función de transferencia 
El grado de una función de transferencia de un sistema lineal e invariante en el tiempo (LTI) está determinado por el orden del sistema. El orden del sistema se define como el grado del polinomio del denominador de la función de transferencia cuando se expresa como una fracción irreducible de polinomios en la variable compleja 's' (para sistemas continuos) o 'z' (para sistemas discretos).
## Teorema del valor final 

