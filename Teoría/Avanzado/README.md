# El lenguaje de programaci贸n Python - Avanzado 馃惓

 **<div style="text-align: right"> Samuel Arturo Garrido S谩nchez</div>**

Python es un lenguaje de programaci贸n **multiparadigma**, muy 煤til para demasiadas ramas de la investigaci贸n, desarrollos y procesos. 
Su filosof铆a radica en un c贸digo legible que cualquier persona no enfocada en el 谩rea de programaci贸n, pueda comprender.

![](img/let.png)

# MarkDown 鈿斤笍

# Cabeceras

# H1
## H2
### H3

Negrita:	**Texto negritas**
Cursiva:	*Texto en cursiva*
Tachado:    ~~El mundo es plano.~~



Comentario:	

> En este ejemplo pudimos notar algo excepcional

## Listas:

1. Primer elemento
2. Segundo elemento
3. Tercer elemento


## Listas desordenadas:

- Primer elemento
- Segundo elemento
- Tercer elemento

## Listas para tachar

- [x] Dar la clase
- [x] Poner su moodle
- [ ] Calificar sus tareas

## C贸digo

#### Terminal
`pip install proteco`

#### Python
```python
import numpy as np
print("Hola mundo")
```

#### Swift
```swift
import Foundation

let hola = "Hola a todos"
print(hola)

```


#### Java

```java
public class HolaMundo {
	public static void main(String[] args) {		
		System.out.println("Hola Mundo");
	}
}
```

Barra horizontal

---


## Link	

[Titulo Del Link](https://developer.apple.com)


## Imagen	

![Descripcion](img/1.jpg)


## LaTEX (v谩lido solo en Jupyter Notebook,Colab o Azure)

$$\int_{x^2}^{x^5} y^t_i s^t dt$$

## Tablas 

| Criterio      | Puntos | Obtenidos | Observaciones     |
|---------------|--------|-----------|-------------------|
| Examen        | 1      | 4         | Nada que comentar |
| Tareas        | 2      | 4         | Nada que comentar |
| Participacion | 3      | 4         | Nada que comentar |

## Tablas con formato

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

## Algo de Web

Tambien podemos poner cosas exclusivas de web por ejemplo im谩genes que tengan una forma. 

**Ejemplo:**

<dl>
  <dt>Lista de definici贸n</dt>
  <dd>Promulgamos algo mejor</dd>

  <dt>Markdown en HTML</dt>
  <dd>No *funciona* **muy** bien. Use mejor tags <em>HTML</em>.</dd>
</dl>

## VIDEOS

<a href="http://www.youtube.com/watch?feature=player_embedded&v=HzZxcfVn_08
" target="_blank"><img src="http://img.youtube.com/vi/HzZxcfVn_08/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="400" height="200" border="10" /></a>

<a href="http://www.youtube.com/watch?feature=player_embedded&v=afvT1c1ii0c
" target="_blank"><img src="http://img.youtube.com/vi/afvT1c1ii0c/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="400" height="200" border="10" /></a>

# Derivada

Voy a hacer la siguiente derivada 

$$\frac{d(x^2+2x)}{dx}$$

Y lo hago as铆 con Python


```python

```

Y eso es todo! 馃榾

# Gestor de paquetes PIP 馃崁

Nadie quiere inventar la rueda 2 veces y construir artefactos con mejores instrumentos nos ayuda a tener mejores resultados. El 茅xito de Python mayormente se basa en su comunidad, donde varios c贸digos funcionales de Python se liberan al mundo para que otras personas puedan desarrollar sus soluciones a partir de estas herramientas. 

#### Estos programas funcionales que nos pueden ayudar a crear gr谩ficas o hacer an谩lisis de datos m谩s r谩pidamente se llaman paquetes.

Un administrador de paquetes o un sistema de administraci贸n de paquetes es una colecci贸n de herramientas de software que automatiza el proceso de instalaci贸n, actualizaci贸n, configuraci贸n y eliminaci贸n de programas de computadora para el sistema operativo de una computadora de manera consistente.

El gestor de paquetes pip nos permitir谩 tener biblitecas de Python y podremos instalarlas con pip install <algo\>. 

- Para la instalaci贸n en: Windows

Descarga el c贸digo de Pip en: https://bootstrap.pypa.io/get-pip.py
luego c贸rrelo con python3 get-pip.py

- Para la instalaci贸n en: Mac

easy_install pip
o si ya lo instalaste por homebrew no hay problema. Viene incluido en brew install python3

- Para la instalaci贸n en: GNU/Linux Ubuntu


sudo apt install python3-pip

**LA MAYOR脥A DEL TIEMPO YA VIENE INSTALADO, PARA VERIFICAR ESTO ESCRIBA EN SU TERMINAL: pip**

## 馃挴 Numpy: De vuelta a Matem谩ticas

NumPy es una biblioteca para el lenguaje de programaci贸n Python, que agrega soporte para matrices y matrices grandes y multidimensionales, junto con una gran colecci贸n de funciones matem谩ticas de alto nivel para operar en estas matrices.





```python
#NP es un alias, para no escribir completamente numpy
import numpy as np
arreglo = np.array([1, 2, 3, 4, 5])
print(arreglo)
print("Tipo: ",type(arreglo))
print("Elementos del array:",arreglo.dtype)
```

    [1 2 3 4 5]
    Tipo:  <class 'numpy.ndarray'>
    Elementos del array: int64



```python
lista = [1,2,3]

vector = np.array(lista)

print("El vector:",vector)
print("Dimensiones del vector: ",vector.shape)
print("Cada elemento del vector +1:",vector+1)
print("Cada elemento del vector multiplicado por 5:",vector*5)
print("Suma de todos sus elementos: ",np.sum(vector))
print("Media de todos sus elementos:",np.mean(vector))

print("Suma del mismo vector:",vector+vector)

vector2 = np.array([8,9,10])

print("Suma de 2 vectores: ",vector + vector2)

print("Producto Punto de vectores:",vector.dot(vector2))
print("Producto Cruz de vectores",np.cross(vector,vector2))
```

    El vector: [1 2 3]
    Dimensiones del vector:  (3,)
    Cada elemento del vector +1: [2 3 4]
    Cada elemento del vector multiplicado por 5: [ 5 10 15]
    Suma de todos sus elementos:  6
    Media de todos sus elementos: 2.0
    Suma del mismo vector: [2 4 6]
    Suma de 2 vectores:  [ 9 11 13]
    Producto Punto de vectores: 56
    Producto Cruz de vectores [-7 14 -7]


### Matrices

Las matrices en numpy las usaremos de la siguiente forma, tomando en cuenta que cada lista que insertemos dentro de numpy singifica una nueva fila o de n煤meros dentro de la matriz.



```python
##Producto punto entre 2 matrices
a = np.array([[1,2],[3,4]]) 
b = np.array([[11,12],[13,14]])

print("Matriz 1:")
print(a)

print("Matriz 2:")
print(b)

print("Producto Punto entre ambas matrices:")
print(np.dot(a,b))
```

    Matriz 1:
    [[1 2]
     [3 4]]
    Matriz 2:
    [[11 12]
     [13 14]]
    Producto Punto entre ambas matrices:
    [[37 40]
     [85 92]]



```python
matriz1 = np.array([[1,2,3], [4,5,6]])
matriz2 = np.array([[4,5,6], [1,2,3]])
print("Producto cruz entre matrices:")
print(np.cross(matriz1,matriz2))
```

    Producto cruz entre matrices:
    [[-3  6 -3]
     [ 3 -6  3]]


Agregar una fila completa a una matriz solo es cuesti贸n de utilizar el m茅todo append. **Si queremos a帽adir una coluna deberemos especificar una correcta forma y dimensi贸n del arreglo**


```python
# A帽adir fila
primeraMatriz = np.array([[1, 2, 3], [4, 5, 6]])

print("Primera Matriz: ")
print(primeraMatriz)

nuevaMatriz = np.append(primeraMatriz, [[50, 60, 70]], axis = 0)
print("\nSegunda Matriz, a帽adiendo una fila: ")
print(nuevaMatriz)
```

    Primera Matriz: 
    [[1 2 3]
     [4 5 6]]
    
    Segunda Matriz, a帽adiendo una fila: 
    [[ 1  2  3]
     [ 4  5  6]
     [50 60 70]]



```python
#A帽adir una columna

import numpy
 
primerMatrix = numpy.array([[1, 2, 3], [4, 5, 6]])

#Podemos agregar un array de numpy o una lista al m茅todo append
segundaMatrix = numpy.array([[400], [800]])

print("Primera Matriz: ")
print(primerMatrix)
print("\nSegunda Matriz: ")
print(segundaMatrix)

nuevaMatriz = numpy.append(primerMatrix, segundaMatrix, axis = 1)

print("\nResultado de matrices, a帽adiendo una columna:")

print(nuevaMatriz)
```

    Primera Matriz: 
    [[1 2 3]
     [4 5 6]]
    
    Segunda Matriz: 
    [[400]
     [800]]
    
    Resultado de matrices, a帽adiendo una columna:
    [[  1   2   3 400]
     [  4   5   6 800]]


#### Dimensiones,tama帽os y formas de los arrreglos
Una cosa es la forma de los arreglos o matrices, o sea cu谩ntos elementos tiene de ancho y alto y otra muy distinta es si es un n煤mero escalar, un vector, una matriz o algo m谩s. La dimensi贸n es como decir estoy en el plano 2D pero tengo un rect谩ngulo que mide 5x10, el atributo .shape me da las medidas mientas .ndim me dir谩 que es 2 ya que estamos en dimensi贸n 2D y el tama帽o es la cantidad de elementos que tenemos en el arreglo, si es de forma 5x10, tendr谩 50 elementos.


```python
cero = np.array(1) 
uno = np.array([1, 2, 3, 4, 5])
dos = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
tres = np.array([[[1,2,3],[4,5,6]],[[7,8,9],[10,11,12]]])

#con el atributo ndim conoceremos su dimensi贸n
print("Arreglo 1 => Dimensi贸n: ",cero.ndim,"  Forma:",cero.shape, "         Tama帽o: ",cero.size)
print("Arreglo 2 => Dimensi贸n: ",uno.ndim,"  Forma:",uno.shape,"       Tama帽o: ",uno.size)
print("Arreglo 3 => Dimensi贸n: ",dos.ndim,"  Forma:",dos.shape,"     Tama帽o: ",dos.size)
print("Arreglo 4 => Dimensi贸n: ",tres.ndim,"  Forma:",tres.shape,"  Tama帽o: ",tres.size)

#Si queremos crear un arreglo de n dimensiones tendremos que colocar como par谩metro a ndim
cinco = np.array([1,2,3,4], ndmin = 5)
print("\nArreglo de dimensi贸n 5:",cinco)
```

    Arreglo 1 => Dimensi贸n:  0   Forma: ()          Tama帽o:  1
    Arreglo 2 => Dimensi贸n:  1   Forma: (5,)        Tama帽o:  5
    Arreglo 3 => Dimensi贸n:  2   Forma: (3, 3)      Tama帽o:  9
    Arreglo 4 => Dimensi贸n:  3   Forma: (2, 2, 3)   Tama帽o:  12
    
    Arreglo de dimensi贸n 5: [[[[[1 2 3 4]]]]]


**Podemos adem谩s, reformar o cambiar la estructura de este arreglo, por ejemplo pasar de una matriz de 1x12 a una matriz de 4x3**


```python
arreglo = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12])

nuevo_arr = arreglo.reshape(4,3) # M茅todo reshape me cambia la forma
print("Arreglo original:")
print(arreglo)
print("\nArreglo cambiado de forma:")
print(nuevo_arr)
```

    Arreglo original:
    [ 1  2  3  4  5  6  7  8  9 10 11 12]
    
    Arreglo cambiado de forma:
    [[ 1  2  3]
     [ 4  5  6]
     [ 7  8  9]
     [10 11 12]]



```python
# Recorrer arreglo con  np.ndinter nos permite recorrer el arreglo sin importar su dimensi贸n:

for elemento in np.nditer(arreglo):
    print(elemento)
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    11
    12


#### Acceso a los elementos dentro de los vectores Numpy
Para acceder a un elemento espec铆fico, podemos hacerlo igual como hac铆amos con listas o tuplas en Python, indicamos la posici贸n pero ahora como tenemos muchas dimensiones, tendremos qu茅 especificar qu茅 elementos querremos.


```python
#Acceso a elementos individuales
print("Elemento en el arreglo uno, pos 0: ",uno[0])
print("Elemento en la pos 1,0 de dos: ",dos[1,0])
print("Elemento en la pos 0,1,1 de tres:",tres[0,1,1])
```

    Elemento en el arreglo uno, pos 0:  1
    Elemento en la pos 1,0 de dos:  4
    Elemento en la pos 0,1,1 de tres: 5



```python
#Acceso a rango de elementos

arregloAcceso = np.array([1, 2, 3, 4, 5])
print("Arreglo:",arregloAcceso)
print("Del arreglo uno, de la pos 1 a la 3:",arregloAcceso[1:3])
print("Desde la pos. 1 hasta terminar:",arregloAcceso[1:])
print("Desde el principio hasta la pos 4:",arregloAcceso[:4])
print("De la posici贸n -3 a la pos -1 (empezar a contar desde el final):",arregloAcceso[-3:-1])
print("De la pos 1, hasta la 4 saltando de 2 en 2:",arregloAcceso[1:4:2])
```

    Arreglo: [1 2 3 4 5]
    Del arreglo uno, de la pos 1 a la 3: [2 3]
    Desde la pos. 1 hasta terminar: [2 3 4 5]
    Desde el principio hasta la pos 4: [1 2 3 4]
    De la posici贸n -3 a la pos -1 (empezar a contar desde el final): [3 4]
    De la pos 1, hasta la 4 saltando de 2 en 2: [2 4]


### Arreglos de otras cosas
Podemos tener arreglos de decimales, de strings pero no se utilizan tanto como los n煤meros en numpy.

Adem谩s podemos indicar si nuestro arreglo lo queremos pasar a un tipo de dato como un n煤mero complejo o a flotante.


```python
matrizCadena = np.array(['Hola','Adios','Permiso'])
print("Tipo de Cadena:",matrizCadena.dtype)

matrizFlotante = np.array([10.411, 20.533, 30.851])
print("Tipo de cadena:",matrizFlotante.dtype)

matrizConversion = np.array([1, 2, 3, 4], dtype='f')
print("Arreglo de float:",matrizConversion.dtype)

cerosComplejos = np.zeros((2,2),dtype=np.complex_)
print("\n")
print(cerosComplejos)
print("\n")
print("Tipo dato de arreglo de complejos:",cerosComplejos.dtype)

#Con el m茅todo AsType podremos pedirle que nos pase 
## toda la matriz en un tipo de dato Espec铆fico
matrizEnteros = matrizFlotante.astype(int)

print("Castear todos los elementos, usar astype:",matrizEnteros)
```

    Tipo de Cadena: <U7
    Tipo de cadena: float64
    Arreglo de float: float32
    
    
    [[0.+0.j 0.+0.j]
     [0.+0.j 0.+0.j]]
    
    
    Tipo dato de arreglo de complejos: complex128
    Castear todos los elementos, usar astype: [10 20 30]


### Arreglos aleatorios y funciones 煤tiles
Podemos utilizar la funci贸n random de numpy para optener n煤meros aleatorios a trav茅s de numpy


```python
from numpy import random

enteroAleatorio = random.randint(100) #del 0 a 100
print("N煤mero entero aleatorio entre 0 y 100:",enteroAleatorio)

#Para una matriz aleatoria especificamos la forma en que la queremos 
# Y saldr谩n solo n煤mero entre 0 y 1

matrizAleatoriaFlotantes = random.rand(2,3) 
print("\nMatriz Flotantes:\n",matrizAleatoriaFlotantes)

#Para una matriz aleatoria especificamos la forma en que la queremos 
# Y saldr谩n solo n煤mero entre 0 y 1
matrizAleatoriaEnteros = random.randint(100, size = (5,5))
print("\nMatriz Enteros:\n",matrizAleatoriaEnteros)
```

    N煤mero entero aleatorio entre 0 y 100: 63
    
    Matriz Flotantes:
     [[0.37067447 0.70828821 0.66149885]
     [0.38387195 0.79572182 0.70431242]]
    
    Matriz Enteros:
     [[ 1 56 58 95  6]
     [67 19 91 30  7]
     [12 71 21 56 92]
     [33 85 34 51 43]
     [65  0 57 66 73]]



```python
#Crear arreglo dado rangos
arregloPersonalizado = np.arange(2,30,3) #Inicio, fin, de cu谩nto en cu谩nto
print("Arreglo rangos 1D:",arregloPersonalizado)

#Crear matriz de ceros
matrizCeros = np.zeros((3,3), dtype=int)
print("\nMatriz Ceros:\n",matrizCeros,"\n")

#Crear matriz de unos
matrizUnos = np.ones((3,3), dtype=int)
print("\nMatriz Unos:\n",matrizUnos,"\n")


#Sacar ra铆z cuadrada a cada elemento
raiz = np.sqrt(np.array([1,4,9,16,25]))
print("Matriz ra铆z cuadrada:",raiz)


#Rellenar con vectores una matriz
relleno = np.full((2,2), [3,5])
print("\nMatriz rellenada:\n",relleno)
```

    Arreglo rangos 1D: [ 2  5  8 11 14 17 20 23 26 29]
    
    Matriz Ceros:
     [[0 0 0]
     [0 0 0]
     [0 0 0]] 
    
    
    Matriz Unos:
     [[1 1 1]
     [1 1 1]
     [1 1 1]] 
    
    Matriz ra铆z cuadrada: [1. 2. 3. 4. 5.]
    
    Matriz rellenada:
     [[3 5]
     [3 5]]


### Operaciones fundamentales de matrices

- T = Transpuesta
- H = Hermitiana


```python
matrix = np.array([[1,2,3],[3,4,5],[4,5,6]])
```


```python
import sympy as sp

sp.pi.evalf(100)

x = Symbol('x')
sp.integrate(x**3,x)
```




## 馃搳 Matplolib: Todos merecemos ver 

Matplotlib es una biblioteca para la generaci贸n de gr谩ficos a partir de datos contenidos en listas o arrays en el lenguaje de programaci贸n Python y su extensi贸n matem谩tica NumPy. Por ejemplo, si yo quiero graficar la siguiente funci贸n:

$$ f(x) = x^2$$


Lo haremos de la siguiente manera:


```python
import matplotlib.pyplot as plt # Importamos matplotlib pyplot y le ponemos un alias: plt
import numpy as np # Importamos numpy y ponemos un alias, np

%matplotlib inline 
##Esta l铆nea es importante para que muestre las gr谩ficas en Jupyter Notebook
```


```python
x = np.linspace(-10, 10, 100) ## Especificamos un rango y cu谩ntos puntos intermedios ir谩 calculando
#print(x)

y = x**2   ## Definimos la funci贸n
#print(y)

figura, imagen = plt.subplots() ## Este m茅todo regresa una figura para exportar a png y la imagen para proyectar
imagen.plot(x, y) ## Mostramos la imagen
plt.show() ## Es importante para que nos muestre la imagen
```


    
![](img/output_36_0.png)
    



```python
x = np.arange(0.,2.,.05)

y1= x
y2= x**2

plt.plot(x,y1, '.b', label='Lineal', markersize=1)
plt.plot(x,y2, '--g', label="Cuadrada", linewidth=2)

#Nombres: Podemos colocar el nombre de la gr谩fica, del eje x y del eje y
plt.title('Gr谩fica de ventas')
plt.xlabel('Ventas')
plt.ylabel('Ganancias')


plt.legend() # Nos muestra la simbolog铆a
plt.grid(True) ## Nos muestra la cuadr铆cula
plt.show() # Nos muestra la gr谩fica
```


    
![png](img/output_37_0.png)
    



```python
import matplotlib.pyplot as plt
import numpy as np

# Informaci贸n para plotear
rango = np.arange(0.0, 2.0, 0.01)

onda = 1 + np.sin(2 * np.pi * rango)

figura, grafica = plt.subplots()
grafica.plot(rango, onda)

grafica.set(xlabel='Tiempo (s)', ylabel='Voltaje (V)',title='Ejemplo')
grafica.grid()

## figura.savefig("imagen.png")
plt.show()
```


    
![](img/output_38_0.png)
    



```python
x=np.arange(0.,10., 0.2)
seno=np.sin(x)
coseno=np.cos(x)

plt.plot(x,seno, label="Seno")
plt.plot(x,coseno, label="Coseno")
plt.title('Gr谩ficas de Seno y Coseno')

plt.legend()
plt.grid(True)
plt.show()
```


    
![](img/output_39_0.png)
    



```python
x = [2,4,6,7,9,13,19,26,29,31,36,40,48,51,57,67,69,71,78,88]
y = [54,72,43,2,8,98,109,5,35,28,48,83,94,84,73,11,464,75,200,54]
plt.scatter(x,y)
plt.show()
```


    
![](img/output_40_0.png)
    



```python
plt.plot([4,8,13,17,20],[54, 67, 98, 78, 45],'r--d')
plt.show()
```


    
![](img/output_41_0.png)
    



```python
import matplotlib.pyplot as plt
x = [2,4,6,5,42,543,5,3,73,64,42,97,63,76,63,8,73,97,23,45,56,89,45,3,23,2,5,78,23,56,67,78,8,3,78,34,67,23,324,234,43,544,54,33,223,443,444,234,76,432,233,23,232,243,222,221,254,222,276,300,353,354,387,364,309]
num_bins = 6
n, bins, patches = plt.hist(x, num_bins, facecolor = 'green')
plt.show()
```


    
![png](img/output_42_0.png)
    



```python
import matplotlib.pyplot as plt
plt.plot((4,8,13,17,20),(54, 67, 98, 78, 45))
plt.show()
```


    
![png](img/output_43_0.png)
    



```python
from scipy import misc
import matplotlib.pyplot as plt

face = misc.face()
plt.imshow(face)
plt.show()
```


    
![png](img/output_44_0.png)
    


## Ejemplo: Cantidad de Sistemas Operativos




```python
DataSetSO = {'iOS':1, 'Android':5, 'Windows':10, 'macOS':2, 'GNU/Linux':20}

SO_Nombre= list(monedas.keys())
SO_Cantidad=list(monedas.values())
```


```python
import matplotlib.pyplot as plt

plt.pie(SO_Cantidad, labels=SO_Nombre, colors=['blue','cyan','red','green','gold'], autopct='%.4f%%', startangle=90)
plt.title('Gr谩fica de pastel de Sistemas Operativos')

plt.show()
```


    
![png](img/output_47_0.png)
    


## Gr谩fica de Barras


```python
plt.bar(SO_Nombre, SO_Cantidad, color='red', linewidth='4')
plt.title('Sistemas operativos')
plt.show()
```


    
![png](img/output_49_0.png)
    


## Gr谩fica de burbujas


```python
N=50 ## Cantidad de puntos
x=np.random.rand(N)
y=np.random.rand(N)

colors = np.random.rand(N) ## colores aleatorios

area = (30*np.random.rand(N))**2

plt.scatter(x,y, s=area, c=colors, alpha=0.5)
plt.show()
```


    
![png](img/output_51_0.png)
    



```python
from mpl_toolkits.mplot3d import Axes3D
import matplotlib.pyplot as plt # Importamos matplotlib pyplot y le ponemos un alias: plt
%matplotlib inline 
fig = plt.figure()
ax=Axes3D(fig)

x= np.linspace(-4,4,50)
y= np.linspace(-4,4,50)
X,Y=np.meshgrid(x,y)


ax.plot_surface(X,Y,np.cos(np.sqrt(X**2+Y**2)), color='green')

#Para girar la imagen usamos view_init
#elev: es el angulo de elevaci贸n sobre el eje z
#azim: es el azimuth, rota la gr谩fica en los ejes x y y, es decir de manera horizontal
#Los valores por defecto utilizados son azim=-60 elev=30
ax.view_init(elev=30, azim=-60)

plt.show()
```


    
![png](img/output_52_0.png)
    



```python
%matplotlib notebook
import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D

fig = plt.figure()
ax=Axes3D(fig)

x= np.linspace(-4,4,50)
y= np.linspace(-4,4,50)
X,Y=np.meshgrid(x,y)

ax.plot_surface(X,Y,np.cos(np.sqrt(X**2+Y**2)), color='red')
plt.show()
```


 <IPython.core.display.Javascript object>

## Ejemplo de m茅todos num茅ricos 馃崷

**<span style="color:red"> ** IMPORTANTE ** </span>**

Para escribir una ecuaci贸n tienes que separar todo y multiplicar con \*:  
f=2x+3 鉂?     
f = 2*x + 3 鉁?

Para poner una potencia por ejemplo $2^3$ es poniendo doble aster铆sco. Ejemplo:

$$f(x) = x^2 + 2x +1$$

Equivale a:


```python
import sympy as sy
from sympy.functions import sin,cos
import math
import matplotlib.pyplot as plt
x = sy.symbols('x')
def taylor(funcion,c,n):
    i = 0
    p = 0
    while i <= n:
        p = p + (funcion.diff(x,i).subs(x,c))/(math.factorial(i))*(x-c)**i
        i += 1
    return p
```


```python
#CAMBIA LA FUNCION, en d贸nde est谩 alineado taylor (este caso c=0) y cu谩l es el mayor exponenete que quieres (este es 4)
p = taylor(cos(x),0,4)
print("El polinomios de Taylor es: ",p)
```

    El polinomios de Taylor es:  x**4/24 - x**2/2 + 1



```python
#Coloca aqu铆 la evaluaci贸n del mismo
x=math.pi/3
## COLOCA AQU脥 EL RESULTADO DEL ANTERIOR POR AHORA D:
VALOROBTENIDO = x**4/24 - x**2/2 + 1
print("El valor de taylor es: ",VALOROBTENIDO)
```

    El valor de taylor es:  0.501796201500181


## M茅todo de bisecci贸n 馃搳


```python
# Inserta la ecuaci贸n a buscar ra铆z
fx = lambda x: x**2 + 9*x + 4
```


```python
# Inserta tu rango y tolerancia
a = -5
b = 2
tolera = 0.01
```


```python
# PROCEDIMIENTO
tabla = []
tramo = b-a
fa = fx(a)
fb = fx(b)
i = 1
while (tramo>tolera):
    c = (a+b)/2
    fc = fx(c)
    tabla.append([i,a,c,b,fa,fc,fb,tramo])
    i = i+1
                 
    cambia = np.sign(fa)*np.sign(fc)
    if (cambia<0):
        b = c
        fb = fc
    else:
        a=c
        fa = fc
    tramo = b-a
c = (a+b)/2
fc = fx(c)
tabla.append([i,a,c,b,fa,fc,fb,tramo])
tabla = np.array(tabla)
raiz = c
np.set_printoptions(precision = 4)
print('i   a     c    b     f(a)   f(c)  f(b)  toler')
n=len(tabla)
for i in range(0,n,1):
    unafila = tabla[i]
    formato = '{:.0f}'+' '+(len(unafila)-1)*'{:.3f} '
    unafila = formato.format(*unafila)
    print(unafila)
print('raiz: ',raiz)
```

    i   a     c    b     f(a)   f(c)  f(b)  toler
    1 -5.000 -1.500 2.000 -16.000 -7.250 26.000 7.000 
    2 -1.500 0.250 2.000 -7.250 6.312 26.000 3.500 
    3 -1.500 -0.625 0.250 -7.250 -1.234 6.312 1.750 
    4 -0.625 -0.188 0.250 -1.234 2.348 6.312 0.875 
    5 -0.625 -0.406 -0.188 -1.234 0.509 2.348 0.438 
    6 -0.625 -0.516 -0.406 -1.234 -0.375 0.509 0.219 
    7 -0.516 -0.461 -0.406 -0.375 0.064 0.509 0.109 
    8 -0.516 -0.488 -0.461 -0.375 -0.156 0.064 0.055 
    9 -0.488 -0.475 -0.461 -0.156 -0.046 0.064 0.027 
    10 -0.475 -0.468 -0.461 -0.046 0.009 0.064 0.014 
    11 -0.475 -0.471 -0.468 -0.046 -0.019 0.009 0.007 
    raiz:  -0.47119140625



```python
import scipy.optimize as opt
#Inserta tu funci贸n
f1 = lambda x: x**3 + 4*x**2 - 10
# Solo cambia el rango 1,2 y la tolerancia, no cambies el xtol o tronar谩
print(opt.bisect(f1,1,2,xtol=0.001))
```

    1.3642578125


### M茅todo de Newton Raphson 猸愶笍


```python
x=sy.symbols('x')
#funcion
funcion=sin(x) + cos(x)

derivada=sy.diff(funcion,x)

x_0=0
xr=x_0

ea=100/100

es=0.001/100
contador=-1
print("i\t   xi\t     Error Absoluto Porcentual")
while ea>es:
    xra=xr
    contador+=1
    newton_rhapson=x-(funcion/derivada)

    xr=newton_rhapson.evalf(subs={x: xr})
    
    #error aproximado relativo porcentual
    ea=sy.Abs(((xr-xra)/xr)*100)
    #resultado
    print(contador   ,xra, ea)
```

    i	   xi	     Error Absoluto Porcentual
    0 0 100.000000000000
    1 -1.00000000000000 27.8703862327451
    2 -0.782041901539138 0.427334129760588
    3 -0.785398175999702 1.60456876032265e-6


## M茅todo de la regla falsa.

El m茅todo de regla falsa o interpolaci贸n se basa en tener 2 limitantes o rango que sepamos que contienen a la ra铆z de la funci贸n. Su ecuaci贸n es:


$$r\in[a,b]$$


$$ x_i = \frac{f(a_i)bi - f(b_i)a_i}{f(a_i)-f(b_i)} $$


```python
## Inserte la ecuaci贸n aqu铆
x=sy.symbols('x')
Px = lambda x: x**2 - 2*x - 10

## Fija los rangos de a y b donde buscar谩n
a = 2
b = 6
tolerancia = 0.1
l = (Px(a)*b - Px(b)*a)/(Px(a)-Px(b))
print(l)
```

    3.6666666666666665



```python
def metodoFalso(f,a,b):
    anterior = 0
    error = 1
    while(error>tolerancia):
        l = (Px(a)*b - Px(b)*a)/(Px(a)-Px(b))
        
```

## Introducci贸n a Inteligencia Artificial 馃

La investigaci贸n en inteligencia artificial comenz贸 en la d茅cada de los 50, continuando el trabajo llevado a cabo por el matem谩tico brit谩nico Alan Turing durante la Segunda Guerra Mundial. Sin embargo, no ha sido hasta la 煤ltima d茅cada cuando se han producido los avances m谩s r谩pidos en cuanto a IA, como consecuencia de la combinaci贸n de tres factores cruciales: el cloud computing (computaci贸n en la nube), la gran cantidad de datos y los grandes avances en machine learning (aprendizaje autom谩tico).

## SciKitLearn: Aprendizaje M谩quina con Python 鈿斤笍


## Regresi贸n 馃崝

驴Les gustar铆a predecir el futuro?
Bueno antes que nada para los de ciencias e ingenier铆a y los 谩rea 1: 驴Qu茅 es una pendiente y una ordenada al origen?

Bueno en el sentido de la palabra, una regresi贸n lineal es obtener la relaci贸n entre unas variables independietes y una variable dependiente. 

- X's son nuestros inputs
- Y es nuestro target

La expresi贸n matem谩tica general de una regresi贸n lineal es:


$$y = \beta_0 + \beta_1x_1 + \beta_2x_2 + ... + \beta_nx_n + \epsilon$$

$$ y = \beta_0 + \sum_{i=1}^n\beta_ix_i + \epsilon $$

## Regresi贸n: Regresi贸n Lineal Simple

Cuando solo tenemos la expresi贸n con i = 1 tendremos la expresi贸n dada en:

$$\beta_0 + \beta_1x_1 + \epsilon$$

Los que tratamos de hacer es: Obtener las betas y epsilon. Para quedar m谩s claro imagen la expresi贸n anterior como:

$$y = mx + b$$

Si recordar谩n de su curso de matem谩ticas en la secundaria m es la pendiente y b la ordenada al origen y podemos decir que beta 0 es equivalente a b y beta 1 es equivalente a beta 1.

Ahora.驴C贸mo calculaban la pendiente?

$$ m = \frac{y_2-y_1}{x_2-x_1}$$

驴Esto se val铆a si ten铆a puntos regados? NEL, solo se vale cuando tenemos puntos alieados. Qu茅 pasa si quiero encontrar m que tenga el mejor ajuste a todos los puntos de la recta?




```python
import pandas as pd

Data = {'X': [6.1,5.8,5.7,5.7,5.8,5.6,5.5,5.3,5.2,5.2],
        'Y': [1500,1520,1525,1523,1515,1540,1545,1560,1555,1565]
       }
  
tablita = pd.DataFrame(Data,columns=['X','Y'])
tablita
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>X</th>
      <th>Y</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>6.1</td>
      <td>1500</td>
    </tr>
    <tr>
      <th>1</th>
      <td>5.8</td>
      <td>1520</td>
    </tr>
    <tr>
      <th>2</th>
      <td>5.7</td>
      <td>1525</td>
    </tr>
    <tr>
      <th>3</th>
      <td>5.7</td>
      <td>1523</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5.8</td>
      <td>1515</td>
    </tr>
    <tr>
      <th>5</th>
      <td>5.6</td>
      <td>1540</td>
    </tr>
    <tr>
      <th>6</th>
      <td>5.5</td>
      <td>1545</td>
    </tr>
    <tr>
      <th>7</th>
      <td>5.3</td>
      <td>1560</td>
    </tr>
    <tr>
      <th>8</th>
      <td>5.2</td>
      <td>1555</td>
    </tr>
    <tr>
      <th>9</th>
      <td>5.2</td>
      <td>1565</td>
    </tr>
  </tbody>
</table>
</div>



驴C贸mo se est谩n comportando esos datos? Imprimimos la gr谩fica scatter para saberlo.


```python
import matplotlib.pyplot as plt
%matplotlib inline

plotPuntos = tablita.plot(x ='X', y='Y', kind = 'scatter')
plt.show()
```


    
![png](img/output_75_0.png)
    



```python
from scipy import stats
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

pendiente, ordenadaOrigen, valor_r, valor_p, error = stats.linregress(tablita['X'].tolist(),tablita['Y'].tolist())

t = np.arange(5.2,6.2,0.1)

plt.plot(t,pendiente*t+ordenadaOrigen,'--r')
plt.scatter(tablita['X'].tolist(),tablita['Y'].tolist())
plt.show()
```


    
![png](img/output_76_0.png)
    


#### M铆nimos cuadrados
Para poder determinar la recta que tenga mejor ajuste necesitaremos una t茅cnica llamada m铆nimos cuadrados y esto como para qu茅?

Bueno lo que hace es minimizar el error cuadr谩tico medio dado:

$$b = \frac{\sum y\sum x^2 - \sum x-\sum x y}{N\sum x^2 - (\sum x)^2}$$

$$ m = \frac{N\sum xy - \sum x\sum y}{N\sum x^2 - (\sum x)^2} $$

**Peeeero**, imag铆nense con un dataset enorme, gigantesco donde la memoria es primordial. 驴Volver铆an a ejecutar estas ecuaciones para cada nuevo dato que tengamos en el dataset?

**Pues la respuesta es NO**. Para ello existen los m茅todos num茅ricos.

Para calcular b y m no es necesario seguir esas ecuaciones, ya que son muy precisas. 

> Los que ya hayan llevado m茅todos num茅ricos me entender谩n.

Cuando una computadora realiza c谩lculos siempre lo hace con m茅todos num茅ricos y estos tienen una tolerancia y mediante iteraciones vamos reduciendo esa tolerancia lo m谩s posible siendo un tiempo determinado. Se aceptan errores, claro, y esto nos permite que si ya tenemos ajustado nuestro modelo solo tengamos que moverlo un poquito.




## Tama帽os de predicci贸n. 

Por lo general en el 谩rea de estad铆stica existe algo llamado estad铆stica inferencial donde tomamos de una muestra de la poblaci贸n. Considerarlo al momento de obtener muestras muy peque帽as.

Para calcular ese error o tolerancia se recurre a algo llamado el c谩lculo del error cuadr谩tico medio de estad铆stica que quiere decir, la suma de todas las diferencias de la funci贸n calculada hasta los inputs cu谩nto me da. Buscamos que se la m铆nima posible y al ser una funci贸n cuadr谩tica esta es una par谩bola.


$$ECM(\theta') = E[(\theta' - \theta)^2] = Var(\theta') + sesgo(\theta') ^2$$


```python
import numpy as np
import random
from sklearn import linear_model
from sklearn.metrics import mean_squared_error, r2_score
import matplotlib.pyplot as plt

%matplotlib inline
 
# Generador de distribuci贸n de datos para regresi贸n lineal simple
def generador_datos_simple(beta, muestras, desviacion):
    # Genero n (muestras) valores de x aleatorios entre 0 y 100
    x = np.random.random(muestras) * 100
    # Genero un error aleatorio gaussiano con desviaci贸n t铆pica (desviacion)
    e = np.random.randn(muestras) * desviacion
    # Obtengo el y real como x*beta + error
    y = x * beta + e
    return x.reshape((muestras,1)), y.reshape((muestras,1))
 
# Par谩metros de la distribuci贸n normal
desviacion = 200
beta = 10
n = 50

x, y = generador_datos_simple(beta, n, desviacion)

plt.scatter(x, y)
plt.title("Gr谩fica de puntos aleatorios")
plt.show()
```


    
![png](img/output_80_0.png)
    



```python
# Creo un modelo de regresi贸n lineal
modelo = linear_model.LinearRegression()

# Entreno el modelo con los datos (X,Y)
modelo.fit(x, y)


# Ahora puedo obtener el coeficiente b_1
print ('Coeficiente beta1: ', modelo.coef_[0])
 
# Podemos predecir usando el modelo
y_pred = modelo.predict(x)


# Por 煤ltimo, calculamos el error cuadr谩tico medio y el estad铆stico R^2
print ("Error cuadr谩tico medio: ", mean_squared_error(y, y_pred))

plt.scatter(x, y) ## Graficamos los puntos

plt.plot(x, y_pred, color='red') ## Graficamos la predicci贸n de SciKitLearn

x_real = np.array([0, 100])
y_real = x_real*beta

plt.plot(x_real, y_real, color='green') ## Graficamos con M茅todo de M铆nimos Cuadrados
plt.show()
```

    Coeficiente beta1:  [8.0409]
    Error cuadr谩tico medio:  51423.42693265156



    
![png](img/output_81_1.png)
    


**驴Conclusiones?**

## Clasificaci贸n: Regresi贸n Log铆stica


```python
import matplotlib.pyplot as plt

# Importar el dataset, clasificadores y m茅tricas de rendimiento

from sklearn import datasets, svm, metrics
from sklearn.model_selection import train_test_split

digitos = datasets.load_digits()

_, renglon = plt.subplots(2, 4) ## imprimimos un arreglo de im谩genes de 2 x 4

imagenes_con_etiquetas = list(zip(digitos.images, digitos.target)) 

## Aqu铆 vamos recorriendo cada una de nuestras im谩genes con etiquetas 
for grafo, (imagen, etiqueta) in zip(renglon[0, :], imagenes_con_etiquetas[:4]):
    grafo.set_axis_off()
    grafo.imshow(imagen, cmap=plt.cm.gray_r, interpolation='nearest')
    grafo.set_title('Entrena:'+str(etiqueta))

# Para aplicar un clasificador a estos, necesitamos una imagen plana,

##Reacomodamos la imagen a una lineal
CantidadImagenes = len(digitos.images)
print("Hay ",CantidadImagenes,"im谩genes")
data = digitos.images.reshape((CantidadImagenes, -1)) ## Las hacemos todas lineales

# Creamos un vector clasificador
clasificador = svm.SVC(gamma=0.001)

# Sacar el conjunto de train y de test
X_train, X_test, y_train, y_test = train_test_split(data, digitos.target, test_size=0.5, shuffle=False)

# Entrenamos con los subconjuntos de traing
clasificador.fit(X_train, y_train)

# Tomamos una imagen, la probamos y mandamos a predicci贸n
imagen_predicha = clasificador.predict(X_test)

## Ahora tomamos las im谩genes de prueba, las de TEST
test = list(zip(digitos.images[CantidadImagenes // 2:], imagen_predicha))

for grafo, (imagen, prediccion) in zip(renglon[1, :], test[:4]):
    grafo.set_axis_off()
    grafo.imshow(imagen, cmap=plt.cm.gray_r, interpolation='nearest')
    grafo.set_title("Predicci贸n:"+str(prediccion))

plt.show()

```

    Hay  1797 im谩genes



    
![png](img/output_84_1.png)
    


## No s茅 si poner algoritmo: Diagn贸stico de Wisconsin para el c谩ncer de mama. 馃槵

El c谩ncer de mama (BC) es uno de los c谩nceres m谩s comunes entre las mujeres en todo el mundo, y representa la mayor铆a de los casos nuevos de c谩ncer y las muertes relacionadas con el c谩ncer seg煤n las estad铆sticas mundiales, lo que lo convierte en un problema de salud p煤blica importante en la sociedad actual.

Lo que tenemos disponible en el DataSet es:

- radio (media de las distancias desde el centro hasta los puntos del per铆metro)
- textura (desviaci贸n est谩ndar de los valores de escala de grises)
- per铆metro
- zona
- suavidad (variaci贸n local en longitudes de radio)
- compacidad (per铆metro虏 / 谩rea - 1.0)
- concavidad (gravedad de las porciones c贸ncavas del contorno)
- puntos c贸ncavos (n煤mero de porciones c贸ncavas del contorno)
- simetr铆a
- dimensi贸n fractal ("aproximaci贸n de la l铆nea costera" - 1)

## Extra: TensorFlow - Framework para Redes Neuronales 猸愶笍

### Primer Algoritmo: MNIST


<p>
  <img src="https://storage.googleapis.com/kaggle-datasets-images/2243/3791/9384af51de8baa77f6320901f53bd26b/dataset-cover.png" align = "right" width="600"/>
</p>


MNIST es un dataset muy popular y algunos lo consideran el "Hola mundo" para Tensor. B谩sicamente consta de varias im谩genes de ropa para poder clasificar a trav茅s de una Red Neuronal Artificial, ya que todas son del mismo tama帽o.

Para ello usaremos una capa densa, una capa de Dropout y una segunda capa densa de Salida.

- Compilaremos y entrenaremos el modelo para poder sacar los respectivos pesos de la funci贸n.


```python
import numpy as np #Importamos numpy para los arreglos
import datetime
import tensorflow as tf # Importamos TensorFlow
from tensorflow.keras.datasets import fashion_mnist ## Importams un dataset de Keras, el MNIST

#Cargar el dataset Fashion Mnist y las variables Xtrain, Xtest, Ytrain Ytest guardan los valores de retorno
(X_train, y_train), (X_test, y_test) = fashion_mnist.load_data()
```

### Normalizaci贸n de las im谩genes

Se divide cada imagen en los conjunto de entrenamiento (train) y de pruebas (test) entre el valor m谩ximo de cada uno de los p铆xeles (255), ya que 0 significa negro y 255 significa un pixel blanco.

De este modo, cada p铆xel se hallar谩 en el rango [0, 1], siendo 0 negro y 1 blanco. 

- 驴Para qu茅 hacemos esto? 

Al normalizar las im谩genes, nos aseguramos que nuestro modelo de RNA entrenar谩 m谩s r谩pidamente.


```python
 X_train = X_train / 255.0
X_test = X_test / 255.0
```

### Redimensionar el dataset

Como vamos a utilizar una red neuronal totalmente conectada, vamos a redimensionar los subconjuntos de entrenamiento y testing a formato de vector en lugar de en formato de matriz. Esto significa, nuestras im谩genes tienen 28x28 pixeles, podemos representar cada uno de sus pixeles como un color entre 0 y 1 ya que normalizamos las im谩genes. Ahora en lugar de ponerlo como matriz pondremos un arreglo lineal de 1x(28x28) = 1x784. Esto para tener la primera capa 784 neuronas.


```python
#Como cada imagen tiene 28x28 p铆xeles, usamos la funci贸n reshape en todo el dataset de entrenamiento para convertirlo 
# en vectores de tama帽o [-1 (todos los elementos), anchura * altura]
X_train = X_train.reshape(-1, 28*28)
print(X_train.shape)
X_test = X_test.reshape(-1, 28*28)
print(X_test.shape)
```

    (60000, 784)
    (10000, 784)


## Que empiece la construcci贸n del RNA 馃崁

## - Definir el modelo
Simplemente se define un objeto de modelo Sequential.


```python
model = tf.keras.models.Sequential()
```

## - A帽adir la primera capa totalmente conectada (capa Densa)

Hyper-parametros de la capa:

- N煤mero de unidades/neuronas: **128**

- Funci贸n de activaci贸n: **ReLU**


```python
model.add(tf.keras.layers.Dense(units=128, activation='relu', input_shape=(784, )))
```

## - A帽adir una capa de Dropout

Dropout es una t茅cnica de Regularization donde aleatoriamente se asignan a ciertas neuronas de la red el valor cero. De este modo, mientras se entrena, estas neuronas no actualizar谩n sus valores. Al tener cierto porcentaje de neuronas sin actualizar, el proceso de entrenamiento toma m谩s tiempo pero por contra tenemos menos posibilidades de sufrir sobreentrenamiento (overfitting).


```python
model.add(tf.keras.layers.Dropout(0.2))
```

## - A帽adir capa de salida

En el caso de MNIST tenemos 10 posibles prendas de ropa, por lo que a帽adiremos una capa con 10 neuronas 煤nicamente al final, en este caso como es una capa de salida y queremos probabilidades por lo mismo, utilizaremos una funci贸n de activaci贸n SoftMax

- N煤mero de unidades/neuronas: **10** en el caso del Fashion MNIST

- Funci贸n de activaci贸n: **softmax** (probabilidades de cada clase)


```python
model.add(tf.keras.layers.Dense(units=10, activation='softmax'))
```

## Compilar el modelo

Ahora compilaremos todo nuestro modelo, para ello es necesario una funci贸n de 

- Funci贸n optimizaci贸n: Adam

- Funci贸n de costo o p茅rdida: Sparse softmax (categorical) crossentropy

- M茅trica: sparse_categorical_accuracy comprueba si el valor verdadero m谩ximo es igual al 铆ndice del valor predicho m谩ximo.


```python
model.compile(optimizer='adam', loss='sparse_categorical_crossentropy', metrics=['sparse_categorical_accuracy'])
model.summary()
```

    Model: "sequential"
    _________________________________________________________________
    Layer (type)                 Output Shape              Param #   
    =================================================================
    dense (Dense)                (None, 128)               100480    
    _________________________________________________________________
    dropout (Dropout)            (None, 128)               0         
    _________________________________________________________________
    dense_1 (Dense)              (None, 10)                1290      
    =================================================================
    Total params: 101,770
    Trainable params: 101,770
    Non-trainable params: 0
    _________________________________________________________________


## Entrenar el modelo



```python
model.fit(X_train, y_train, epochs=5)
```

    Train on 60000 samples
    Epoch 1/5
    60000/60000 [==============================] - 4s 63us/sample - loss: 0.5341 - sparse_categorical_accuracy: 0.80953
    Epoch 2/5
    60000/60000 [==============================] - 3s 57us/sample - loss: 0.4030 - sparse_categorical_accuracy: 0.8540
    Epoch 3/5
    60000/60000 [==============================] - 3s 52us/sample - loss: 0.3692 - sparse_categorical_accuracy: 0.8644
    Epoch 4/5
    60000/60000 [==============================] - 3s 49us/sample - loss: 0.3500 - sparse_categorical_accuracy: 0.8712
    Epoch 5/5
    60000/60000 [==============================] - 3s 49us/sample - loss: 0.3320 - sparse_categorical_accuracy: 0.87820s - loss: 0.3326 - sparse_categorical_accuracy: 0.8





    <tensorflow.python.keras.callbacks.History at 0x149bc7710>



# Evaluaci贸n del modelo


```python
test_loss, test_accuracy = model.evaluate(X_test, y_test)
print("Precisi贸n del modelo: ",test_accuracy)
```

    10000/10000 [==============================] - 0s 37us/sample - loss: 0.3555 - sparse_categorical_accuracy: 0.8684
    Precisi贸n del modelo:  0.8684


Si deseamos, podemos guardar los pesos del modelo en un JSON o en un archivo de nuestra preferencia


```python
#model_json = model.to_json()
#with open("fashion_model.json", "w") as json_file:
#    json_file.write(model_json)
##GUARDAR LOS PESOS
#model.save_weights("fashion_model.h5")
```

## Google Maps API 馃椇

Google Maps es un servicio de mapas web desarrollado por Google. Ofrece im谩genes satelitales, fotograf铆a a茅rea, mapas de calles, vistas panor谩micas interactivas de 360 掳 de las calles, condiciones del tr谩fico en tiempo real y planificaci贸n de rutas para viajar a pie, en autom贸vil, bicicleta y aire, o en transporte p煤blico.


```python
import pandas as pd

import folium
import googlemaps
import gmaps

clinicas = pd.read_csv('ConsultasGmaps.csv', sep=',',encoding='utf_8',dtype="unicode")
clinicas
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>CLUES</th>
      <th>LATITUD</th>
      <th>LONGITUD</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>ASIMS000185</td>
      <td>21.835575</td>
      <td>-102.284527</td>
    </tr>
    <tr>
      <th>1</th>
      <td>ASSSA000960</td>
      <td>21.8463</td>
      <td>-102.711</td>
    </tr>
    <tr>
      <th>2</th>
      <td>BCIMS000460</td>
      <td>32.608992</td>
      <td>-115.3826</td>
    </tr>
    <tr>
      <th>3</th>
      <td>GTSSA016580</td>
      <td>20.5667</td>
      <td>-101.186</td>
    </tr>
    <tr>
      <th>4</th>
      <td>SRSSA017655</td>
      <td>27.048359</td>
      <td>-109.436685</td>
    </tr>
    <tr>
      <th>5</th>
      <td>TCIMS000401</td>
      <td>17.97565</td>
      <td>-92.928943</td>
    </tr>
    <tr>
      <th>6</th>
      <td>TSSSA017791</td>
      <td>23.7319</td>
      <td>-99.1469</td>
    </tr>
    <tr>
      <th>7</th>
      <td>TSSSA017803</td>
      <td>23.7683</td>
      <td>-99.1711</td>
    </tr>
    <tr>
      <th>8</th>
      <td>YNSSA013580</td>
      <td>20.3994</td>
      <td>-89.5377</td>
    </tr>
    <tr>
      <th>9</th>
      <td>ZSIMS000440</td>
      <td>22.953428</td>
      <td>-102.702333</td>
    </tr>
    <tr>
      <th>10</th>
      <td>ZSSSA012504</td>
      <td>22.7398</td>
      <td>-102.504</td>
    </tr>
  </tbody>
</table>
</div>




```python
mapa = folium.Map(
    location=[float(clinicas.iloc[0].LATITUD),
              float(clinicas.iloc[0].LONGITUD)],zoom_start=5,
)

for x in range(len(clinicas.index)):
    folium.Marker(
        location=[float(clinicas.iloc[x].LATITUD), float(clinicas.iloc[x].LONGITUD)],
        popup=clinicas.iloc[x].CLUES,
        icon=folium.Icon(color='blue', icon='asterisk')
).add_to(mapa)
    
mapa
```




```python
gmaps.configure(api_key="AIzaSyCaEFgabVDlUztxMCOfeGo3FmCpQvskmWc")
APIGoogleMaps = googlemaps.Client(key='AIzaSyCaEFgabVDlUztxMCOfeGo3FmCpQvskmWc')
```


```python
figura = gmaps.figure()

for x in range(len(clinicas)):
    if float(clinicas.iloc[x].LATITUD)==21.835575 and float(clinicas.iloc[x].LONGITUD) == -102.284527:
        continue
    RUTA = gmaps.directions_layer((21.835575,-102.284527), (float(clinicas.iloc[x].LATITUD), float(clinicas.iloc[x].LONGITUD)))
    figura.add_layer(RUTA)

figura
```


    Figure(layout=FigureLayout(height='420px'))



```python
request = APIGoogleMaps.distance_matrix((float(clinicas.iloc[0].LATITUD),float(clinicas.iloc[0].LONGITUD)), (float(clinicas.iloc[1].LATITUD), float(clinicas.iloc[1].LONGITUD)))
print(request)
```

    {'destination_addresses': ['Privada Articulo 115 Constituci贸n 912, Zona Centro, 20800 Calvillo, Ags., Mexico'], 'origin_addresses': ['Carolina Villanueva de Garc铆a 316, Cd Industrial, 20290 Aguascalientes, Ags., Mexico'], 'rows': [{'elements': [{'distance': {'text': '54.8 km', 'value': 54833}, 'duration': {'text': '52 mins', 'value': 3133}, 'status': 'OK'}]}], 'status': 'OK'}



```python
listaLugares = []
listaLugares.clear()

centro = (21.835575,-102.284527)

for x in range(len(clinicas)):
    if float(clinicas.iloc[x].LATITUD)==21.835575 and float(clinicas.iloc[x].LONGITUD) == -102.284527:
        continue
    destino = (float(clinicas.iloc[x].LATITUD), float(clinicas.iloc[x].LONGITUD))
    request = APIGoogleMaps.distance_matrix((21.835575,-102.284527), destino)
    distanciaKM = request["rows"][0]["elements"][0]["distance"]["text"]
    distanciaM = request["rows"][0]["elements"][0]["distance"]["value"]
    tiempoMinH = request["rows"][0]["elements"][0]["duration"]["text"]
    tiempoRealSeg = request["rows"][0]["elements"][0]["duration"]["value"]
    listaLugares.append([clinicas.iloc[0].CLUES,clinicas.iloc[x].CLUES,distanciaKM,distanciaM,tiempoMinH,tiempoRealSeg])
Distancias = pd.DataFrame(listaLugares, columns=["CLUES ORIGEN","CLUES DESTINO","Distancia KM","Distancia M","Tiempo Horas-Min","Tiempo Seg"])
Distancias
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>CLUES ORIGEN</th>
      <th>CLUES DESTINO</th>
      <th>Distancia KM</th>
      <th>Distancia M</th>
      <th>Tiempo Horas-Min</th>
      <th>Tiempo Seg</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>ASIMS000185</td>
      <td>ASSSA000960</td>
      <td>54.8 km</td>
      <td>54833</td>
      <td>52 mins</td>
      <td>3133</td>
    </tr>
    <tr>
      <th>1</th>
      <td>ASIMS000185</td>
      <td>BCIMS000460</td>
      <td>2,248 km</td>
      <td>2248077</td>
      <td>23 hours 52 mins</td>
      <td>85935</td>
    </tr>
    <tr>
      <th>2</th>
      <td>ASIMS000185</td>
      <td>GTSSA016580</td>
      <td>209 km</td>
      <td>209454</td>
      <td>2 hours 18 mins</td>
      <td>8265</td>
    </tr>
    <tr>
      <th>3</th>
      <td>ASIMS000185</td>
      <td>SRSSA017655</td>
      <td>1,246 km</td>
      <td>1245712</td>
      <td>14 hours 6 mins</td>
      <td>50783</td>
    </tr>
    <tr>
      <th>4</th>
      <td>ASIMS000185</td>
      <td>TCIMS000401</td>
      <td>1,226 km</td>
      <td>1226458</td>
      <td>13 hours 30 mins</td>
      <td>48582</td>
    </tr>
    <tr>
      <th>5</th>
      <td>ASIMS000185</td>
      <td>TSSSA017791</td>
      <td>499 km</td>
      <td>499373</td>
      <td>6 hours 0 mins</td>
      <td>21629</td>
    </tr>
    <tr>
      <th>6</th>
      <td>ASIMS000185</td>
      <td>TSSSA017803</td>
      <td>508 km</td>
      <td>508237</td>
      <td>6 hours 8 mins</td>
      <td>22085</td>
    </tr>
    <tr>
      <th>7</th>
      <td>ASIMS000185</td>
      <td>YNSSA013580</td>
      <td>1,772 km</td>
      <td>1771573</td>
      <td>20 hours 44 mins</td>
      <td>74636</td>
    </tr>
    <tr>
      <th>8</th>
      <td>ASIMS000185</td>
      <td>ZSIMS000440</td>
      <td>145 km</td>
      <td>145358</td>
      <td>2 hours 4 mins</td>
      <td>7419</td>
    </tr>
    <tr>
      <th>9</th>
      <td>ASIMS000185</td>
      <td>ZSSSA012504</td>
      <td>118 km</td>
      <td>118321</td>
      <td>1 hour 41 mins</td>
      <td>6079</td>
    </tr>
  </tbody>
</table>
</div>




```python
Distancias.to_csv("DistanciasGoogleMaps.csv")
```


```python
import networkx as nx 
import matplotlib.pyplot as plt 

G= nx.barabasi_albert_graph(40,15) 
nx.draw(G, with_labels=True) 
plt.show() 
```


    
![png](output_118_0.png)
    

