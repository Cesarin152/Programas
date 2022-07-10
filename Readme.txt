
La libreria de cktotrifasico() tiene 2 funciones las cuales son
•	fallat(y_ad,uk_n,v_b) “Para falla trifásica” 
•	fallalt(y_ad0,y_ad1,y_ad2,uk_n,v_b) “Para falla línea a tierra”

y_ad: Es la matriz de admitancia.
Uk_n: Nodo donde ocurre la falla “Recibe un numero entero el cual es el nodo donde ocurre la falla”.
V_b: Lista {} de Voltajes antes de la falla, pueden ser un solo valor de voltaje el cual 
lo considera como el voltaje para todos los nodos, o n cantidad de voltajes para cada nodo.
y_ad0: Es la matriz de admitancia la secuencia 0.
y_ad1: Es la matriz de admitancia la secuencia 1 o positiva.
y_ad2: Es la matriz de admitancia la secuencia 2 o negativa. 

Sistema con 3 nodos y se desea conocer la falla trifásica en el nodo 2.
Fallat(matriz_de_admitancia,2,{VAF1,VAF2,VAF3})
Si es el método aproximado seria:
Fallat(matriz_de_admitancia,2,{VAF})

Sistema con 2 nodos y se desea conocer la falla línea a tierra en el nodo 1.
Fallalt(matriz_de_admitancia0, matriz_de_admitancia1, matriz_de_admitancia2,1,{VAF1,VAF2,VAF3})
Si es el método aproximado seria:
Fallalt(matriz_de_admitancia0, matriz_de_admitancia1, matriz_de_admitancia2,1,{VAF})

Para invocar las funciones a utilizar seria:
cktotrifasico():fallat(y_ad,uk_n,v_b)
cktotrifasico():fallalt(y_ad0,y_ad1,y_ad2,uk_n,v_b)

PD: El programa funciona para n cantidad de nodos, aparte tiene la 
capacidad de saber cuantos nodos hay presente sin la necesidad de especificarlo. 
Tenga en cuenta que el programa usa todos los decimales por lo que la respuesta 
si se hace a mano puede ser levemente diferente y puede considerarse imperceptible.
®All rights reserved
