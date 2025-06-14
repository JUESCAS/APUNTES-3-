# Modelamiento de sistemas con diagramas de bloques 
#### Julián Castro, Leslie Rodriguez
## Modelos de sistemas complejos 
### Solenoide
>🔑 Un solenoide para la dinámica de sistemas es un actuador electromecánico que convierte una señal eléctrica en una fuerza mecánica lineal a través de un campo magnético generado por un transductor  que atrae o repele un émbolo ferromagnético

Su comportamiento dinámico, caracterizado por la relación entre la entrada eléctrica (voltaje o corriente) y la salida mecánica fuerza mecánica que es proporcional a la corriente en e bobinado, el electroimán atrae una masa que es acoplada en el resorte cuyo amortiguamiento es dado por la envolvente de la bobina. 

$$V_L + V_R = v(t)$$
$$L \frac{di}{dt} + Ri = v(t)$$
$$LsI(S) + RI(S) = V(S)$$
$$I(S)(Ls + R) = V(S)$$
$$I(S) = V(S) \frac{1}{Ls + R}$$
$$\frac{I(S)}{V(S)} = \frac{1}{Ls + R}$$
$$f_s = K_s I(S)$$
$$\frac{f_s(S)}{I(S)} = K_s$$
$$f(t) - Kx - b\dot{x} = m\ddot{x}$$
$$F(S) - KX(S) - bSX(S) = mS^2 X(S)$$
$$F(S) = X(S)(mS^2 + bS + K)$$
$$X(S) = F(S) \frac{1}{mS^2 + bS + K}$$


### Motor DC
>🔑 Un motor de corriente continua (DC) es un actuador electromecánico que convierte energía eléctrica en energía mecánica rotacional mediante la interacción entre un campo magnético estático (generado por imanes permanentes o bobinas de campo) y un campo magnético rotatorio inducido por la corriente que fluye a través de las bobinas de la armadura.

Desde la perspectiva de la dinámica de sistemas, su funcionamiento se analiza mediante ecuaciones diferenciales que relacionan el voltaje de entrada con la corriente, el par motor y la velocidad angular, considerando parámetros como la resistencia y la inductancia de la armadura, la constante de par, la constante de fuerza contraelectromotriz y el momento de inercia y la fricción de la carga.
#### Motor DC (corriente de campo)
El modelado de un motor DC desde la corriente de campo se centra en cómo la variación de la corriente que circula por las bobinas del campo magnético afecta el rendimiento del motor, especialmente el par motor y la velocidad; en este enfoque, la corriente de armadura se considera generalmente controlada o constante, y la dinámica del sistema se describe principalmente por la relación entre la corriente de campo y el flujo magnético generado, el cual a su vez influye directamente en la constante de par y la constante de fuerza contraelectromotriz del motor.


$$L_c \frac{di_c}{dt} + R_c i_c = v_c(t)$$
$$I_c(s) = V_c(s) \frac{1}{(sL_c + R_c)}$$
$$\Phi = K_c i_c$$
$$T_m = K_a i_a(t) K_c i_c(t)$$
$$T_m(s) = (K_a K_c I_a) I_c(s) = K_m I_c(s)$$
$$T_c(s) = T_m(s) - T_p(s)$$
$$J \frac{d^2\theta}{dt^2} + b \frac{d\theta}{dt} + k\theta = \tau(t)$$
$$\Theta(s) = T_c(s) \frac{1}{(s^2 J + bs)}$$
$$\Theta(s) = V_c(s) \frac{K_m}{(s L_c + R_c)(J s^2 + bs)} - T_p(s) \frac{1}{(J s^2 + bs)}$$
$$\frac{\Theta(s)}{V_c(s)} = \frac{K_m}{(s L_c + R_c)(J s^2 + bs)}$$

#### Motor DC (corriente de armadura)
El modelado de un motor DC desde la corriente de armadura se enfoca en cómo la variación de la corriente que fluye a través de las bobinas del rotor (armadura) afecta directamente el par motor y, consecuentemente, la velocidad angular; en este enfoque, el flujo magnético generado por la corriente de campo se considera constante (típicamente proporcionado por imanes permanentes o una excitación de campo fija), y la dinámica del sistema se describe primordialmente por la relación entre el voltaje aplicado a la armadura y la corriente resultante, el par motor producido (proporcional a la corriente de armadura) y la velocidad angular del rotor.

$$T_m(s) = (K_a K_c I_c) I_a(s) = K_m I_a(s)$$
$$V_a(s) = (s L_a + R_a) I_a(s) + V_b(s)$$
$$V_a(s) = (s L_a + R_a) I_a(s) + V_b(s)$$
$$V_b(s) = K_b \omega(s)$$
$$I_a(s) = \frac{V_a(s) - K_b \omega(s)}{s L_a + R_a}$$
$$T_c(s) = T_m(s) - T_p(s)$$
$$\Theta(s) = T_c(s) \frac{1}{(s^2 J + bs)}$$

## Elementos transmisores de energía 
### Engranajes y poleas 
>🔑 Un sistema de engranajes y poleas, en dinámica de sistemas, es un subsistema mecánico que transmite y modifica movimiento rotacional y par mediante la interconexión de cuerpos rígidos con relaciones de transmisión definidas por sus dimensiones

Su modelado implica considerar la transformación de velocidad y par, la inercia equivalente referida a un eje.

$$\frac{\tau_2}{\tau_1} = \frac{N_2}{N_1}$$
$$\frac{N_2}{N_1} = -\frac{\theta_1}{\theta_2}$$
$$\frac{\Theta(s)}{V_c(s)} = \frac{K_m}{(s L_c + R_c)(J s^2 + bs)}$$
$$\beta_{equiv} = \left(\frac{N_1}{N_2}\right)^2 \beta \quad y$$
$$J_{equiv} = J_{N1} + \left(\frac{N_1}{N_2}\right)^2 (J + J_{N2})$$

### Transmisor rotacional a lineal 
>🔑 Un transmisor rotacional a lineal en dinámica de sistemas es un mecanismo o dispositivo que convierte un movimiento de rotación (velocidad angular, par) en un movimiento lineal (velocidad lineal, fuerza).

Su modelado dinámico se centra en la relación matemática que describe esta transformación, considerando factores como la geometría del mecanismo (por ejemplo, el radio en un sistema piñón-cremallera o tornillo sin fin), la eficiencia de la conversión, la inercia rotacional que se traduce en una masa lineal equivalente, y cualquier fricción o holgura presente en el sistema.
### Palancas 
>🔑 Una palanca, en el estudio del movimiento de sistemas, es una barra rígida que gira sobre un punto de apoyo llamado pivote.

Para entender cómo funcionan en sistemas más complejos, pensamos en las fuerzas que actúan sobre ellas y en dónde están aplicadas respecto al pivote. La ventaja mecánica nos dice si la palanca hace que la fuerza que necesitamos aplicar sea menor o mayor. También consideramos cómo la palanca acelera o frena cuando se le aplica una fuerza, lo que depende de su peso y forma (su inercia).

$$-\frac{f_2}{f_1} = \frac{d_1}{d_2} \quad y \quad \frac{d_1}{d_2} = -\frac{x_1}{x_2}$$

## Potenciómetro
>🔑 Un potenciómetro es una resistencia eléctrica variable que se usa para controlar el voltaje en un circuito.

Funciona como un divisor de voltaje ajustable: al girar o deslizar una perilla o cursor, se cambia la proporción de la resistencia total, lo que altera la cantidad de voltaje que sale por un terminal específico.
### Potenciómetro de rotación 
>🔑 Es un sensor que convierte la posición angular de un eje rotatorio en una señal eléctrica, típicamente un voltaje variable.

Su funcionamiento se basa en un elemento resistivo circular sobre el cual se desliza un contacto móvil conectado al eje. A medida que el eje gira, la resistencia entre el contacto móvil y uno de los extremos del elemento resistivo cambia proporcionalmente al ángulo de rotación.

$$V_o = \frac{\theta}{\theta_{máx}} V_a$$
 
### Potenciómetro de translación 
>🔑 Un potenciómetro de traslación (también conocido como potenciómetro lineal o deslizante) es un sensor que convierte una posición lineal en una señal eléctrica, generalmente un voltaje variable. Internamente, consiste en una tira de material resistivo y un contacto deslizante que se mueve a lo largo de esta tira.

Al aplicar un voltaje a los extremos de la tira resistiva, la posición del contacto deslizante determina la cantidad de resistencia entre este y uno de los extremos, actuando como un divisor de voltaje variable.

$$V_o = \frac{x}{x_{máx}} V_a$$

## Tacómetros 
>🔑 Un tacómetro en dinámica de sistemas es un sensor utilizado para medir la velocidad angular de un eje rotatorio.

Proporciona una señal de salida, generalmente un voltaje o una serie de pulsos, que es proporcional a la velocidad de rotación.

$$v(t) = k \frac{d\theta(t)}{dt}$$
$$G(s) = \frac{V(s)}{\Theta(s)} = ks$$

## Sensores transmisores
### Lineales

$$H(s) = \frac{TO}{PV} = K$$

### No lineales 

$$H(s) = \frac{TO(s)}{PV(s)} = \frac{K_T}{\tau_T s + 1}$$

## Modelos de procesos 
### Mezcla de sustancias
Se representa como un sistema donde las entradas son los flujos de las sustancias reaccionantes (con sus concentraciones, temperaturas, etc.) y las salidas son los flujos de los productos y reactivos no convertidos. Dentro del bloque del reactor, se consideran las relaciones constitutivas que describen la cinética de la reacción química (velocidad de reacción en función de la concentración y temperatura), el balance de masa de cada especie química (entrada - salida + generación/consumo = acumulación), y el balance de energía (transferencia de calor, calor de reacción, acumulación de energía térmica).
### Sistema térmico 
Un sistema térmico en dinámica de sistemas se modela por bloques representando componentes como fuentes de calor, resistencias térmicas (conducción, convección, radiación) y capacitancias térmicas (almacenamiento de energía). Las entradas suelen ser el flujo de calor aplicado o la temperatura ambiente, y las salidas son las temperaturas en diferentes puntos del sistema.

$$G(s) = \frac{T(s)}{Q_{in}(s)} = \frac{1/C}{s + 1/RC}$$

## 7. Ejercicios
### 📚Ejercicio 1
<img src="build/sistemaej1.PNG"  width="300"/>
<img src="build/sistemaej1a.PNG"  width="300"/>
<img src="build/sistemaej1b.PNG"  width="300"/>
<img src="build/sistemaej1c.PNG"  width="300"/>
<img src="build/sistemaej1d.PNG"  width="300"/>
<img src="build/sistemaej1e.PNG"  width="300"/>


### 📚Ejercicio 2
## 8. Conclusiones
El uso de diagramas de bloques facilita el modelado de sistemas complejos, ya que permite representar gráficamente las relaciones funcionales entre los componentes del sistema, evitando la manipulación directa de ecuaciones diferenciales complejas. A diferencia del enfoque puramente matemático, los diagramas de bloques brindan una visión modular del sistema, en la que cada bloque representa una función de transferencia específica, simplificando así el análisis, la simulación y el diseño del sistema.

Para construir correctamente un diagrama de bloques, es fundamental definir con claridad la entrada y la salida del sistema, ya que esto determina la dirección del flujo de señal y el comportamiento global del modelo.

## 9. Bibliografia 

[ChatGPT] (https://openai.com/chatgpt)

[Katsuhiko Ogata] (dinamica de sistemas.PHH prentice Hall)


[Lidefer] (https://fjferrer.webs.ull.es/Apuntes3/Leccion01/15_dinmica_de_los_sistemas_mecanicos.html)



