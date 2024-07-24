# Reto-11
## Suma/Resta de Matrices
```python
def mts1(p, z):
    m1 = []
    for i in range(p):
        f1 = []
        for j in range(z):
            fp = int(input(f"Introduce la coordenada A{i + 1},{j + 1}: "))
            f1.append(fp)
        m1.append(f1)
    return m1

def mts2(p, z):
    m2 = []
    for i in range(p):
        f1 = []
        for j in range(z):
            fp = int(input(f"Introduce la componente B{i + 1},{j + 1}: "))
            f1.append(fp)
        m2.append(f1)
    return m2

def sum(p, z):
    m = []
    for i in range(len(p)):
        t = []
        for j in range(len(p)):
            v = p[i][j] + z[i][j]
            t.append(v)
        m.append(t)
    return m

def rest(p, z):
    m = []
    for i in range(len(p)):
        t = []
        for j in range(len(p)):
            v = p[i][j] - z[i][j]
            t.append(v)
        m.append(t)
    return m

def im(x):
    for i in x:
        print(i)
        
if __name__ == "__main__":
    f = int(input("Filas: "))
    c = int(input("Columnas: "))
    mat1 = mts1(f, c)
    mat2 = mts2(f, c)
    mat3 = sum(mat1, mat2)
    mat4 = rest(mat1, mat2)
    print("Matriz 1:",)
    im(mat1)
    print("Matriz 2:")
    im(mat2)
    print("Matriz Suma:")
    im(mat3)
    print("Matriz Retsa:")
    im(mat4)
```
## Producto matrices
```python
def mts1(p, z):
    m1 = []
    for i in range(p):
        f1 = []
        for j in range(z):
            fp = int(input(f"Introduce la coordenada A{i + 1},{j + 1}: "))
            f1.append(fp)
        m1.append(f1)
    return m1

def mts2(p, z):
    m2 = []
    for i in range(p):
        f1 = []
        for j in range(z):
            fp = int(input(f"Introduce la componente B{i + 1},{j + 1}: "))
            f1.append(fp)
        m2.append(f1)
    return m2

def m(p, z):
    m = []
    for i in range(len(p)):
        t = []
        for j in range(len(p)):
            v = p[i][j] * z[i][j]
            t.append(v)
        m.append(t)
    return m

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


