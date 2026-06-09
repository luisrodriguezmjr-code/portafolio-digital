## Unidad 1

# TRABAJO PRÁCTICO DE PROGRAMACIÓN

---

## 1. Contenidos Teóricos

* Algoritmo

Un algoritmo es una secuencia de pasos lógicamente ordenados y finitos que dan solución a un problema determinado. También deben ser:
Cualitativos: Implica la descripción a través de frases y palabras.
Ejemplo:
¿Qué hacer para ver una película en el Cine?
0. Inicio
1. Ir al cine.
2. Comprar una entrada (o ticket).
3. Ver la película.
4. Regresar a casa.
5. Fin

Cuantitativos: Se refiere al uso de cálculos o fórmulas matemáticas.
Ejemplo:
¿Qué hacer para sumar dos números?
0. Inicio
1. Numero uno 3.
2. Número dos 5.
3. Sumar 3 y 5.
4. El resultado es 8.
5. Fin

Características:
1. Un algoritmo debe ser "preciso", indicar el orden de cada paso de manera clara y sin ambigüedades.
2. Un algoritmo debe estar "definido", si se sigue el algoritmo varias veces con los mismos datos de entrada, los resultados obtenidos deben ser los mismos.
3. Un algoritmo debe ser "finito", de tiempo finito, su ejecución debe concluir en algún momento.

* Pseudocódigo

Son instrucciones escritas bajo cierta estructura y reglas que inducirán al alumno hacia los lenguajes de programación.

<img width="642" height="848" alt="f8dd12e9-9921-48cd-87ec-f3e9fbe77974" src="https://github.com/user-attachments/assets/d236c3e8-3a6b-4658-b7d4-bcc58ed24daf" />



>

* Diagrama de Flujo

Utiliza símbolos y describen las instrucciones que debe seguir el algoritmo.

<img width="986" height="771" alt="7c94bfc3-0605-44ba-bedd-67d02824bb89" src="https://github.com/user-attachments/assets/e7d762b0-abb4-438c-a9f3-5f1d752485b2" />
<img width="606" height="565" alt="9da74477-568a-4dea-8045-7397d9c8fe91" src="https://github.com/user-attachments/assets/98f15557-f170-45f9-a952-6327f7c8418b" />


* Prueba de Escritorio

Simular datos de entrada, para comprobar que los resultados sean correctos.
De no ser así, será necesario revisar el análisis del problema y el código del algoritmo para aplicar las respectivas correcciones y repetir la prueba de escritorio hasta obtener los datos de salida esperados o correctos.

<img width="746" height="300" alt="Captura de pantalla 2026-05-01 191611" src="https://github.com/user-attachments/assets/9452092b-c5cd-4148-ab18-cad4793d23ad" />


* Lenguajes de Programación

Es un conjunto de símbolos y signos que se combinan entre sí según una serie de reglas de sintaxis predefinidas del lenguaje. Permite expresar programas (software).
Los lenguajes de programación se pueden clasificar de la siguiente manera:
Lenguaje máquina:
Está escrito en un “idioma” que entiende el microprocesador (el CPU, el cerebro de la máquina). Las instrucciones son cadenas de 0 y 1 en código binario. 
La instrucción sumar los números 9 y 11 podría ser 0001 1100 0111 0011 1001 1011
Lenguaje bajo nivel:
Son los ENSAMBLADORES (ASSEMBLER). Las instrucciones son mnemotécnicos (patrones o abreviaturas de palabras), como por ejemplo ADD, DIV, STR, etc. 
La instrucción de suma sería ADD 9, 11 o ADD x,y,z
Lenguaje alto nivel:
Está diseñado para que las personas escriban y entiendan los programas de modo mucho más natural (inglés), acercándose al lenguaje natural:
La instrucción de sumar sería suma = 9 + 11
Los programas escritos en un lenguaje de alto nivel se llama programa fuente.
Existen muchos lenguajes de alto nivel, los principales son: c/c++, Visual Basic, Pascal, php, Python, Java y Fortran.

El lenguaje de alto nivel no es entendible directamente por la máquina (se aleja del procesador), entonces necesita ser traducido.

Lenguaje algorítmico:
Está formado por acciones primitivas provenientes de nuestro lenguaje natural, entonces se podrá escribir en español. 
La instrucción de sumar sería 9+11=20

Lenguaje compilado:
Un programa escrito en un lenguaje compilado se traduce a través de un programa anexo llamado compilador. El compilador traduce el programa fuente a uno llamado programa objeto. Este programa objeto se utiliza en la fase de ejecución del programa, obteniendo un programa ejecutable (que no requiere de ninguna traducción).

Lenguaje interpretado:
Un programa escrito en un lenguaje interpretado requiere de un programa auxiliar (el intérprete), que traduce los comandos de los programas según sea necesario.

Interpretado vs. Compilado:
Un programa escrito en un lenguaje compilado posee la ventaja de no necesitar un programa anexo para ser ejecutado una vez que ha sido compilado, entonces se vuelve más rápido.
Sin embargo, no es tan flexible como un programa escrito en lenguaje interpretado, ya que cada modificación del archivo fuente (el archivo comprensible para los seres humanos: el archivo a compilar) requiere de la compilación del programa para aplicar los cambios.

Entorno de desarrollo integrado:
Abarcan e integran varias herramientas para el desarrollo de software en una sola aplicación (editor de código, compilador/intérprete, depurador y en muchos casos soporte para control de versiones).

* Programación por Bloques
Es una forma de aprender y desarrollar software donde se utilizan piezas visuales (como bloques de legos) en vez de usar códigos escritos.
En la programación tradicional, para mostrar un mensaje en pantalla escribirías algo como print("¡Hola, mundo!"). En la programación por bloques, arrastras un bloque que dice "decir" y le escribes dentro "¡Hola, mundo!".

---

## 2. Ejercicio con Estructura Secuencial

* Planteamiento del Problema
Realice un programa que, tomando una cantidad de tiempo expresada en horas, la transforme a su equivalente en días, minutos y segundos.

* Diagrama de flujo
  
<img width="1147" height="710" alt="codigo c" src="https://github.com/user-attachments/assets/e86b6233-5fc9-42b7-bce4-af5f43c8c01e" />


#### Código en C
```c
#include <stdio.h>

int main() {
    //VARIABLES
    float horas, dias, minutos, segundos;
    
    //DATOS
    printf("Ingrese la cantidad de tiempo en horas: ");
    scanf("%f", &horas);

    //PROCESO
    dias = horas / 24;         
    minutos = horas * 60;       
    segundos = horas * 3600;   

    //SALIDA
    printf("%f horas equivalen a:\n", horas);
    printf("%f dias\n", dias);
    printf("%f minutos\n", minutos);
    printf("%f segundos\n", segundos);

    return 0;
}
