# Listicas__y_mass...!
Veremos las listas y todo lo relacionado con ellas.
## Punto 1:
- Desarrollar un algoritmo que calcule el promedio de un arreglo de reales.
### Explicación: ###
- creamos el arreglo luego use un ciclo for para que los dgitos de el arreglo se sumaran luego cree otra variable la cual era el promedio con su respectivo procedimiento y luego imprimi. Hice uso de el len para saber cuantos digitos y usarlo para usar toos los digitos de el arreglo.
```
#Inicializamos el arreglo(lista)
arreglo= [3.5, 6.7, 1.23, 2.34, 4.567, 34.5, 34.2, 3.98, 3.4]
#inicializamos la variable para poder sumar los valores de la lista
suma= 0

for digito in arreglo: # Usamos ciclo for para que todos los valores de la lista se sumen
    suma += digito
#Inicializamos la variable promedio usando la formula que es la suma de todos lo variables dividida en la cantidad de variables
Promedio= suma / len(arreglo) # usamos len para que nos de la cantidad de valores que hay en la lista arreglos

print("Este es el promedio de arreglos:", Promedio)
```
## Punto 2:
- Desarrollar un algoritmo que calcule el producto punto de dos arreglos de números enteros (reales) de igual tamaño.
### Explicación: ###
-  Use los conceptos de len para tomar todos los argumentos y usando el ciclo for pude saacr el producto de las dos listas.
```
def productoPunto(lista1, lista2):# tomamos dos listas como argumentos
    productoPunto= 0
    for i in range(len(lista1)): # usamos un for para que pase por todos los digitos de las listas y usamos como refencia la lista 1 ya que deben tener la misma cantidad de digitos 
      productoPunto += lista1[i]*lista2[i]
    return productoPunto 
n= [1.2, 3.6, 4.7, 2.7]
m= [4.6, 2.4, 1,6, 6.9]
print("Este es sun producto punto de sus listas:", productoPunto(n,m))
```
## Punto 3:
- Hacer un algoritmo que deje al final de un arreglo de números todos los ceros que aparezcan en dicho arreglo.
### Explicación: ###
- Aqui tuve que buscar omo se cambiaba las pocisiones en un arreglo para poder realizarlo, pero en si hice lo mismo inicialice una variable en o para luego se guardara alli la cantidad de 0 que habia y asi poder identificar en el arreglo cuales eran y cambiarlos de posicion.

```
#arreglo que deja todo los ceros a lo ultimo
def cero_en_arreglo(arreglo: list):
    contadordeceros= 0 #inicializamos el contador en 0
    for i in range(len(arreglo)): #creamos el ciclo for para que pase a través de todo el arreglo
        if arreglo[i]!= 0: #creamos la condición donde si el elemento no es 0
            arreglo[i - contadordeceros] = arreglo[i]# cambiamos la pocision de elemento que no es 0 hacia la izquierda
        else:
            contadordeceros +=1 #se tiene que subir uno el contador de 0
    for i in range(contadordeceros):
        arreglo[len(arreglo)-i-1] = 0 #arr[len(arr)-i-1] con esta formula se accede a las ultimas pocisiones lo que ayudara a que el 0 se acomode en las ultimas pocisiones
    return arreglo

arreglo= [3,0,6,0,4,0,1,0,3,5,0,76] # damos el arreglo
print("este es el arreglo original:", arreglo)
print()
arreglo= cero_en_arreglo(arreglo) #limpiamos y decimos cual es el nuevo arreglo
print("Este es el arreglo organizado:", arreglo)
        
```
