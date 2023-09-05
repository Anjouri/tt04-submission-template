![](../../workflows/gds/badge.svg) ![](../../workflows/docs/badge.svg) ![](../../workflows/wokwi_test/badge.svg)

# Demultiplexor NAND


## Autores: 
 Mauricio Caballero Hernández - Alejandro Duran Morales - Marvin Yahir Salamanca Ramirez - Kevin Ortiz Sarate


### Descripcion:
 Demultiplexor de 3 entradas independientes y 3 entradas de dirección que arrojan valore logicos de 0 y 1 en 8 salidas diferentes, constituido por compuertas NAND y NOT, imitando el comportamiento de un LS138


### How does it work?
 Introduciendo un total de 6 señales en el circuito se puede arrojar una señal negada (un valor de 0 logico) en una de las 8 salidas 
 disponibles. 
 Las primeras 3 entradas dentro del circuito son clasificadas como entradas de dirección y se encargan de configurar el Demultiplexor, 
 los 
 otros 3 puertos de entrada admiten valores de entrada independientes que terminan por infliur en las entradas de las compuertas logicas 
 NAND y eso enconjunto permite que se arrojen valores logicos, predominando los estados altos en 7 de 8 salidas, mientras que la salida 
 restante arroja un valor logico de 0 (lo cual admite un total de 8 combinaciones posibles con resultados diferentes). 
 Todo el cuerpo del Demultiplexor esta conformado por compuertas NAND de 4 entradas y su demanda de compuertas NOT es minima en 
 comparacion.


### How to test?
 Para probar el circuito es necesario utilizar un dip switch de 6 entradas donde las primeras 3 posiciones conformaran las entradas
 de dirección (E0-E2) mientras que las posiciones 4 a 6 seran las entradas independientes (A0-A2).
 En su estado natural, (sin señales de entrada más que la E0), se arrojara el estado bajo a O0, 
 Para arrojar un valor de 0 a la salida O1 es necesario mantener activa la entrada de direccion E0 y la entrada independiente A0. 
 Para cambiar a la salida O2 se mantiene la entrada de dirección E0 y la entrada A1.
 Para cambiar a la salida O3 se mantiene la entrada de dirección E0 y la entrada A0 + A1.
 Para cambiar a la salida O4 se mantiene la entrada de dirección E0 y la entrada A2.
 Para cambiar a la salida O5 se mantiene la entrada de dirección E0 y la entrada A0 + A2.
 Para cambiar a la salida O6 se mantiene la entrada de dirección E0 y la entrada A1 + A2.
 Para cambiar a la salida O7 se mantiene la entrada de dirección E0 y la entrada A0 + A1 + A2.
 Para que todas las salidas arrojen un valor logico de 1 se necesita que se activen las entradas E1 + E2.



### Inputs
  - E0 (Entrada de dirección)
  - E1 (Entrada de dirección)
  - E2 (Entrada de dirección)
  - A0 (Entrada independiente)
  - A1 (Entrada independiente)
  - A2 (Entrada independiente)


### Outputs
  - segment a
  - segment b
  - segment c
  - segment d
  - segment e
  - segment f
  - segment g
  - dot

