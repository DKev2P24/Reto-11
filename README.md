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

def mts2(p, z): 
    m2 = []
    for i in range(p):
        f1 = []
        for j in range(z):
            fp = int(input(f"Introduce la componente B{i + 1},{j + 1}: "))
            f1.append(fp)
        m2.append(f1)
    return m2

def sum(p, z): # Funcion que opera las matrices ingresadas
    m = [] # lista que acumula los valores de la suma
    for i in range(len(p)): # recorre las filas de las matrices
        t = [] # lista para almacenar las filas
        for j in range(len(p)): # se recorre las columnas de las matrices
            v = p[i][j] + z[i][j] # se opera cada elemento de cada fila y columna
            t.append(v) # se agregan a la lista los valores de las filas
        m.append(t) # se agregan los valores a la matriz
    return m # entrega la matriz

def rest(p, z):
    m = []
    for i in range(len(p)):
        t = []
        for j in range(len(p)):
            v = p[i][j] - z[i][j]
            t.append(v)
        m.append(t)
    return m

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

def m(p, z):  # funcion que opera las matrices
    m = [] # se acumulan los valores
    for i in range(len(p)): # se recorre cada elemento 
        t = [] # se acumulan las filas 
        for j in range(len(p)): # se recorre cada elemento  
            v = p[i][j] * z[i][j] se opera cada elemnto de cada fila y columna 
            t.append(v) # se agrega la lista
        m.append(t) # se agrega la lista y consolida la matriz
    return m # regresa la matriz producto

def im(x):
    for i in x:
        print(i)
        
if __name__ == "__main__":
    f = int(input("Filas: "))
    c = int(input("Columnas: "))
    mat1 = mts1(f, c)
    mat2 = mts2(f, c)
    mat4 = m(mat1, mat2)
    print("Matriz 1:",)
    im(mat1)
    print("Matriz 2:")
    im(mat2)
    print("Matriz Producto:")
    im(mat4)
```
## Matriz Transpuesta
```python
def m(m,n):
    k = []
    for i in range(m):
        l = []
        for j in range(n):
            mx = int(input(F"Coordenada F({j+1},{i+1})C: "))
            l.append(mx)
        k.append(l)
    return k

def z(m):
    for i in range(len(m)) :
         print(m[i])

if __name__ == "__main__":
    f = int(input("columnas: "))
    c = int(input("filas: "))
    ko = m(f,c)
    z(ko)
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

def k(n,o):
    p = 0
    for i in n:
         p += i[o]
    return p

def l(m):
    for i in m:
     print(i)

if __name__ == "__main__":
    f = int(input("Columnas:: "))
    c = int(input("Filas: "))
    a = int(input("Columna a sumar: ")) - 1
    mt = m(c,f)
    r = k(mt,a)
    print("Matriz:")
    l(mt)
    print(f"Suma de columna: {r}")
```
## Suma de Fila
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

def k(n,o):
    p = 0
    for i in n[o]:
        p += i
    return p
        
def l(m):
    for i in m:
     print(i)

if __name__ == "__main__":
    f = int(input("Columnas: "))
    c = int(input("Filas: "))
    a = int(input("Fila a sumar: ")) - 1
    mt = m(c,f)
    r = k(mt,a)
    print("Matriz:")
    l(mt)
    print(f"Suma de Fila: {r}")
```
