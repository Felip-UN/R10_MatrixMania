# R10_MatrixMania
## Resumen de Repositorio
El presente repositorio tiene como finalidad realizar las actividades del reto numero 10 de clase entre las cuales se incluye:
1. Suma/Resta de matrices
2. Producto de matrices
3. Matrices transpuestas
## Programas
### Creador de matrices
Para cumplir con los retos pero trambien cumplir con que el codigo sea reutilizable creé un programa que permite crear matrices con n filas y n columnas
```python
filas=int(input("cuantas filas tiene?: "))
columnas=int(input("cuantas columnas tiene?: "))
A=[] #Matriz vacia
for fil in range(filas):
  while True: #Bucle convencional, para agrenas una n cantidad de filas de la matriz
    An=list(map(float, input("Valores en la fila:").split(" ")))
    #^^Split separara los numeros, map los convertira en flotantes y list los convertira en una lista
    if len(An) == columnas:
      #^^La cantidad de elementos EN la lista debe ser igual al a cantidad de columnas
      A.append(An) #Agregamos la fila a la matriz A
      break # Rompemos el bucle para no agregar mas cosas
    else: print("Cantidad de valores incorrecta intenta nuevamente") #Se repetira el bucle sin agregar nada
print(A)
```
La unica condicion para que se ejecute correctamente es separar los numeros con 1 espacio (' ') ejemplo: '2 3 5 6' 
