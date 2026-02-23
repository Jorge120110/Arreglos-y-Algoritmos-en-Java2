# Pseudocodigo y algoritmo

Pseudocodigo:

```java
Algoritmo EncontrarSegundos
    Entrada: Arreglo de enteros 'nums'
    
    // Paso 1: Inicialización con valores extremos
    max1 <- -Infinito, max2 <- -Infinito
    min1 <- +Infinito, min2 <- +Infinito
    
    // Paso 2: Recorrido único del arreglo
    Para cada número 'n' en nums Hacer:
        
        // Lógica para los mayores
        Si n > max1 Entonces:
            max2 <- max1
            max1 <- n
        Sino Si n > max2 Y n != max1 Entonces:
            max2 <- n
        Fin Si
        
        // Lógica para los menores
        Si n < min1 Entonces:
            min2 <- min1
            min1 <- n
        Sino Si n < min2 Y n != min1 Entonces:
            min2 <- n
        Fin Si
        
    Fin Para
    
    // Paso 3: Retornar resultados
    Escribir "Segundo Mayor:", max2
    Escribir "Segundo Menor:", min2
```

## Explicacion:

El algoritmo evalua el arreglo con funciones if, recorre los valores y toma el primero como valor absoluto "max1" cuando encuentra un valor que supere a este, pasa a ser el mayor, el nuevo no se descarta si no que pasa a ser el "max2", cuando encuentra un numero que no es el mayor de todos, evalua si es mayor que el segundo numero, si lo es, pasa a ser el, el segundo. 

Para los numeros menores, utiliza la misma logica pero al contrario, evalua los numeros y compara si el nuevo numero encontrado es menor al actual, si lo es, pasa a ser el mas pequeño, si no lo es, se evalua contra el segundo, si es mas pequeño que ese, pasa a ser el segundo mas pequeño.

## Análisis de complejidad:

### Tiempo (Notación O)

En este algortimo la complejidad del tiempo es "O(n)" ya que, al ser un ciclo que recorre un arreglo una unica vez, su tiempo de ejecucion durara "O(n)" directamente proporcional a la cantidad de "n" elementos que tenga nuestro arreglo.

### Espacio (Notación O)

En el algoritmo, la complejidad del espacio es de "O(1)", porque, no importa la cantidad de elementos que contenga nuestro arreglo, el espacio en memoria que utilice siempre sera el mismo (el espacio utilizado por las 4 variables temporales para guardar los numeros maximos y minimos)
