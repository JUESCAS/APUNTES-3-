# Función de transferencia 
#### Julián Castro, Leslie Rodriguez
## Definición
>🔑 La función de transferencia es una representación matemática en el dominio de la frecuencia, obtenida mediante la transformada de Laplace para sistemas continuos, o la transformada Z para sistemas discretos, que describe la relación entre la salida de un sistema lineal e invariante en el tiempo LTI y su entrada, bajo la suposición de condiciones iniciales cero. En esencia, codifica la dinámica del sistema y cómo este modifica una señal de entrada para producir una señal de salida, facilitando el análisis del comportamiento del sistema, su estabilidad y su diseño de control.
## Clasificación de las funciones de transferencia
Las funciones de transferencia en dinámica de sistemas se pueden clasificar de diversas maneras, atendiendo a diferentes criterios en este caso basandose por la presencia de zeros y polos.
### Función de Transferencia Propia
El grado del polinomio del denominador es mayor o igual al grado del polinomio del numerador. Estos sistemas son físicamente realizables.
$$\fraq{N(s)}{D(s)}$
### Función de Transferencia Estrictamente Propia
El grado del polinomio del denominador es estrictamente mayor que el grado del polinomio del numerador. La salida no depende directamente de la entrada actual.
### Función de Transferencia Impropia
El grado del polinomio del numerador es mayor que el grado del polinomio del denominador. Estos sistemas no son físicamente realizables en su forma pura, aunque pueden aparecer como aproximaciones.

💡**Ejemplo 1:** clasificar las siguientes funciones 

$$\begin{align*}
& \frac{s^2 + 1}{2} \quad &\text{impropia} \\
& \frac{1}{s + 1} \quad &\text{Estrictamente propia} \\
& \frac{s^2 - 1}{s + 1} \quad &\text{impropia} \\
& \frac{s - 1}{s + 1} \quad &\text{bipropia}
\end{align*}$$

## Ceros de una función de transferencia 
Los ceros de una función de transferencia son los valores específicos de la variable compleja (ya sea 's' para sistemas continuos o 'z' para sistemas discretos) que anulan el polinomio del numerador de dicha función. Para calcularlos, se toma el polinomio que se encuentra en la parte superior de la expresión de la función de transferencia y se iguala a cero. Al resolver esta ecuación polinómica, las raíces obtenidas son precisamente los ceros del sistema. Estos puntos en el plano complejo tienen una influencia significativa en la dinámica del sistema, particularmente en su respuesta transitoria, afectando aspectos como el sobreimpulso y el tiempo de asentamiento, así como en su comportamiento en el dominio de la frecuencia.

💡**Ejemplo 2:** calcular los ceros de la función  

$$ G(s) = \frac{Y(s)}{U(s)} = \frac{3s - 1}{s^2 + 3s + 2} = \frac{N(s)}{D(s)}$$
$$ 3s - 1 = 0 $$
$$ s = \frac{1}{3}$$

💡**Ejemplo 3:** calcular los ceros de la función 

$$\frac{s^2 + 4s + 1}{s^4 + 3s^3 + 3s^2 + s + 2}$$

## Polos de una función de transferencia 
Los polos de una función de transferencia son los valores de la variable compleja 's' (para sistemas continuos) o 'z' (para sistemas discretos) que hacen que el denominador de la función de transferencia sea igual a cero, provocando que la magnitud de la función de transferencia tienda a infinito. En otras palabras, son las raíces del polinomio característico del sistema, que se obtiene al igualar a cero el denominador de la función de transferencia.

💡**Ejemplo 4:** calcular los polos de la función 

$$ G(s) = \frac{Y(s)}{U(s)} = \frac{3s - 1}{s^2 + 3s + 2} = \frac{N(s)}{D(s)}$$
$$ D(s) = 0$$
$$\begin{align*}
s^2 + 3s + 2 = 0 \\
(s + 1)(s + 2) = 0 \\
s = -1 \\
s = -2
\end{align*}$$

💡**Ejemplo 5:** calcular los polos de la función

$$\frac{(s+2)}{(s+3)(s^2 + 0.5s + 1)}$$

## Grado de una función de transferencia 
El grado de una función de transferencia de un sistema lineal e invariante en el tiempo (LTI) está determinado por el orden del sistema. El orden del sistema se define como el grado del polinomio del denominador de la función de transferencia cuando se expresa como una fracción irreducible de polinomios en la variable compleja 's' (para sistemas continuos) o 'z' (para sistemas discretos).

$$G(s) = \frac{3s - 1}{s^2 + 3s + 2}$$

## Teorema del valor final 

El teorema del valor final en la dinámica de sistemas es una herramienta que permite determinar el valor al que tiende la salida de un sistema lineal e invariante en el tiempo (LTI) cuando el tiempo tiende a infinito, directamente a partir de su transformada de Laplace Y(s), sin necesidad de calcular la transformada inversa y(t). Este teorema establece que si el límite lim t→∞ y(t) existe (es decir, la salida se estabiliza en un valor constante), entonces este valor final está dado por el límite de sY(s) cuando s tiende a cero. Es una herramienta útil para analizar el comportamiento estacionario de los sistemas en respuesta a entradas escalón o impulsionales, siempre y cuando todos los polos de sY(s) se encuentren en el semiplano izquierdo del plano complejo 's'.

$$\lim_{t \to \infty} f(t) = \lim_{s \to 0} sF(s)$$

💡**Ejemplo 6:** 

$$\begin{align*}
G(s) &= \frac{Y(s)}{U(s)} = \frac{4}{5s + 1} \\
Y(s) &= \frac{4 \cdot U(s)}{5s + 1}
\end{align*}$$
$$Y(s) = \frac{\frac{4}{s}}{5s + 1}$$
$$\lim_{s \to 0} sY(s) = \lim_{s \to 0} s \cdot \frac{\frac{4}{s}}{5s + 1}$$
$$\lim_{s \to 0} \frac{4}{5s + 1} = 4$$

💡**Ejemplo 7:** calcular los polos de la función

$$G(s) = \frac{Y(s)}{U(s)} = \frac{8}{s^3 + 6s^2 + 11s + 6}$$

💡**Ejemplo 8:** calcular los polos de la función

$$G(s) = \frac{Y(s)}{U(s)} = \frac{8}{s^3 + 8s^2 + 15s}$$

## 7. Ejercicios
### 📚Ejercicio 1
Dada la siguiente función de transferencia, determine los zeros y los polos:

$$
G(s) = \frac{5(s + 3)}{s^2 + 4s + 3}
$$


$$
5(s + 3) = 0 \Rightarrow s = -3
$$

✅ **Zeros**: \( s = -3 \)

$$
s^2 + 4s + 3 = 0 \Rightarrow (s + 1)(s + 3) = 0 \Rightarrow s = -1,\ -3
$$

✅ **Polos**: \( s = -1,\ s = -3 \)
 
### 📚Ejercicio 2
Sea la función de transferencia:

$$
G(s) = \frac{10(s + 2)}{s(s + 5)(s + 1)}
$$

Determine los polos y los zeros.

$$
10(s + 2) = 0 \Rightarrow s = -2
$$

✅ **Zeros**: \( s = -2 \)


$$
s(s + 5)(s + 1) = 0 \Rightarrow s = 0,\ -5,\ -1
$$

✅ **Polos**: \( s = 0,\ s = -1,\ s = -5 \)

## 8. Conclusiones
La función de transferencia es una herramienta fundamental en el análisis y diseño de sistemas dinámicos, ya que permite describir la relación entre la salida y la entrada de un sistema lineal en el dominio de Laplace (dominio (s)).

Para obtener una función de transferencia correcta, es indispensable identificar claramente cuál es la entrada y cuál es la salida del sistema, ya que esto define el comportamiento que se desea modelar o controlar.

Trabajar en el dominio de Laplace simplifica la resolución de ecuaciones diferenciales, permitiendo convertir derivadas e integrales en operaciones algebraicas y facilitar así el análisis de sistemas complejos.

## 9. Bibliografia 

[ChatGPT] (https://openai.com/chatgpt)

[Katsuhiko Ogata] (dinamica de sistemas.PHH prentice Hall)

[Lidefer] (https://fjferrer.webs.ull.es/Apuntes3/Leccion01/15_dinmica_de_los_sistemas_mecanicos.html)
