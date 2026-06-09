# Unidad 1: Trabajo Práctico de Programación

---

## 1. Contenidos Teóricos

###  Algoritmo
Un algoritmo es una secuencia de pasos lógicamente ordenados y finitos que dan solución a un problema determinado. También se clasifican en:

* **Cualitativos:** Implica la descripción a través de frases y palabras.
  > **Ejemplo: ¿Qué hacer para ver una película en el cine?**
  > 1. **Inicio**
  > 2. Ir al cine.
  > 3. Comprar una entrada (o ticket).
  > 4. Ver la película.
  > 5. Regresar a casa.
  > 6. **Fin**

* **Cuantitativos:** Se refiere al uso de cálculos o fórmulas matemáticas.
  > **Ejemplo: ¿Qué hacer para sumar dos números?**
  > 1. **Inicio**
  > 2. Número uno = 3.
  > 3. Número dos = 5.
  > 4. Sumar 3 y 5.
  > 5. El resultado es 8.
  > 6. **Fin**

#### Características de los algoritmos:
1. **Preciso:** Debe indicar el orden de cada paso de manera clara y sin ambigüedades.
2. **Definido:** Si se sigue el algoritmo varias veces con los mismos datos de entrada, los resultados obtenidos deben ser siempre los mismos.
3. **Finito:** Debe tener un tiempo de ejecución limitado; su ejecución debe concluir en algún momento.

---

###  Pseudocódigo
Son instrucciones escritas bajo cierta estructura y reglas que inducirán al alumno hacia los lenguajes de programación de manera más natural.

<img src="./Imagenes/f8dd12e9-9921-48cd-87ec-f3e9fbe77974.jpg" alt="Ejemplo de Pseudocódigo" width="400">

---

###  Diagrama de Flujo
Utiliza símbolos geométricos específicos y flechas para describir las instrucciones detalladas que debe seguir el algoritmo.

<img src="./Imagenes/9da74477-568a-4dea-8045-7397d9c8fe91.jpg" alt="Diagrama de Flujo 1" width="400">

<img src="./Imagenes/7c94bfc3-0605-44ba-bedd-67d02824bb89.jpg" alt="Diagrama de Flujo 2" width="400">

---

###  Prueba de Escritorio
Consiste en simular datos de entrada de forma manual para comprobar si los resultados finales son correctos. 
Si no es así, es necesario revisar el análisis del problema y el diseño del algoritmo para aplicar las respectivas correcciones y repetir la prueba hasta obtener los datos de salida esperados.

<img src="./Imagenes/Captura de pantalla 2026-05-01 191611.png" alt="Prueba de Escritorio" width="400">

---

###  Lenguajes de Programación
Es un conjunto de símbolos y signos que se combinan entre sí según una serie de reglas de sintaxis predefinidas. Permite expresar programas (software) que la computadora pueda ejecutar.

#### Clasificación de los lenguajes:

* **Lenguaje máquina:** Está escrito en el "idioma" nativo que entiende el microprocesador (CPU). Las instrucciones son cadenas de ceros y unos en código binario.
  * *Ejemplo:* La instrucción de sumar los números 9 y 11 podría verse como `0001 1100 0111 0011`.
* **Lenguaje de bajo nivel (Ensamblador / Assembler):** Las instrucciones utilizan mnemotécnicos (abreviaturas de palabras en inglés) en lugar de números.
  * *Ejemplo:* La instrucción de suma sería `ADD 9, 11`.
* **Lenguaje de alto nivel:** Diseñado para que las personas escriban y entiendan los programas de modo mucho más natural, acercándose al lenguaje humano (inglés). Los programas escritos aquí se denominan **programa fuente**.
  * *Ejemplo:* La instrucción de suma sería `suma = 9 + 11;`
  * *Principales lenguajes:* C/C++, Python, Java, PHP, Pascal, C# y Fortran.

> ⚠️ El lenguaje de alto nivel no es entendible directamente por el procesador, por lo que necesita ser traducido mediante uno de los siguientes métodos:

* **Lenguaje algorítmico:** Formado por acciones primitivas de nuestro lenguaje natural (en nuestro caso, español). 
  * *Ejemplo:* `9 + 11 = 20`.
* **Lenguaje compilado:** Se traduce a través de un programa anexo llamado **compilador**, el cual transforma el *programa fuente* en un *programa objeto* ejecutable independiente.
  * *Ventaja:* Es mucho más rápido en su ejecución.
  * *Desventaja:* Es menos flexible, ya que cualquier cambio exige volver a compilar todo el archivo.
* **Lenguaje interpretado:** Requiere de un programa auxiliar (el **intérprete**) que traduce y ejecuta los comandos línea por línea en tiempo real según sea necesario.

#### Entorno de Desarrollo Integrado (IDE):
Herramientas de software que abarcan e integran varias utilidades para el desarrollo en una sola aplicación (editor de código, compilador/intérprete, depurador y, en muchos casos, soporte para control de versiones como Git).

---

###  Programación por Bloques
Es una forma visual de aprender y desarrollar software utilizando piezas gráficas interconectables (como bloques de Lego) en lugar de líneas de código de texto. 
* En programación tradicional escribirías: `print("¡Hola, mundo!")`.
* En programación por bloques, arrastras un bloque visual que dice `"decir"` y le introduces el texto dentro.

---

## 2. Ejercicio con Estructura Secuencial

###  Planteamiento del Problema
Realice un programa que, tomando una cantidad de tiempo expresada en horas, la transforme a su equivalente en días, minutos y segundos.

###  Código Fuente en C
```c
#include <stdio.h>

int main() {
    // VARIABLES
    float horas, dias, minutos, segundos;
    
    // DATOS DE ENTRADA
    printf("Ingrese la cantidad de tiempo en horas: ");
    scanf("%f", &horas);

    // PROCESO
    dias = horas / 24;         
    minutos = horas * 60;       
    segundos = horas * 3600;   

    // SALIDA DE DATOS
    printf("%f horas equivalen a:\n", horas);
    printf("%f dias\n", dias);
    printf("%f minutos\n", minutos);
    printf("%f segundos\n", segundos);

    return 0;
}
