# Diagrama de flujo de señales
## 1 Diagrama de flujo de señales
## 2 Elementos de los diagramas de flujo
### 2.1 Nodo
### 2.2 Flecha
## 3 Interpretacion de los diagramas de flujo de señales 
## 4 Conceptos para interpretar un diagrama de flujo de señales 
### 4.1 Camino o trayectoria 
### 4.2 Ganancia de lazo 
### 4.3 Trayecto o camino directo 
### 4.4 Ganancia de trayecto directo 
### 4.5 Lazo 
### 4.6 Ganancia de lazo 
## 5 Comparacion entre diagrama de bloques y diagrama flujo de señales 
## 6 Formula de Mason

💡**Ejemplo 1:**  


<img src="build/EJ1.JPG"  width="300"/>
Figura 8

$$\text{Trayectoria directa$$
$$P_1 = 1 * 1 * G_1 * G_2 * G_3 * 1 = G_1 G_2 G_3$$
$$\text{Lazos cerrados}$$
$$L_1 = G_1 G_2 H_1$$
$$L_2 = -G_2 G_3 H_2$$
$$L_3 = -G_1 G_2 G_3$$
$$\Delta = 1 - (L_1 + L_2 + L_3) \quad \$$
$$\Delta_1 = 1 \quad \text{Cofactores}$$
$$\frac{C(s)}{R(s)} = \frac{P_1 \Delta_1}{\Delta} = \frac{G_1 G_2 G_3}{1 - G_1 G_2 H_1 + G_2 G_3 H_2 + G_1 G_2 G_3}$$


💡**Ejemplo 2:** 

<img src="build/EJ2.JPG"  width="300"/>
Figura 8

$$\text{Trayectoria directa}$$
$$P_1 = G_1 G_2 G_3 G_4 G_5$$
$$P_2 = G_1 G_6 G_4 G_5$$
$$P_3 = G_1 G_2 G_7$$
$$\text{Lazos cerradoP}$$
$$L_1 = -G_4 H_1$$
$$L_2 = -G_2 G_7 H_2$$
$$L_3 = -G_6 G_4 G_5 H_2$$
$$L_4 = -G_2 G_3 G_4 G_5 H_2$$
$$\text{Determinante}$$
$$\Delta = 1 - (L_1 + L_2 + L_3 + L_4) + L_1 L_2$$
$$\Delta_1 = 1$$
$$\Delta_2 = 1$$
$$\Delta_3 = 1 - L_1$$
$$\frac{C(s)}{R(s)} = \frac{G_1 G_2 G_3 G_4 G_5 + G_1 G_6 G_4 G_5 + G_1 G_2 G_7 (1 + G_4 H_1)}{1 + G_4 H_1 + G_2 G_7 H_2 + G_6 G_4 G_5 H_2 + G_2 G_3 G_4 G_5 H_2 + G_4 H_1 G_2 G_7 H_2}$$

💡**Ejemplo 3:** 

<img src="build/EJ3.JPG"  width="330"/>

Figura 8


## 7. Ejercicios
### 📚Ejercicio 1
### 📚Ejercicio 2
## 8. Conclusiones

El modelo de sistemas hidraulicos es uno de los mas versatiles ya que permite modelar modelar cada tanque de manera independiente segun la variable que se requiera, y despues buscar una incognita que me permita relacionar todos los sistemas en funcion de construir un modelo en general. Una vez diseñado o en operación, los modelos permiten predecir y analizar el rendimiento del sistema ante diferentes cargas, perturbaciones o cambios en los parámetros. Esto ayuda a comprender el comportamiento dinámico, identificar posibles cuellos de botella, evaluar la eficiencia y prever la respuesta ante situaciones inesperadas.

## 9. Bibliografia 

[ChatGPT] (https://openai.com/chatgpt)

[Katsuhiko Ogata] (dinamica de sistemas.PHH prentice Hall)


[Lidefer] (https://fjferrer.webs.ull.es/Apuntes3/Leccion01/15_dinmica_de_los_sistemas_mecanicos.html)
