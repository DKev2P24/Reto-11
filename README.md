# Reto-11
## Suma/Resta de Matrices
```python
def mts1(p, z): # Funcion que genera la primera matriz
    m1 = []     # lista que acumula los valores de filas y columnas
    for i in range(p):   # recorrer dentro de los valores dados
        f1 = [] 
        for j in range(z):
            fp = int(input(f"Introduce la coordenada A{i + 1},{j + 1}: ")) # se solicitan los valores de la matriz
            f1.append(fp) # se agregan los valores ingresados a una lista
        m1.append(f1) # se agrega una lista a otra lista 
    return m1 # entrega la matriz 1

def mts2(p, z): # Funcion que genera la segunda matriz
    m2 = []
    for i in range(p):
        f1 = []
        for j in range(z):
            fp = int(input(f"Introduce la componente B{i + 1},{j + 1}: ")) # se solicitan los valores de la segunda matriz
            f1.append(fp)
            f1.append(fp)
        m2.append(f1)
    return m2

def sum(p, z):         # Funcion que opera las matrices ingresadas
    m = []      # lista que acumula los valores de la suma
    for i in range(len(p)):      # recorre las filas de las matrices
        t = []       # lista para almacenar las filas
        for j in range(len(p)):      # se recorre las columnas de las matrices
            v = p[i][j] + z[i][j]      # se opera cada elemento de cada fila y columna
            t.append(v)      # se agregan a la lista los valores de las filas
        m.append(t)        # se agregan los valores a la matriz
    return m        # entrega la matriz

def rest(p, z):     # Funcion que resta las matrices ingresadas
    m = []      # lista que acumula los valores de la resta
    for i in range(len(p)):      # recorre las filas de las matrices
        t = []       # lista para almacenar las filas
        for j in range(len(p[i])):      # se recorre las columnas de las matrices
            v = p[i][j] - z[i][j]      # se resta cada elemento de cada fila y columna
            t.append(v)      # se agregan a la lista los valores de las filas
        m.append(t)        # se agregan los valores a la matriz
    return m        # entrega la matriz resta

def im(x): # Funcion Muestra Matriz
    for i in x:  
        print(i)  # Imprime cada fila ordenada de la matriz
        
if __name__ == "__main__":
    f = int(input("Filas: "))
    c = int(input("Columnas: ")) # Entrada de Valores de las Matrices
    mat1 = mts1(f, c)
    mat2 = mts2(f, c) # se llaman a las funciones de Matrices
    mat3 = sum(mat1, mat2)
    mat4 = rest(mat1, mat2) # se llaman a las funciones operadoras de matrices
    print("Matriz 1:",) # se imprimen las matrices ingresadas y sus respectivas operaciones entre ellas
    im(mat1)
    print("Matriz 2:")
    im(mat2)
    print("Matriz Suma:")
    im(mat3)
    print("Matriz Retsa:")
    im(mat4)
```
## Producto de matrices
```python
def mts1(p, z): # se genera la matriz 1
    m1 = []
    for i in range(p):
        f1 = []
        for j in range(z):
            fp = int(input(f"Introduce la coordenada A{i + 1},{j + 1}: "))
            f1.append(fp)
        m1.append(f1)
    return m1

def mts2(p, z): # se genera la matriz 2
    m2 = []
    for i in range(p):
        f1 = []
        for j in range(z):
            fp = int(input(f"Introduce la componente B{i + 1},{j + 1}: "))
            f1.append(fp)
        m2.append(f1)
    return m2

def m(p, z):   # funcion que opera las matrices para multiplicarlas
    m = []  # se acumulan los valores
    for i in range(len(p)):  # se recorre cada elemento 
        t = [] # se acumulan las filas 
        for j in range(len(p[i])):  # se recorre cada elemento  
            v = p[i][j] * z[i][j]  # se multiplica cada elemento de cada fila y columna 
            t.append(v)  # se agregan los valores a la lista de filas
        m.append(t)  # se agregan los valores a la matriz
    return m  # regresa la matriz producto

def im(x): # Funcion Muestra Matriz
    for i in x:
        print(i)  # Imprime cada fila ordenada de la matriz
        
if __name__ == "__main__":
    f = int(input("Filas: "))
    c = int(input("Columnas: "))
    mat1 = mts1(f, c)
    mat2 = mts2(f, c)
    mat4 = m(mat1, mat2) # se llama a la funcion de producto de matrices
    print("Matriz 1:")
    im(mat1)
    print("Matriz 2:")
    im(mat2)
    print("Matriz Producto:")
    im(mat4) # se imprime la matriz resultado del producto
```
## Matriz Transpuesta
```python
def m(m,n):
    k = []
    for i in range(m):
        l = []
        for j in range(n):
            mx = int(input(F"Coordenada F({j+1},{i+1})C: ")) # se intercambian las posiciones de "i" y "j"
            l.append(mx)
        k.append(l)
    return k

def z(m): # funcion que imprime la matriz transpuesta
    for i in range(len(m)): 
         print(m[i]) # se imprime cada fila para cambiar la apariencia respecto a la matriz original

if __name__ == "__main__":
    f = int(input("Columnas: ")) # se ingresan los datos de la matriz
    c = int(input("Filas: "))
    ko = m(f,c) # se llama a la funcion de transposicion
    z(ko) # se imprime la matriz transpuesta
```
## Suma de Columna 
```python
def m(m,n):
    k = []
    for i in range(m):
        l = []
        for j in range(n):
            mx = int(input(F"Coordenada F({i+1},{j+1})C: ")) 
            l.append(mx)
        k.append(l)
    return k

def k(n,o): # funcion que separa los valores de columna indicada, del resto de la matriz
    p = 0
    for i in n:
         p += i[o]
    return p # regresa una lista con los valores de columna

def l(m): # funcion que imprime la matriz
    for i in m:
     print(i) 

if __name__ == "__main__": 
    f = int(input("Columnas: ")) # se ingresan los datos de la matriz
    c = int(input("Filas: "))
    a = int(input("Columna a sumar: ")) - 1 # se solicita la columna a sumar
    mt = m(c,f) # se llama a la funcion de generacion de matriz
    r = k(mt,a) # se llama a la funcion que suma la columna
    print("Matriz:") 
    l(mt) # se imprime la matriz
    print(f"Suma de columna: {r}") # se imprime la suma de la columna
```
## Suma de Fila
```python
def m(m,n): # funcion que genera la matriz
    k = []
    for i in range(m):
        l = []
        for j in range(n):
            mx = int(input(F"Coordenada F({i+1},{j+1})C: "))
            l.append(mx)
        k.append(l)
    return k

def k(n,o): # funcion que separa los valores de la fila indicada, del resto de la matriz
    p = 0
    for i in n[o]:
        p += i
    return p # regresa la suma de los valores de la fila
        
def l(m): # funcion que imprime la matriz
    for i in m:
     print(i)

if __name__ == "__main__":
    f = int(input("Columnas: ")) # se ingresan los datos de la matriz
    c = int(input("Filas: "))
    a = int(input("Fila a sumar: ")) - 1 # se solicita la fila a sumar
    mt = m(c,f) # se llama a la funcion de generacion de matriz
    r = k(mt,a) # se llama a la funcion que suma la fila
    print("Matriz:")
    l(mt) # se imprime la matriz
    print(f"Suma de Fila: {r}") # se imprime la suma de la fila
```
