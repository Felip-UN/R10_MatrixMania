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
    An=list(map(float, input("Valores en la fila: ").split(" ")))
    #^^Split separara los numeros, map los convertira en flotantes y list los convertira en una lista
    if len(An) == columnas:
      #^^La cantidad de elementos EN la lista debe ser igual al a cantidad de columnas
      A.append(An) #Agregamos la fila a la matriz A
      break # Rompemos el bucle para no agregar mas cosas
    else: print("Cantidad de valores incorrecta intenta nuevamente") #Se repetira el bucle sin agregar nada
print(A)
```
La unica condicion para que se ejecute correctamente es separar los numeros con 1 espacio (' ') ejemplo: '2 3 5 6' 

### Suma!
Segun lo visto en el enlace proporcionado el valor con una posicion x,y establecida se sumara con otro con una poscision x,y igual y se agregara
```python
suma=[]
for f in range(filas): 
    suma.append([0]*columnas) 
    #^^Se agregara una fila de ceros con la misma cantidad de columnas que la matriz
    for c in range(columnas):
        suma[f][c]=A[f][c]+B[f][c] #poscision: f=fila c=columna o de otra manera: lista -> indexacion de la lista
        #^^se reemplazara la poscision de los ceros con los valores que se suman en esa misma poscision
```
Se me complico mas de lo que me gustaria admitir y doy credito a el [Gitbook]([https://material-docente.gitbook.io/parte-practica-informatica-para-ingenieria](https://material-docente.gitbook.io/parte-practica-informatica-para-ingenieria/practica-6.-matrices.-conjuntos/matrices-suma-y-multiplicacion)) de practica-informatica-para-ingenieria, el cual empeze a analizar para saber como interpretarlo, fue realmente ingenioso el crear una fila de ceros para unicamente reemplazar esos valores especificos sin mas rodeos

[Gitbook]([https://material-docente.gitbook.io/parte-practica-informatica-para-ingenieria](https://material-docente.gitbook.io/parte-practica-informatica-para-ingenieria/practica-6.-matrices.-conjuntos/matrices-suma-y-multiplicacion))

**Entradas(Creador de matrices):** 

Matriz 1:

Valores en la fila: 1 2 3 <-Esto es una cadena

Valores en la fila: 1 3 4

Valores en la fila: 5 6 7

Valores en la fila: 2 3 4 5 <-Caso de error

Cantidad de valores incorrecta intenta nuevamente <-Salida de error

Valores en la fila:12 3 4

[[1.0, 2.0, 3.0], [1.0, 3.0, 4.0], [5.0, 6.0, 7.0], [12.0, 3.0, 4.0]]

Matriz 2:

Valores en la fila: 1 2 3

Valores en la fila: 1 2 3

Valores en la fila: 2 3 4

Valores en la fila: 3 4 5

[[1.0, 2.0, 3.0], [1.0, 2.0, 3.0], [2.0, 3.0, 4.0], [3.0, 4.0, 5.0]]

**Salida (programa suma):**

[[2.0, 4.0, 6.0], [2.0, 5.0, 7.0], [7.0, 9.0, 11.0], [15.0, 7.0, 9.0]]


### Producto

