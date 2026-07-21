# Unidad 3

---

## Contenidos Teóricos

## Programación modular

La modularidad es una técnica de diseño de software que consiste en dividir un programa en partes más pequeñas, independientes y reutilizables llamadas módulos (funciones o procedimientos). Esto permite segmentar un problema complejo en subproblemas más sencillos de resolver, mejorando la legibilidad y el mantenimiento del código.
- Cuando tenemos algoritmos largos y complejos, una técnica para reducir la complejidad es dividir el programa grande en subprogramas pequeños (divide y vencerás).
- En programación, a esta técnica se la conoce como modularización (paradigma de programación). Estos módulos reciben el nombre de: procesos, funciones, rutinas, sub-rutinas, etcétera.

### Funciones

- ¿Qué es una Función?
      
Una función es un bloque de código autónomo diseñado para realizar una tarea específica. En lugar de escribir todo el código en la función principal (main), creamos funciones independientes que podemos "llamar" o invocar cada vez que las necesitemos. Esto evita la duplicación de código y facilita su mantenimiento.

- Estructura de una funcion
 1. No pueden ejecutarse por sí solas, estas deben estar ancladas a un programa principal (ejemplo main).
 2. Las funciones solicitadas por el main a su vez pueden llamar a otras funciones.

  <img width="1046" height="226" alt="Captura de pantalla 2026-07-16 115511" src="https://github.com/user-attachments/assets/8bf1525a-0d2c-4d3b-b80b-70cb3dac5081" />

- Funciones con Envío de Parámetros
  
Para que una función sea verdaderamente útil y dinámica, a menudo necesita recibir datos del exterior para trabajar con ellos. Estos datos que se le envían se conocen como parámetros (o argumentos).Al definir una función, especificamos en su cabecera qué tipo de datos espera recibir. Al invocarla, le enviamos los valores reales que procesará.C. Métodos de Envío de Parámetros   La forma en que el programa gestiona los datos que pasamos a las funciones es crucial. Existen dos métodos principales en C++:

1. Paso de Parámetros por Valor (Teoría y Ejemplo)

Teoría: En el paso por valor, la función recibe una copia del dato almacenado en la variable original. Esto crea una nueva variable en una zona de memoria distinta para uso exclusivo dentro de la función. Cualquier cambio o modificación que sufra esta variable dentro de la función no afectará en absoluto a la variable original del programa principal (main).  
¿Cuándo usarlo?: Se utiliza cuando solo necesitamos leer o procesar la información sin alterar la variable original.

 ### Ejemplo en C.
 - Contexto del problema
   
Crear un programa en C que simule el incremento de $5.00 a un precio base dentro de una función, verificando si la variable original del programa principal se modifica o no tras realizar la operación.

```c
#include <stdio.h>

// Función que recibe un parámetro por valor
void aumentarPrecio(float precio) {
    precio = precio + 5.0; // Se modifica únicamente la copia local
    printf("Dentro de la funcion (copia modificada): $%.2f\n", precio);
}

int main() {
    float precioOriginal = 20.0;
    
    printf("Antes de llamar a la funcion: $%.2f\n", precioOriginal);
    
    // Enviamos 'precioOriginal' por valor
    aumentarPrecio(precioOriginal); 
    
    // La variable original permanece intacta
    printf("Despues de la funcion (variable original): $%.2f\n", precioOriginal); 
    
    return 0;
}
```
### resultado del código en c

<img width="512" height="125" alt="Captura de pantalla 2026-07-16 155404" src="https://github.com/user-attachments/assets/496ec4e5-3bb6-4854-820f-4b6d117af719" />

2. Paso de Parámetros por Referencia (Teoría y Ejemplo en C)
   
En el lenguaje C estándar, el paso por referencia se emula utilizando punteros. En lugar de enviar el valor de la variable, enviamos su dirección de memoria usando el operador de dirección & en la llamada a la función. La función recibe esta dirección usando un puntero (declarado con el asterisco *). Al trabajar con punteros, la función accede y modifica directamente el valor almacenado en esa dirección física, por lo que cualquier cambio sí modificará de forma permanente la variable original en el main().

¿Cuándo usarlo?: Se utiliza cuando queremos que la función modifique directamente una o más variables externas, o cuando necesitamos retornar más de un valor desde una función.

 ### Ejemplo en C.
 - Contexto del problema
Crear un programa en C que aplique un descuento de $5.00 al precio de un producto dentro de una función, de tal manera que el cambio afecte directamente y de forma permanente a la variable original del programa principal.

```c
#include <stdio.h>

// Función que recibe un puntero (dirección de memoria)
void aplicarDescuento(float *precio) {
    // Usamos '*' para modificar el valor dentro de esa dirección de memoria
    *precio = *precio - 5.0; 
    printf("Dentro de la funcion (valor modificado directamente): $%.2f\n", *precio);
}

int main() {
    float precioOriginal = 20.0;
    
    printf("Antes de llamar a la funcion: $%.2f\n", precioOriginal);
    
    // Enviamos la direccion de memoria de 'precioOriginal' usando '&'
    aplicarDescuento(&precioOriginal); 
    
    // El valor original ha cambiado de forma permanente
    printf("Despues de la funcion (variable original): $%.2f\n", precioOriginal); 
    
    return 0;
}
```
### Prueba de escritorio

<img width="566" height="123" alt="Captura de pantalla 2026-07-16 155929" src="https://github.com/user-attachments/assets/fc65960c-2202-4e08-8b38-2b98ef3574cf" />

## Estructuras de Datos Estáticas Básicas
Las estructuras de datos estáticas son aquellas cuyo tamaño en memoria se define al momento de compilar el programa y no puede modificarse durante la ejecución del mismo. La estructura estática por excelencia es el arreglo (array), el cual almacena una colección de elementos del mismo tipo de forma contigua en memoria.

## Arrays
- La traducción de arreglos al inglés es arrays.
- Cada dato que forma parte del arreglo se denomina elemento.
- Los arreglos ofrecen una estructura que facilita el acceso a los elementos (índices)

## Arreglos Unidimensionales
- Solo tiene una fila y columnas, llamados vector o lista.
  
<img width="1105" height="115" alt="Captura de pantalla 2026-07-16 120514" src="https://github.com/user-attachments/assets/4b04e738-0b2e-4e3f-a33a-e77338549ef7" />

- Las posiciones del arreglo son llamadas índices y siempre empiezan en cero.

Un arreglo unidimensional es una lista ordenada de elementos del mismo tipo de datos que se guardan bajo un único nombre. Para acceder o modificar cualquier elemento individual, se utiliza un único índice numérico encerrado entre corchetes []. En el lenguaje C, los índices siempre comienzan en 0 y terminan en N-1 (donde $N$ es el tamaño del arreglo).

¿Cuándo usarlo?: Se utiliza para almacenar listas simples de datos, como una lista de calificaciones, nombres, temperaturas diarias o precios.
### Ejemplo en C.
```c
#include <stdio.h>

int main() {
    // Declaración e inicialización de un vector de 5 notas
    int notas[5] = {15, 18, 14, 20, 17};
    
    printf("--- NOTAS DE ESTUDIANTES (Arreglo Unidimensional) ---\n");
    
    // Recorrido del arreglo usando un solo bucle 'for'
    for (int i = 0; i < 5; i++) {
        printf("Estudiante [%d] - Nota: %d\n", i + 1, notas[i]);
    }
    
    return 0;
}
```
###  Prueba de escritorio
<img width="495" height="130" alt="Captura de pantalla 2026-07-16 160621" src="https://github.com/user-attachments/assets/31420242-1dbb-4723-8bfa-b22ce41c0f13" />

### Arreglos Bidimensionales
Un arreglo bidimensional es una estructura de datos organizada en una rejilla bidimensional de filas y columnas (se asemeja a una tabla o cuadrícula matemática). Para acceder a un elemento en particular, se requieren obligatoriamente dos índices: el primero representa la fila [fila] y el segundo representa la columna [columna].
 - Cuando tienen varias filas y columnas, llamados también matiz.
<img width="670" height="275" alt="Captura de pantalla 2026-07-16 161011" src="https://github.com/user-attachments/assets/92ec4ee8-96db-4b92-abb1-a5c4d3bfdae4" />

- La representación es m[i][j], donde i es el número de filas y j número de columnas.
  
<img width="631" height="348" alt="Captura de pantalla 2026-07-16 161036" src="https://github.com/user-attachments/assets/e4ccdc08-d631-47a1-b4bf-6c7d6c24ce4d" />

### Ejemplo en C.
```c
#include <stdio.h>

int main() {
    int lista[3][2];
    
    printf("INGRESO DE DATOS\n");
    for (int filas = 0; filas < 3; filas++) {
        for (int columna = 0; columna < 2; columna++) {
            printf("Ingresa el valor para la posicion %d , %d: ", filas, columna);
            scanf("%i", &lista[filas][columna]);
        }
    }

    printf("\nMATRIZ DISEÑADA:\n");
    for (int filas = 0; filas < 3; filas++) {
        
        printf("[ "); 
        
        for (int columna = 0; columna < 2; columna++) {
            printf(" %d ", lista[filas][columna]); 
        }
        
        printf(" ]\n"); 
        
    }

    return 0;
}
```
###  Prueba de escritorio
<img width="437" height="270" alt="Captura de pantalla 2026-07-16 161413" src="https://github.com/user-attachments/assets/55c25d80-7a11-464e-8ec1-43752a02ca6f" />

### Arreglos Multidimensionales
Son arreglos que poseen tres o más dimensiones. El caso más común es el de tres dimensiones (arreglo tridimensional), que se puede conceptualizar físicamente como un cubo de datos o un conjunto de matrices superpuestas (capas). Para acceder a un elemento se requieren tres índices: [capa], [fila] y [columna].
- Cuando tenemos varias filas,  columnas, y de profundidad.
- La representación es m[i][j][k], donde i es la profundidad, j el número de filas y k el número de columnas.
  
<img width="537" height="275" alt="Captura de pantalla 2026-07-16 161539" src="https://github.com/user-attachments/assets/a6d10bdb-a841-4b14-98d1-37b88e527ddb" />

### Ejemplo en C.
```c
#include <stdio.h>
int main(){

    int arreglos[2][2][3]; 
    
    printf("Ingrese los valores de La matriz: \n");
    for(int capa= 0; capa < 2; capa++){
        for(int filas = 0; filas < 2; filas++){
            for(int columna = 0; columna < 3; columna++){
                printf("Ingresa el valor para [capa %d] [filas %d] [Columna %d]: ", capa, filas, columna);
                scanf("%i", &arreglos[capa][filas][columna]);
            }
        }
    }

    printf("\nLa matriz diseñada es\n");
    for(int capa = 0; capa < 2; capa++){
        printf("CAPA %d:\n", capa); 
        for(int filas = 0; filas < 2; filas++){ 
            
            printf("[ "); 
            for(int columna = 0; columna < 3; columna++){
                printf(" %2d ", arreglos[capa][filas][columna]); 
            }
            
            printf(" ]\n"); 
        }
        printf("\n"); 
    }
    return 0;
}
```
###  Prueba de escritorio
<img width="517" height="490" alt="Captura de pantalla 2026-07-16 161935" src="https://github.com/user-attachments/assets/6ce19372-57ad-4413-969a-37f94edd1508" />

## Principales dificultades
La verdad es que me cuesta bastante entender la lógica de los arreglos bidimensionales y multidimensionales; coordinar los índices con tantos bucles for anidados se me hacía un lío y muchas veces terminaba accediendo a posiciones de memoria vacías o con errores. Además, cuando intentaba aplicar la modularidad en C, me confundía muchísimo el paso por referencia usando punteros con los asteriscos (*) y ampersands (&), ya que al mezclar funciones con arreglos muchas veces no sabía cómo estructurar el código ni qué parámetros colocar, lo que me causaba bloqueos y constantes errores en el compilador.

## Reflexión Crítica
Esta unidad me ha enseñado que programar en C requiere mucha paciencia y, sobre todo, planificar antes de escribir. Aunque me frustré bastante al inicio porque no me salían los códigos de funciones y matrices, me di cuenta de que no puedo codificar al azar sin entender primero cómo se mueve la memoria. Al final, comprender la modularidad y los arreglos me demostró que, aunque es difícil al principio, dividir un problema en partes más pequeñas es la única forma de crear programas ordenados y eficientes que realmente sirvan en mi carrera de Computación.

## Bibliografía 

Arteaga Martínez M. M. (2023). Lógica de programación con Pseint. Enfoque práctico (Primera edición). Fondo Editorial Remington. Disponible en: https://research.ebsco.com/linkprocessor/plink?id=0c1115b8-e552-38e4-bc75-bf84bbdd293f 

Guerra Salazar, J. E, Ramos Valencia,M. V, Vallejo Vallejo, G. E. (2023). Programando en C desde la práctica problemas resueltos. Puerto Madero Editorial. Disponible en: https://dialnet.unirioja.es/servlet/libro?codigo=933288 

Goin, M. (2022). Caminando junto al Lenguaje C. Editorail UNRN Disponible en: https://editorial.unrn.edu.ar/index.php/catalogo/346/view_bl/62/lecturas-de-catedra/26/caminando-junto-al-lenguaje-c?tab=getmybooksTab&is_show_data=1 

Guerra Salazar, J. E, Ramos Valencia,M. V, Vallejo Vallejo, G. E. (2023). Programando en C desde la práctica problemas resueltos. Puerto Madero Editorial. Disponible en: https://dialnet.unirioja.es/servlet/libro?codigo=933288 

## Conclusiones generales.
1. La modularidad en C es una herramienta clave que me ayuda a no repetir código y a tener programas mucho más limpios; aunque usar punteros y direcciones de memoria para el paso por referencia es complicado al principio, entiendo que es la mejor manera de optimizar el uso de los recursos de la computadora.
 
2. Los arreglos (desde los vectores simples hasta las matrices y arreglos multidimensionales) son indispensables para manejar grandes cantidades de datos bajo un solo nombre, permitiéndome organizar la información de forma lógica en lugar de usar variables individuales para todo.

3. El uso de cadenas de caracteres en C me enseñó que la memoria se maneja de forma muy estricta en este lenguaje, ya que al ser simplemente arreglos de tipo char, siempre se debe tener en cuenta el carácter nulo '\0' al final para evitar errores al mostrar o guardar textos.

## Declaracion del uso de IA
En cumplimiento con las directrices de la asignatura , declaro que utilicé herramientas de Inteligencia Artificial Generativa como tutor de acompañamiento. Su uso se limitó a resolver dudas conceptuales sobre la lógica de los punteros en C, estructurar de manera óptima y limpia los ejemplos de código planteados en el portafolio, y como apoyo para organizar mis ideas en la redacción de las dificultades y la reflexión crítica

---
<p align="center">
  <a href="../readme.md"> Volver a la Página Principal</a>
</p>
