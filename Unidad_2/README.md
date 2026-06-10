# Unidad 2

---

## Contenidos Teóricos

### Estructura Condicionales
Son usados para seleccionar “la ruta que debe tomar la ejecución de
instrucciones de un algoritmo/programa (tomas de decisiones)”

<img width="750" height="326" alt="Captura de pantalla 2026-06-09 160437" src="https://github.com/user-attachments/assets/8e7b63e8-2217-4e60-acd3-e8b4ce43626a" />

También llamada de alternativa o selectivas, permite en
función de una condición elegir un camino de ejecución.

## 1. Estructura Condicional Simple (Si ..Entonces)
<img width="766" height="282" alt="Captura de pantalla 2026-06-09 160914" src="https://github.com/user-attachments/assets/3c8e0533-9f97-4574-9ab7-6806c8669de9" />
Las estructuras condicionales simples son el primer paso para darle "cerebro" a nuestro código. Le permiten a un programa tomar decisiones básicas: si se cumple una condición, se hace algo; si no se cumple, simplemente se ignora y el programa sigue de largo.
<img width="512" height="436" alt="imagen06" src="https://github.com/user-attachments/assets/8335ff40-0346-43e0-a11a-792274bbf1e3" />

## 2. Estructura Condicional Doble (Si ..Entonces, Sino ..)

  La estructura condicional doble (también conocida como Si...Entonces...Sino) permite a un programa tomar decisiones, ofreciendo dos caminos distintos a seguir: uno si la condición resulta ser verdadera (o se cumple) y otro diferente si resulta ser falsa
  
  <img width="512" height="436" alt="imagen06" src="https://github.com/user-attachments/assets/89ee471e-7066-41f4-be38-e86b5c1a14f0" />

## 3. Estructura Condicional Múltiple (En caso de ....)
  
La Estructura Condicional Múltiple (conocida en pseudocódigo como "En caso de" o "Según", y en lenguajes de programación como switch o match) se utiliza cuando tienes una sola variable que puede tomar múltiples valores distintos y quieres ejecutar un bloque de código diferente para cada valor, sin tener que encadenar muchísimos Si... Sino... Si....

<img width="450" height="283" alt="foto035" src="https://github.com/user-attachments/assets/25483e95-f03f-4b7c-ac47-f8da8c5d4e6c" />

## 4. Anidamiento de estructuras de Condicionales

El Anidamiento de estructuras condicionales (o simplemente condicionales anidadas) ocurre cuando colocas una estructura condicional (Si... Entonces) dentro de otra estructura condicional.
Se utiliza cuando para tomar una decisión no basta con evaluar una sola condición, sino que, tras haber cumplido o fallado una primera condición, se requiere comprobar inmediatamente otra condición interna para determinar la acción exacta a realizar.

<img width="502" height="637" alt="foto036" src="https://github.com/user-attachments/assets/cf306621-d43c-4348-b790-2f9398a48563" />

5. Implementación de Estructuras Condicionales en Lenguaje de programación
  
Para implementar las tomas de decisiones en un lenguaje de programación, el compilador utiliza palabras reservadas en inglés que sustituyen los comandos lógicos del pseudocódigo y las bifurcaciones de los diagramas de flujo:  

## 5.1. Si se traduce e implementa como if.
   
   Condicional Simple (if)
Evalúa una condición booleana entre paréntesis. Si esta es verdadera (true), ejecuta las instrucciones que se encuentran dentro de las llaves {}. Si es falsa (false), el programa ignora por completo ese bloque.

## 5.2. Entonces se representa mediante la apertura de llaves { (que delimitan el bloque de instrucciones).
   
   Condicional Doble (if - else)
Se utiliza cuando el algoritmo cuenta con dos caminos de ejecución obligatorios. Cuando la condición del if resulta falsa, el flujo del programa se desvía inmediatamente a las instrucciones contenidas dentro del bloque else.

## 5.3. Sino se traduce e implementa como else
   
   Condicionales Anidadas (if dentro de otro if)
Su implementación consiste en colocar una estructura if o if-else completa dentro de las llaves de otra condición. Al programarlas, es un requisito de buena práctica mantener una correcta indentación (sangrado con la tecla Tabulador) para identificar visualmente a qué declaración pertenece cada llave de cierre.

## 5.4. Según / En caso de se traduce e implementa como switch.
   
   Condicional Múltiple (switch)
Es la traducción del "Según / En caso de". Evalúa una sola variable (que debe ser de tipo entero o carácter) y salta directamente hacia la etiqueta case que coincida de forma exacta con su valor.

## 6. Planteamiento del Problema
  
Un sistema para una tienda tecnológica debe procesar la compra de un artículo. El programa debe:
Solicitar el precio del artículo y la cantidad.
Calcular el total. Si la cantidad de artículos es mayor a 5, aplicar un descuento inicial del 10% (Condicional Simple).
Preguntar si el cliente tiene tarjeta de membresía VIP. Si la tiene, aplicar un 5% de descuento adicional, pero si el total con descuento quedó por debajo de $100, el descuento adicional será solo del 2% (Condicional Anidada dentro de una Condicional Doble).
Solicitar el método de pago (1. Efectivo, 2. Tarjeta de Crédito, 3. Transferencia) y aplicar una comisión o beneficio según el caso (Condicional Múltiple).

*Diagrama de flujo.
<img width="912" height="846" alt="Captura de pantalla 2026-06-09 174325" src="https://github.com/user-attachments/assets/2ef448aa-d543-46b5-81be-0e0ab068a86f" />

### Estructuras repetitivas

Las estructuras repetitivas permiten repetir un número determinado de veces un grupo de sentencias o instrucciones, o hasta que se cumpla una condición.
A estas estructuras se denomina bucle. Al hecho de repetir la ejecución de esta secuencia de instrucciones se le llama iteración, de donde viene el otro nombre de estas estructuras: Iterativas (Figueroa Piscoya et al, 2021).

## 1. Terminología Básica (Contadores y Acumuladores)

  Contadores.
Es una variable cuyo valor se incrementa sucesivamente de uno en uno por lo general. Debe ser inicializada en cero:

contador = contador + constante
persona = persona + 1
stock = stock - 3;

  Acumuladores.
Es una variable que acumula sucesivamente valores que pueden variar. Debe ser inicializada en cero:

acumulador = acumulador + variable;
suma = suma + edad
total = total – descuento

## 2. Estructura Mientras.
La Estructura Repetitiva "Mientras" (conocida en inglés y en la mayoría de los lenguajes de programación como el bucle while) es una estructura de control que permite ejecutar un bloque de instrucciones de forma cíclica o repetitiva mientras una condición determinada sea verdadera.  Su característica principal es que evalúa la condición al inicio, antes de entrar al bucle. Si la condición es falsa desde el primer intento, el bloque de código de su interior nunca se ejecutará.

<img width="752" height="713" alt="while" src="https://github.com/user-attachments/assets/bcb0e139-c850-4c07-aab8-601664ec20f5" />

## 3. Estructura Hacer .. Mientras (Repetir ..Hasta)

La Estructura Repetitiva "Hacer... Mientras" (conocida en pseudocódigo como "Repetir... Hasta" o "Hacer... Repetir", y en lenguajes de programación como el bucle do-while) es una estructura de control cíclica que ejecuta un bloque de instrucciones y, después de ejecutarlas, evalúa una condición para decidir si vuelve a repetir el ciclo.
Su característica fundamental y diferenciadora es que evalúa la condición al final. Esto garantiza que el bloque de código de su interior se ejecute al menos una vez, sin importar si la condición es verdadera o falsa desde el principio.

<img width="326" height="294" alt="repetir-hasta-que-diagrama-de-flujo" src="https://github.com/user-attachments/assets/b3ed43bb-cb34-43a5-92a5-16496d4273ef" />

## 4. Estructura Para.
  
La Estructura Repetitiva "Para" (conocida universalmente en los lenguajes de programación como el bucle for) es una estructura de control cíclica diseñada para situaciones donde se conoce de antemano el número exacto de veces que se debe ejecutar el bloque de instrucciones.
A diferencia de los bucles Mientras o Hacer... Mientras, que dependen puramente de una condición lógica que puede cambiar en cualquier momento, el bucle Para utiliza una variable de control (o contador) que se incrementa o decrementa de forma automática en cada vuelta hasta alcanzar un límite preestablecido.

  <img width="743" height="683" alt="for" src="https://github.com/user-attachments/assets/0977e07f-d724-4f1a-a617-ec32bf045531" />

## 5. Anidamiento de estructuras repetitivas

  El Anidamiento de estructuras repetitivas (también conocido como bucles anidados o nested loops) ocurre cuando se coloca una estructura repetitiva (Para, Mientras o Repetir) dentro del cuerpo de otra estructura repetitiva.
Cuando se programan bucles anidados, el bucle que está afuera se denomina bucle externo y el que está adentro se conoce como bucle interno.
Su regla de funcionamiento es estricta: por cada una de las vueltas que da el bucle externo, el bucle interno debe ejecutarse por completo (dar todas sus vueltas planificadas) antes de que el externo pueda avanzar a su siguiente iteración.

<img width="351" height="376" alt="Estructuras_de_decisi%3Fn_anidadas" src="https://github.com/user-attachments/assets/7a4f2ce3-da2e-41c3-9d82-ccca14f8176c" />

## 6. Implementación de Estructuras repetitivas en Lenguaje de programación
  
## 6.1. Bucle Basado en Condición Inicial (while)
Es la implementación directa de la estructura Mientras. Evalúa la condición booleana entre paréntesis antes de permitir cualquier acción. Si es verdadera, ejecuta el bloque de código entre llaves {} y vuelve a evaluar.

## 6.2. Bucle Basado en Condición Final (do - while)
Es la implementación de la estructura Hacer... Mientras (o Repetir... Hasta). Las instrucciones dentro del bloque do se ejecutan de forma obligatoria la primera vez. Al llegar a la llave de cierre, se evalúa el while; si la condición es verdadera, el flujo regresa al do.

## 6.3. Bucle Basado en Contador Determinado (for)
Es la implementación de la estructura Para. Es la estructura más compacta porque condensa la inicialización, la condición de parada y el incremento/decremento en una sola línea de cabecera, separados por puntos y comas (;).

###  Ejercicio con estructura condicional y repetitiva

## 2. Evidencia Práctica o Aplicación

### Planteamiento del problema
Se requiere desarrollar un programa en Lenguaje C para automatizar el control de un puesto de peaje vehicular que procesa un flujo determinado de autos por turno. El programa debe realizar lo siguiente:
1. Solicitar al operador la cantidad total de vehículos que cruzaron por la cabina en el turno.
2. Utilizar un ciclo iterativo para registrar los datos de cada vehículo de forma individual.
3. Solicitar el tipo de vehículo mediante un menú numérico: `1. Motocicleta`, `2. Automóvil`, `3. Camión`. Se debe validar mediante un bucle que el usuario ingrese una opción correcta; de lo contrario, mostrar un error y volver a pedirla.
4. Definir una tarifa base según el tipo: Motocicleta = $1.00, Automóvil = $2.50, Camión = $5.00.
5. Aplicar una condicional anidada para los Camiones: si el camión tiene más de 3 ejes, se le cobrará un recargo adicional de $1.50 por cada eje extra.
6. Al finalizar el turno, el programa debe desplegar estadísticas globales: el total de dinero recaudado en la cabina y el conteo exacto de cuántos vehículos de cada tipo fueron procesados.

### Análisis del problema

* **Entradas:**
  * Cantidad de vehículos en el turno (`total_vehiculos` - entero).
  * Tipo de vehículo (`tipo` - entero: 1, 2 o 3).
  * Cantidad de ejes si es camión (`ejes` - entero).
* **Procesos:**
  * Iterar desde 1 hasta `total_vehiculos` usando un bucle `for`.
  * Validar la opción del menú con un ciclo `do-while` para asegurar que `tipo` esté entre 1 y 3.
  * Determinar el costo base usando una estructura condicional múltiple (`switch`).
  * Aplicar una condicional anidada (`if`) si el tipo es camión para calcular el recargo por ejes extras (`ejes > 3`).
  * Acumular la recaudación (`total_recaudado += costo_vehiculo`) e incrementar los contadores individuales de cada categoría.
* **Salidas:**
  * Monto total recaudado en el peaje.
  * Cantidad total de motocicletas, automóviles y camiones atendidos.

### Diseño del algoritmo
<img width="630" height="786" alt="Captura de pantalla 2026-06-09 180312" src="https://github.com/user-attachments/assets/479f7605-68d7-49db-bce1-5751f56dd8b5" />

### Codificación (Lenguaje C)

```c
#include<stdio.h>

int main(){
    //Declaración de variables
    int total_vehiculos, tipo, ejes;
    int c_motos = 0, c_autos = 0, c_camiones = 0;
    float costo_vehiculo, total_recaudado = 0.0;

    //Entrada: Tamaño del flujo vehicular
    printf("Ingrese la cantidad de vehiculos a procesar en el turno: ");
    scanf("%d", &total_vehiculos);

    //Control de seguridad inicial en caso de turno vacío o negativo
    if(total_vehiculos <= 0){
        printf("[INFO] No se registraron vehiculos en este turno. Fin del programa.\n");
        return 0;
    }

    //ESTRUCTURA REPETITIVA PRINCIPAL: Ciclo para procesar cada vehículo
    for(int i = 1; i <= total_vehiculos; i++){
        printf("\n--- Procesando Vehiculo Nro. %d ---\n", i);

        //ESTRUCTURA REPETITIVA ANIDADA: Validación del tipo de vehículo (Hacer... Mientras)
        do{
            printf("Seleccione el tipo de vehiculo:\n");
            printf("1. Motocicleta\n");
            printf("2. Automovil\n");
            printf("3. Camion\n");
            printf("Opcion: ");
            scanf("%d", &tipo);

            if(tipo < 1 || tipo > 3){
                printf("[ERROR] Opcion no valida. Por favor, intente de nuevo.\n");
            }
        }while(tipo < 1 || tipo > 3); //Se repite si la opción está fuera del rango 1-3

        //ESTRUCTURA CONDICIONAL MÚLTIPLE: Asignación de tarifa base
        switch (tipo){
            case 1:
                costo_vehiculo = 1.00;
                printf("Tarifa: Motocicleta -> $%.2f\n", costo_vehiculo);
                c_motos++;
                break;
            case 2:
                costo_vehiculo = 2.50;
                printf("Tarifa: Automovil -> $%.2f\n", costo_vehiculo);
                c_autos++;
                break;
            case 3:
                costo_vehiculo = 5.00; // Tarifa base camión
                c_camiones++;
                
                printf("Ingrese la cantidad de ejes del camion: ");
                scanf("%d", &ejes);

                //CONDICIONAL ANIDADA (Dentro de la opción del camión)
                if(ejes > 3){
                    float recargo = (ejes - 3) * 1.50;
                    costo_vehiculo += recargo;
                    printf("Recargo aplicado por %d ejes extras: $%.2f\n", (ejes - 3), recargo);
                }
                printf("Tarifa Final Camion -> $%.2f\n", costo_vehiculo);
                break;
        }

        //Acumulador del dinero total de la estación
        total_recaudado += costo_vehiculo;
    }

    //Reporte Estadístico Final
    printf("\n=============================================\n");
    printf("          REPORTE DE CIERRE DE TURNO         \n");
    printf("=============================================\n");
    printf("Total de vehiculos atendidos: %d\n", total_vehiculos);
    printf("Cantidad de Motocicletas: %d\n", c_motos);
    printf("Cantidad de Automoviles: %d\n", c_autos);
    printf("Cantidad de Camiones: %d\n", c_camiones);
    printf("---------------------------------------------\n");
    printf("TOTAL RECAUDADO EN CAJA: $%.2f\n", total_recaudado);
    printf("---------------------------------------------\n");

    return 0;
}
```
<img width="1057" height="690" alt="Captura de pantalla 2026-06-09 180040" src="https://github.com/user-attachments/assets/843edf85-6629-4605-833b-fa7267888870" />


### Validación (Prueba de Escritorio Basada en Ejecución Real)

La siguiente tabla representa la traza lógica de la ejecución real del programa (captura de pantalla adjunta), procesando un lote de **2 vehículos**:
* **Vehículo 1:** Automóvil (`tipo = 2`, Tarifa: $2.50).
* **Vehículo 2:** Motocicleta (`tipo = 1`, Tarifa: $1.00).

| Ciclo / Acción | total_vehiculos | variable `i` | variable `tipo` | ¿`tipo` inválido? | variable `ejes` | `costo_vehiculo` | `total_recaudado` | Contadores (`c_motos`, `c_autos`, `c_camiones`) | Pantalla / Salida (printf) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| Inicialización | 2 | - | - | - | - | - | 0.0 | 0, 0, 0 | "Ingrese la cantidad de vehiculos..." |
| **Iteración 1** | 2 | 1 | 2 | No (Falso) | - | 2.50 | **2.50** | 0, **1**, 0 | "Tarifa: Automovil -> $2.50" |
| **Iteración 2** | 2 | 2 | 1 | No (Falso) | - | 1.00 | **3.50** | **1**, 1, 0 | "Tarifa: Motocicleta -> $1.00" |
| Fin del Bucle | 2 | (Termina) | - | - | - | - | 3.50 | 1, 1, 0 | *El ciclo `for` finaliza al alcanzar el límite de 2* |
| Impresión Final | 2 | - | - | - | - | - | 3.50 | 1, 1, 0 | **TOTAL RECAUDADO EN CAJA: $3.50** |

### Principales dificultades y reflexión crítica en la aplicación de los contenidos.
## 3. Principales Dificultades y Reflexión Crítica

### Principales Dificultades Encontradas

Al momento de pasar la teoría al código real en Lenguaje C, me topé con varios problemas prácticos, especialmente al trabajar con las estructuras repetitivas:

1. **Confusión con los límites en el bucle `for`:**
   Mi mayor problema con el `for` fue controlar exactamente cuándo debía detenerse el ciclo. A veces me confundía entre usar `<` o `<=`, lo que hacía que el programa diera una vuelta de más o una vuelta de menos (procesando de forma incorrecta la cantidad de vehículos del lote). También me costó un poco acostumbrarme a poner toda la configuración (inicialización, condición e incremento) en una sola línea separada estrictamente por puntos y comas (`;`).

2. **La lógica invertida del `do-while` para validar datos:**
   Esta fue la estructura que más me costó entender. Al programar el menú de opciones, yo tendía a pensar en la condición para los datos que *sí* eran correctos, cuando en realidad el `do-while` en C funciona al revés para las validaciones: se debe quedar repitiendo **mientras la condición de error sea verdadera** (por ejemplo, mientras el usuario ponga un número menor a 1 o mayor a 3). Cambiar mi lógica a esta forma de pensar me tomó varios intentos fallidos donde el bucle se me cerraba antes de tiempo o se volvía infinito.

3. **Olvidar el punto y coma final en el `do-while`:**
   Como venía acostumbrado al `if` y al `for` que no llevan punto y coma al final de sus llaves, me pasaba muy seguido que olvidaba poner el `;` después del paréntesis del `while` en el cierre del `do-while`. Esto me generaba errores de sintaxis que el compilador a veces no explicaba bien y me costaba encontrar el fallo.

### Reflexión Crítica

Aprender a usar bucles junto con condicionales me hizo dar cuenta de que la programación no es solo hacer que el código corra, sino también protegerlo de los errores del usuario. 
Antes de esta unidad, mis programas se rompían si el usuario ingresaba un número que no correspondía. Al meter un `do-while` dentro de un `for`, logré "blindar" el código para que nadie pueda ingresar datos falsos o erróneos antes de que los condicionales (`switch` o `if-else`) hagan sus cálculos. Esto me demostró que en Computación cada operador lógico y cada signo cuentan. 
La prueba de escritorio y revisar mi propia captura de pantalla me sirvieron muchísimo para entender qué es lo que pasa realmente en la memoria de la computadora en cada vuelta del ciclo, ayudándome a conectar la teoría de la materia con la práctica real.

### Bibliografía 

* Arteaga Martínez M. M. (2023). Lógica de programación con Pseint. Enfoque práctico (Primera edición). Fondo Editorial Remington. Disponible en: https://research.ebsco.com/linkprocessor/plink?id=0c1115b8-e552-38e4-bc75-bf84bbdd293f 
* Bhuiyan, A. A., & Amiruzzaman, M. (2025). Programming with Java (2nd ed.). The Pennsylvania Alliance for Design of Open Textbooks (PA-ADOPT). Disponible en: https://open.umn.edu/opentextbooks/textbooks/programming-with-java 
* Guerra Salazar, J. E, Ramos Valencia,M. V, Vallejo Vallejo, G. E. (2023). Programando en C desde la práctica problemas resueltos. Puerto Madero Editorial. Disponible en: https://dialnet.unirioja.es/servlet/libro?codigo=933288 
* Toro Bonilla, J. M. (2023). Fundamentos de programación: Python (2.ª ed.). Editorial Universidad de Sevilla. Disponible en: https://dialnet.unirioja.es/servlet/libro?codigo=871117 


## Declaracion del uso de IA

"Para este trabajo utilicé la IA principalmente como un asistente de desarrollo y co-piloto de código. Me sirvió para estructurar la lógica de las condiciones en Lenguaje C, corregir errores de sintaxis en los bucles for y do-while que me daban problemas al compilar, y automatizar el diseño del diagrama de flujo en PlantUML para draw.io. Además, me ayudó a organizar la prueba de escritorio en una tabla limpia de Markdown basada exactamente en los datos de mi captura de pantalla real, asegurándome de que todo el documento mantenga el formato profesional que exige el portafolio."
