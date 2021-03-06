
# El lenguaje de programaci贸n Python - B谩sico 馃悹

 **<div style="text-align: right"> Samuel Arturo Garrido S谩nchez</div>**


```python
print("Hola a mundo!")  #Es costumbre entre los programadores
#(Postdata, esto es un comentario), con # se escriben
```

    Hola a mundo!


Python es un lenguaje de programaci贸n **multiparadigma**, muy 煤til para demasiadas ramas de la investigaci贸n, desarrollos y procesos. 
Su filosof铆a radica en un c贸digo legible que cualquier persona no enfocada en el 谩rea de programaci贸n, pueda comprender.

![](img/let.png)

# 驴Qu茅 es Python?

Python es un lenguaje de programaci贸n interpretado cuya filosof铆a hace hincapi茅 en la legibilidad de su c贸digo.

Se trata de un lenguaje de programaci贸n multiparadigma, ya que soporta orientaci贸n a objetos, programaci贸n imperativa y, en menor medida, programaci贸n funcional. Es un lenguaje interpretado, din谩mico y multiplataforma.

Es administrado por la Python Software Foundation. Posee una licencia de c贸digo abierto, denominada Python Software Foundation License, que es compatible con la Licencia p煤blica general de GNU a partir de la versi贸n 2.1.1, e incompatible en ciertas versiones anteriores.

![](img/python.jpg)

### Las ventajas de Python pueden ser muchas pero en las que destacan:

- La cantidad de bibliotecas que contiene, tipos de datos y funciones incorporadas en el propio lenguaje, que ayudan a realizar muchas tareas habituales sin necesidad de tener que programarlas desde cero.

- La sencillez y velocidad con la que se crean los programas. Un programa en Python puede tener de 3 a 5 l铆neas de c贸digo menos que su equivalente en Java o C.

- La cantidad de plataformas en las que podemos desarrollar, como Unix, Windows, OS/2, Mac, Amiga y otros.

- Adem谩s, Python es gratuito, incluso para prop贸sitos empresariales.

### Filosof铆a Python

La filosof铆a que rigen las personas que de sean programar en Pythonn est谩n escritas en The Zen of Python (PEP 20), que incluye:

- Hermoso es mejor que feo
- Expl铆cito es mejor que impl铆cito
- Simple es mejor que complejo
- Elaborado es mejor que complicado
- La legibilidad cuenta.

## Y a todo esto, 驴c贸mo se instala?

### Windows

https://www.python.org/downloads/windows/. 

Click en el enlace "Latest Python 3 Release -Python x.x.x". Si tu ordenador ejecuta la versi贸n de 64 bits de Windows, descarga Windows x86-64 executable installer. De lo contrario, descarga Windows x86 executable installer. Despu茅s de descargar el instalador, deber铆as ejecutarlo (d谩ndole doble click) y seguir las instrucciones.

Una cosa para tener en cuenta: Durante la instalaci贸n, ver谩s una ventana de "Setup". Aseg煤rate de marcar las casillas "Add Python 3.6 to PATH" o "Add Python to your environment variables" y hacer click en "Install Now", como se muestra aqu铆 (puede que se vea un poco diferente si est谩s instalando una versi贸n diferente)

![](img/windows.png)

### Mac

Si has utilizado GNU/Linux alguna vez habr谩s escuchado la palabra sistema de gestor de paquetes. En macOS se cuenta con ello tambi茅n, para poder instalar componentes extras a nuestro ordenador.

![](img/scr4.png)

En escencia para instalar **Python, PHP nativo, MySQL**, y entre m谩s cosas como kits para desarrollar entre otras podr谩n ser descargadas solo con el comando:


```console
MacBook-Pro-de-Sam:~$ brew install <Lo que quieras instalar>
```

Para poder instalar homebrew necesitar谩s colocar 茅sto en tu terminal. Lo usaremos mucho en 茅ste curso y lo usar谩s mucho si ser谩s desarrollador en general.

```console
MacBook-Pro-de-Sam:~$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

En nuestro caso, una vez instalado Homebrew en nuestra Mac, en la terminal insertaremos: brew install python.
Y se instalar谩 autom谩ticamente.

### Linux


Para los Pro, dependiendo la distribuci贸n de linux que tengan, **Fedora, Ubuntu, OpenSUSE**.

En la terminal colocan el comando:

#### Debians (Ubuntu, Mint, etc.) 
```console
:~$ sudo apt-get install python3
```

#### Fedora
```console
:~$ sudo dnf install python3
```

#### OpenSUSE
```console
:~$ sudo zypper install python3
```

## 驴Y qui茅n desarroll贸 todo esto? 鉂わ笍

<p>
  <img src="img/Guido.jpg" align = "right"  width="130" />
</p>

Python fue creado a finales de los ochenta3 por **Guido van Rossum** en el Centro para las Matem谩ticas y la Inform谩tica (CWI, Centrum Wiskunde & Informatica), en los Pa铆ses Bajos, como un sucesor del lenguaje de programaci贸n ABC, capaz de manejar excepciones e interactuar con el sistema operativo Amoeba.

**El nombre del lenguaje proviene de la afici贸n de su creador por los humoristas brit谩nicos Monty Python.**

Van Rossum es el principal autor de Python, y su continuo rol central en decidir la direcci贸n de Python es reconocido, refiri茅ndose a 茅l como Benevolente Dictador Vitalicio (en ingl茅s: Benevolent Dictator for Life, BDFL)

## Ejemplos de uso de Python

### 脕lgebra: Soluci贸n a un sistema de ecuaciones

Podemos usar Python para encontrar la soluci贸n a un sistema de ecuaciones.

Tenemos el siguiente sistema de ecuaciones:

<img src="https://render.githubusercontent.com/render/math?math=2x+y-3z=7">
<img src="https://render.githubusercontent.com/render/math?math=5x-4y+z=-19">
<img src="https://render.githubusercontent.com/render/math?math=x-y-4z=4">

Buscaremos la soluci贸n del sistema a trav茅s de python con uso de matrices.


```python
import numpy as np                            #Importar una biblioteca
A = np.matrix([[2,1,-3],[5,-4,1],[1,-1,-4]])  #Matriz A
B = np.matrix([[7],[-19],[4]])                #Matriz B
X = A**(-1)*B                                 #Inversa de matriz A por B
print("El resultado es: \n",X)                #Impresi贸n de la soluci贸n
```

    El resultado es: 
     [[-1.]
     [ 3.]
     [-2.]]


### Crear ventanas: Interfaz gr谩fica

Podemos importar Tkinter que nos permite la creaci贸n de entornos gr谩ficos tales como botones, ventanas, textfields, etc, aunque tendremos que definir desde lo que contendr谩n 茅stos elementos hasta su posici贸n x, y.


```python
from tkinter import *
from tkinter import ttk

def calculate(*args):
    try:
        value = float(feet.get())
        meters.set(int(0.3048 * value * 10000.0 + 0.5)/10000.0)
    except ValueError:
        pass

root = Tk()
root.title("Pies a Metros")

mainframe = ttk.Frame(root, padding="3 3 12 12")
mainframe.grid(column=0, row=0, sticky=(N, W, E, S))
root.columnconfigure(0, weight=1)
root.rowconfigure(0, weight=1)

feet = StringVar()
meters = StringVar()

feet_entry = ttk.Entry(mainframe, width=7, textvariable=feet)
feet_entry.grid(column=2, row=1, sticky=(W, E))

ttk.Label(mainframe, textvariable=meters).grid(column=2, row=2, sticky=(W, E))
ttk.Button(mainframe, text="Calcula", command=calculate).grid(column=3, row=3, sticky=W)

ttk.Label(mainframe, text="Pies").grid(column=3, row=1, sticky=W)
ttk.Label(mainframe, text="es equivalente a").grid(column=1, row=2, sticky=E)
ttk.Label(mainframe, text="metros").grid(column=3, row=2, sticky=W)

for child in mainframe.winfo_children(): child.grid_configure(padx=5, pady=5)

feet_entry.focus()
root.bind('<Return>', calculate)

root.mainloop()
```

### Buscador de palabras: Expresiones regulares

Dentro del mundo del big data y miner铆a de datos, la b煤squeda de elementos dentro de grandes archivos es escencial. RE se encarga de esto.


```python
import re
texto = "En esta cadena existe una palabra magica"
print(re.search("magica",texto))
print(re.search("hola",texto))


# Match en palabras dentro de Strings
```

    <_sre.SRE_Match object; span=(34, 40), match='magica'>
    None


### Gr谩ficas

Para el 谩rea de ciencias e ingenier铆as, los grafos son instrumentos escenciales para poder dar una interpretaci贸n de imagen a un fen贸meno, de esta manera, la mente humana pueda analizar mejor dicha informaci贸n.


```python
from matplotlib import pyplot

## Para que nos muestre la gr谩fica en Jupyter debemos agregar:
%matplotlib inline

def f(x):
    y = x**2
    return y

x = range(-10,11)
pyplot.plot(x, [f(i) for i in x])
print("Gr谩fica de f(x) = x^2")
pyplot.show()
```

    Gr谩fica de f(x) = x^2



![png](img/output_29_1.png)


## Python es usado para much铆simas otras cosas como: 

* Creaci贸n de modelos predictivos (Machine Learning).
* Creaci贸n de Sockets (comunicaci贸n entre computadores).
* Creaci贸n del backend de p谩ginas web con Django.
* Inteligencia Artificial
* Realizar simulaciones de fen贸menos f铆sicos
* Scripts que ayudan al funcionamiento de muchos programas que usamos (Mac OS tiene Python 2.7 de f谩brica, Linux tiene versiones 3.* en todos sus sabores (distros))
* **Y mucho, muuuuchooo m谩s**



# <center> 馃枼   驴Qu茅 esperamos?   馃枍 </center>

## Tipos de "datos" - (objetos)

En Python, todas las **variables son objetos**. Todas las cosas que "declaremos", que reside en alg煤n lugar de la memoria, posee un identificador 煤nico que lo diferencia del resto. Piensa en 茅l como si fuera su INE. Para conocer ese identificador, Python dispone de la funci贸n id().


```python
numero = 6.989796967
id(numero)
print(id(numero))
```

    5064301184


**Al contrario de otros lenguajes de programaci贸n como Java, no es necesario declarar el tipo de variable que se crea.**

Los tipos de datos primitivos no existen como tal en Python, sin embargo podemos saber el tipo de dato que contiene una variable con el m茅todo type(dato)


```python
# Los enteros
opcion = 5 
print(opcion)
type(opcion)
```

    5





    int



Una cadena o String es un tipo de dato que guarda una oraci贸n o conjunto de letras, s铆mbolos y n煤meros para tratarlo como uno solo. En C en cambio un "String" en realidad es un arreglo de caracteres.


```python
saludo = str("Hola")
print(saludo)
saludo1 = "Las saladitas son horneadas"
print(saludo1)
```

    Hola
    Las saladitas son horneadas



```python
#Floats
# ESto es un comentario


enunciado = "Un autom贸vil se movi贸 1135.67 metros en 140.86 segundos. Calcule su velocidad"

distancia = 1135.67
tiempo = 140.86 

velocidad = distancia/(tiempo**2)

print(enunciado)
print("\n \t La velocidad del autom贸vil fue:",velocidad,"m/s")
```

    Un autom贸vil se movi贸 1135.67 metros en 140.86 segundos. Calcule su velocidad
    
     	 La velocidad del autom贸vil fue: 0.05723698981504439 m/s


### Operadores y comparadores matem谩ticos

Dentro de la programaci贸n existe mucha l贸gica. Varios elementos de comparaci贸n en matem谩ticas como lo es <, >, 鈮?, 鈮?, 鈮?(!=), o alg煤n m茅todo dentro de los objetos tienen la funci贸n de devolver un elemento **BOOLEANO** (BOOLEANO: TRUE OR FALSE). Nos devuelve este booleano para determinar si es cierto o falso el enunciado.

Adem谩s de los cl谩sicos operadores matem谩ticos descritos por los siguientes s铆mbolos:

- \+ : Suma
- \- : Resta
- \* : Producto
- / : Divisi贸n
- // : Divisi贸n entera 
- % : M贸dulo o residuo 



```python
a = 6
b = 5
c = 5
print("La suma a+b es: "+str(a)+" + "+str(b)+" = ",a+b)
print("La resta a-b es: "+str(a)+" - "+str(b)+" = ",a-b)
print("El producto a*b es: "+str(a)+" * "+str(b)+" = ",a*b)
print("El cociente a/b es: "+str(a)+"/"+str(b)+" = ",a/b)
print("El cociente entero a/b es: "+str(a)+"//"+str(b)+" = ",a//b)
print("El m贸dulo o residuo a%b es: "+str(a)+"%"+str(b)+" = ",a%b)


## OJO:
## =  1 signo significa asignaci贸n, 
## == doble significa preguntar si son iguales a python

print("\n")
print("驴a es igual a b?",a == b) 
print("驴b es igual a c?",b == c)
print("驴a es menor que 5?",a<5)
print("驴b es mayor a c?",b>c)
print("驴c es diferente de 6?",c!=6)

# No solamente se pueden comparar n煤meros, tambi茅n cadenas de texto

texto1 = "Hola"
texto2 = "Hola"
print("驴texto1 es igual a texto2?",texto1 == texto2)
## Tener cuidado al comparar strings de esta manera, se recomienda 
## funciones especializadas.
```

    La suma a+b es: 6 + 5 =  11
    La resta a-b es: 6 - 5 =  1
    El producto a*b es: 6 * 5 =  30
    El cociente a/b es: 6/5 =  1.2
    El cociente entero a/b es: 6//5 =  1
    El m贸dulo o residuo a%b es: 6%5 =  1
    
    
    驴a es igual a b? False
    驴b es igual a c? True
    驴a es menor que 5? False
    驴b es mayor a c? False
    驴c es diferente de 6? True
    驴texto1 es igual a texto2? True


#### 驴Qu茅 sucede aqu铆?


```python
par = 11%2
par == 0
## La primera l铆nea le asigna el valor 1 a par, la segunda lo compara con 0
```




    False



#### Ejercicio: Quitar la variable de "puedoSalirAlCine" pero obtener el mismo resultado


```python
puedoSalirAlCine = bool() # 驴Por qu茅 no viene al caso hacer 茅sto?
tareas = 9 # Un control de flujo if/else -> pr贸xima clase
if tareas < 8:
    if puedoSalirAlCine:
        print("Yeih! 馃榿")
    else:
        print("No yeih 鈽癸笍")
        puedoSalirAlCine = False
else:
    print("Me voy 馃槑")
    puedoSalirAlCine = True
```

    Me voy 馃槑


#### 驴Y c贸mo ingreso elementos a la ejecuci贸n (a manera de Scanner)?

Si queremos realizar la selecci贸n por casos, en Python no contamos con un Switch case pero podemos usar `elif`


```python
numeroInsertado = int(input("Ingrese un n煤mero: ")) # 驴Por qu茅 el int al principio? Pista: String
if numeroInsertado  < 5:
    print("馃榾")
elif numeroInsertado < 10: #O elif?
    print("猸愶笍")
    
elif numeroInsertado < 30:
    print("馃崁")
else:
    print("Es m谩s grande que 30")
```

    Ingrese un n煤mero: 20
    馃崁


### PALABRAS RESERVADAS: (IMPORTANTE) 鈿狅笍 鈥硷笍

Las palabras reservadas son un conjunto de palabras que **NO** podremos usar como nombre de nuestas variables ya que python sabe que tiene que realizar ciertas acciones si se encuentra con alguna de 茅stas palabras. Entre las cuales podemos encontrar:

- and
- if
- del
- else
- for
- elif
- is
- from
- raise
- lambda
- assert
- return
- break
- global
- not
- try
- class
- except
- or
- while
- continue
- exec
- import
- yield
- def
- finally
- print

**No vayan a intentar usar alguna de 茅stas palabras como nombre de sus variables o no funcionar谩 su programa**

## Operadores l贸gicos. 馃悵

Los operadores l贸gicos son los que trabajan con valores booleanos, nos devuelven falso o verdadero y son la escencia de las condiciones. 

### Operador AND

El operador and eval煤a si las condiciones TODAS se cumplen:


```python
True and False
```




    False



Podemos combinar varios operadores AND dentro de la sentenia if, pero tener en cuenta que todas las condiciones deber谩n ser ciertas para ejecutar el bloque de c贸digo que contiene el condidicional o mandarlo para el bloque else.


```python
examenes = int(input("Ingrese el n煤mero de ex谩menes: "))
tareas = int(input("Ingrese el n煤mero de tareas: "))
participaciones = int(input("Ingrese el n煤mero de participaciones: "))

if examenes >= 10 and tareas >=10 and participaciones >=10:
    print("Podr谩s ir a la peda")
else:
    print("H铆jole creo que no se va a poder")
```

    Ingrese el n煤mero de ex谩menes: 10
    Ingrese el n煤mero de tareas: 20
    Ingrese el n煤mero de participaciones: 40
    Podr谩s ir a la peda


### Operador OR

El operador **or** eval煤a si **ALGUNO** DE LOS VALORES ES VERDADERO


```python
tengoPaseFiesta = False
miCompaTiene = True

if tengoPaseFiesta or miCompaTiene:
    print("Podemos pasar")
else:
    print("Nos quedamos fuera")
```

    Podemos pasar



```python
edad = 18
dinero = 10000
fama = 80 #supongamos que se mide del 1 al 100

if edad >= 18 or dinero >= 1000 or fama >= 50:
    print("Ya llegu茅 paps")
else:
    print("No te preocupes pr铆ncipe, ah铆 para la otra")
```

    Ya llegu茅 paps


### Operador NOT

El operador **not** devuelve el valor opuesto al valor booleano.


```python
print(not True)
```

    False



```python
mayonesa1 = "Hellmans"
mayonesa2 = "Nestl茅"

if mayonesa1 is not "McCORMICK":
    print("Un toque del sabor de mayonesa McCORMICK")
    
if mayonesa2 != "McCORMICK":
    print("Un toque del sabor de mayonesa McCORMICK")
```

    Un toque del sabor de mayonesa McCORMICK
    Un toque del sabor de mayonesa McCORMICK


**Aqu铆 aparece una situaci贸n.** 鈿狅笍

Es bastante frecuente que se use de sin贸nimos a **is** y **==** o **is not** con **!=**. 

Aunque suelen funciona de forma similar sus comportamientos no son exactamente iguales. 

**is** devolver谩 TRUE si las 2 variables apuntan al mismo objecto.

**==** devolver谩 TRUE si los valores de las variables son iguales.



```python
a = 1000
b = 999
```


```python
print("驴a es b+1?",a is b + 1)
```

    驴a es b+1? False



```python
print("驴a continene un valor igual a b+1?",a == b + 1)
```

    驴a continene un valor igual a b+1? True


### 驴Se pueden combinar todo lo visto hasta ahora? S铆


```python
a = 5==5 
b = True
c = 5 is not 7

if not((a or b) and c):
    print("Ya les dio calambre cerebral?")
else:
    print("Todav铆a")
```

    Todav铆a


#### Para mayor informaci贸n de c贸mo tratar con los booleanos existe algo llamado 谩lgebra relacional que tiene mucho que ver con los componentes el茅ctricos y el茅ctronicos que usamos todos los d铆as, desde una lavadora hasta gr煤as. 

Un ejemplo de una tabla de verdad es la siguiente y los posibles resultados que ponemos obtener solo de 2 variables.

![](img/Tabla_de_verdad.png)

## Colecciones 馃悊

Una colecci贸n permite agrupar varios objetos bajo un mismo nombre. El equivalente a las listas, tuplas y diccionarios en otros lenguajes de programaci贸n son ArrayList, SetMaps o Maps, Sets, etc., la ventaja y desventaja si es usado incorrectamente de Python es que cualquier colecci贸n de elementos puede contener cualquier elemento ya que todos son objetos en realidad(wrappers).

En Python existen tres colecciones b谩sicas.

- Listas `[ ]`
- Tuplas `( )`
- Diccionarios `{ }`


```python
listaEjemplo = [1,2,3]
tuplaEjemplo = (4,5,6)
diccionarioEjemplo = {7:"Hola",8:"Gracias",9:"Adi贸s"}

listaMixta = [1,"Hola",True,3.1416,[2,"Polo"]]
tuplaMixta = ("Jaja",False,4<7,("Hola",1,2))
diccionarioMixto = {True:"Hola",2:5.3,1:"Fin"}

mixto = [1,{1:2},3,([4,"5"],6.6,(7<8,9!=10),11,{12:13,14:[15,"16 17","18.8"]},19),20]
```

#### Mutabilidad 馃悰馃

La mutabilidad radica si un elemento dentro de un objeto o el objeto mismo puede cambiar alg煤n atributo que posea. Si es mutable, podemos hacer el cambio, en caso contrario recibiremos un error.

### Listas 馃悳

Son colecciones de elementos que permiten la mutabilidad de elementos. Se delimitan por corchetes `[ ]`

Existen una serie de funciones que nos permiten interactuar con una lista. 
Para una funci贸n solo agregamos a la lista un punto, seguido de la funci贸n y sus par谩metros.     

**lista.funcion(par谩metro)**

**OJO:** Los 铆ndices de las listas comienzan desde el 0, quiere decir que si nos queremos referir al primer elemento de la lista diremos que est谩 en la posici贸n 0.

**M茅todos importantes:**

- `append(x):` Agrega un elemento x al final de la lista.
- `insert(i, x):` Agrega un elemento x en la posici贸n i que le indiquemos.
- `remove(x):` remueve 1 elemento x de la lista. 
- `pop( ):` Nos remueve el 煤ltimo de la lista pero igual nos permite saber cu谩l fue.
- `clear( ):` Remueve todos los elementos de la lista.
- `index(x):` Nos devuelve el 铆ndice o posici贸n de la primer coincidencia de un elemento con x.
- `count(x):` Cuenta cu谩ntos elementos x hay en la lista.
- `sort( ):` Ordena la lista de menor a mayor con n煤meros o alfab茅ticamente con Strings.
- `len( ):` Calcula la cantidad de elementos o longitud de la lista.


```python
## Aqu铆 tenemos una lista, se puede diferenciar de los dem谩s porque tiene [ ] corchetes

lista = [4, 8, 16, 43, 23, 300, 44, 76, 65,44,44]

## Removemos solo 1 elemento 44
lista.remove(44)
print("Lista despu茅s de remover un 44: ",lista)

## Para acceder a un elemento en determinada posici贸n, 
## colocaremos el nombre de la lista y entre corchetes el 铆ndice
## Ejemplo: lista[0] -> Elemento en la lista en la pos. 0 

print("Elemento en la posici贸n 8 de lista: ",lista[8])

lista.append(100)
print("Lista despu茅s de agregar 100 al final:",lista)

lista.insert(2,5)
print("Lista despu茅s de insertar 5 en la pos. 2: ",lista)

print("Tama帽o lista:",len(lista), ", lista: ",lista)

print("El n煤mero 23 se encuentra en la posici贸n: ",lista.index(44))

lista.sort()
print("Lista ordenada: ",lista)
```

    Lista despu茅s de remover un 44:  [4, 8, 16, 43, 23, 300, 76, 65, 44, 44]
    Elemento en la posici贸n 8 de lista:  44
    Lista despu茅s de agregar 100 al final: [4, 8, 16, 43, 23, 300, 76, 65, 44, 44, 100]
    Lista despu茅s de insertar 5 en la pos. 2:  [4, 8, 5, 16, 43, 23, 300, 76, 65, 44, 44, 100]
    Tama帽o lista: 12 , lista:  [4, 8, 5, 16, 43, 23, 300, 76, 65, 44, 44, 100]
    El n煤mero 23 se encuentra en la posici贸n:  9
    Lista ordenada:  [4, 5, 8, 16, 23, 43, 44, 44, 65, 76, 100, 300]


#### Podemos tener listas con elementos mixtas e incluso listas dentro de listas y estos dentro de listas y sucesivamente. No se recomienda hacer tanto anidamiento.


```python
lista2 = ["Hola","Adi贸s",2,False,4.5,[1,[2,3],4]]
print("Lista:",lista2)
lista2.append(6)
print("Lista despu茅s de agregar un 6: ",lista2)
print("脥ndice de 2 en la lista",lista2.index(2))
```

    Lista: ['Hola', 'Adi贸s', 2, False, 4.5, [1, [2, 3], 4]]
    Lista despu茅s de agregar un 6:  ['Hola', 'Adi贸s', 2, False, 4.5, [1, [2, 3], 4], 6]
    脥ndice de 2 en la lista 2



```python
## Algunos m茅todos como sort no se podr谩n ya que los elementos que contiene no son del mismo tipo.
lista2.sort()
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-34-71fd039ea1e5> in <module>()
          1 ## Algunos m茅todos como sort no se podr谩n ya que los elementos que contiene no son del mismo tipo.
    ----> 2 lista2.sort()
    

    TypeError: '<' not supported between instances of 'int' and 'str'


### Tuplas 馃悽

Como las listas, las tuplas siguen la misma estructura. Son id茅nticas a las listas pero con una peque帽a excepci贸n: **NO son mutables**.

Si tratamos de cambiar alg煤n elemento por otro o eliminar, nos marcar谩 un error.

**M茅todos importantes:**

- `index(x):` Nos devuelve el 铆ndice o posici贸n de la primer coincidencia de un elemento con x.
- `count(x):` Cuenta cu谩ntos elementos x hay en la tupla.
- `len( ):` Calcula la cantidad de elementos o longitud de la tupla.


```python
tupla = (16,53,23,76,98,43,43,56,99,77,21,32) #Se usan par茅ntesis en lugar de corchetes ()


## Para acceder a un elemento en determinada posici贸n, 
## colocaremos el nombre de la tupla y entre corchetes [] el 铆ndice
## Ejemplo: tupla[0] -> Elemento en la lista en la pos. 0 

print("Elemento en la posici贸n 1:",tupla[1])

print("Cantidad de 43 en la tupla:",tupla.count(43))

print("Cantidad de elementos o tama帽o de la tupla:",len(tupla))
```

    Elemento en la posici贸n 1: 53
    Cantidad de 43 en la tupla: 2
    Cantidad de elementos o tama帽o de la tupla: 12



```python
tupla.append(100)
tupla.sort()
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    <ipython-input-2-59e97cb5c63b> in <module>()
    ----> 1 tupla.append(100)
          2 tupla.sort()


    AttributeError: 'tuple' object has no attribute 'append'


> Los errores generados son gracias a que quer铆amos modificar una tupla, la cual no tiene el m茅todo pop,sort,append,insert o similares, que modifican a la misma. Solo podemos usar m茅todos que no manipulen su estructura.

**Y a todo 茅sto... 驴Para qu茅 necesitamos tuplas si tenemos listas?** 

Razone el siguiente ejemplo, 驴qu茅 est谩 pasando?


```python
x = [1,2,3,4,5]
y = x
print(y)
```

    [1, 2, 3, 4, 5]



```python
x[0] = 10
print(y)
```

    [10, 2, 3, 4, 5]



```python
id(x) == id(y)
```




    True




```python
z = (1,2,3,4,5)
y = z
x[1] = 50
print(x)
print(y)
print(z)

p = (1,2)
q = [1,2]

p is q
```

    [10, 50, 3, 4, 5]
    (1, 2, 3, 4, 5)
    (1, 2, 3, 4, 5)





    False



### Diccionarios 馃

Los diccionarios son lo equivalente a tablas Hash, a cada llave se le asigna un valor. 

De manera sencilla podemos dar un ejemplo: 

Tenemos un bur贸 con muchos cajones, en los cajones podemos guardar cosas que en este caso ser谩n variables y cuando queramos buscar una crema en el bur贸, naturalmente tendremos qu茅 saber en qu茅 caj贸n est谩. Los cajones tienen una referencia (el caj贸n de abajo por ejemplo) y en el caso de los diccionarios, las llaves son los cajones y guardan variables. 

Los diccionarios se escriben entre`{}` llaves y llevan la estructura `{llave:valor,llave:valor,llave:valor}`

**M茅todos importantes:**

- `clear()`: Elimina todos los elementos del diccionario
- `copy()`: Devuelve una copia del diccionario
- `fromkeys(x,y)`: Devuelve un diccionario con las claves y el valor especificados
- `get(x)`: Devuelve el valor de la clave especificada
- `items()`: Devuelve una lista que contiene una tupla para cada par clave-valor
- `keys()`: Devuelve una lista que contiene las claves del diccionario
- `pop(x)`: Elimina el elemento con la clave especificada
- `popitem()`: Elimina el 煤ltimo par clave-valor insertado
- `setdefault()`: Devuelve el valor de la clave especificada. Si la clave no existe: inserte la clave, con el valor especificado
- `update(x,y)`: Actualiza el diccionario con los pares clave-valor especificados
- `values()`: Devuelve una lista de todos los valores del diccionario.


```python
miPrimerDiccionario = {1:"Hola",2:"Adi贸s"}
print("Valor de llave 1: ",miPrimerDiccionario[1])

print("Las llaves que tiene mi diccionario:",miPrimerDiccionario.keys())
print("Las cosas que tiene que mi diccionario:",miPrimerDiccionario.items())
```

    Valor de llave 1:  Hola
    Las llaves que tiene mi diccionario: dict_keys([1, 2])
    Las cosas que tiene que mi diccionario: dict_items([(1, 'Hola'), (2, 'Adi贸s')])



```python
miDiccionario = {"Hola":[(1,2),6,7,True],"verde":"kiwi","amarillo":"platano","amarillo":"Adi贸s"}
```


```python
print(miDiccionario["amarillo"])
print("Para acceder al 2 dentro de miDiccionario: ",miDiccionario["Hola"][0][1])
```

    Adi贸s
    Para acceder al 2 dentro de miDiccionario:  2



```python
##Podemos definir diferentes tipos de objetos para que sea nuestra clave valor, incluso hacer diccionarios de tuplas de listas
dic = {False:[1,True,2.3,"Hola"],1:"Poco"}

print(dic[False])
```

    [1, True, 2.3, 'Hola']



```python
baseDatos = {
    1: {
        "nombre":"Samuel",
        "apellido":"Garrido",
        "NumCuenta":418045231
    },
    2: {
        "nombre":"Alicia",
        "apellido":"Carballido",
        "NumCuenta":423154132
    },
    3: {
        "nombre":"Alejandro",
        "apellido":"Barreiro",
        "NumCuenta":432131523
    },
    4: {
        "nombre":"Ana",
        "apellido":"Lagunas",
        "NumCuenta":462314263
    }
}

for x in baseDatos:
    print(str(baseDatos[x]['NumCuenta'])+": "+baseDatos[x]['nombre']+" "+baseDatos[x]['apellido'])
```

    418045231: Samuel Garrido
    423154132: Alicia Carballido
    432131523: Alejandro Barreiro
    462314263: Ana Lagunas


Como podemos ver, se hace una colecci贸n de elementos para podernos referirnos a 茅stos m谩s adelante por otro nombre o con una llave.

**Hasta 茅ste momento:**
## <center> [ ] corchetes para listas -> mutable</center>
## <center> ( ) par茅ntesis para tuplas -> inmutable </center>
## <center> { } llaves para diccionarios -> cajones </center>


```python
profesores = ["Laura","Samuel","Hola"]
if profesores[0] == "Laura":
    print("Laura se encuentra en la posici贸n: ",profesores.index("Laura"))
if len(profesores) == 3:
    print("Hay 3 profesores en el curso")
else:
    profesores.append("Fulano")
    print(profesores)
```

    Laura se encuentra en la posici贸n:  0
    Hay 3 profesores en el curso



```python
arreglo = [1,2,3,4,5]
if arreglo[1]*arreglo[2] == 2:
    print(2)
elif arreglo[3]*arreglo[2] == 12:
    print(12)
elif arreglo[1]*arreglo[3] == 8: # 驴Qu茅 pasar铆a si reemplazo elif por if?
    print(8)
else:
    print(0)
```

    12


## Ciclos 馃寑

Los ciclos nos permiten hacer repeticiones de procesos dentro de un rango que nosotros determinemos. 

Esto es 煤til para NO hacer cada uno de los pasos si son repetitivos, por lo que har铆amos l铆neas de c贸digo innecesarias. (Adem谩s, 隆qu茅 flojera!)

### Ciclo for (para cada) 鉃?

Los ciclos for en python funcionan tienen una estructura algo distinta en Python que por ejemplo C o Java. Para poder utilizarlo tendremos que hacer uso de la palabra reservada **in** y luego a decisi贸n,

La funci贸n `range()` nos devuelve un arreglo de n煤meros.

Si range(x) le insertamos solo 1 par谩metro, **"x"** simboliza el punto de llegada -1 desde 0 de 1 en 1.

Si a range(x,y) le insertamos 2 par谩metros, **"x"** simboliza el punto de partida y **"y"** el punto de llegada -1 y va contando de 1 en 1 hasta llegar.

Si a range(x,y,z) le insertamos 3 par谩metros, **"x"** simboliza el punto de partida, **"y"** el punto de llegada -1 y z de cuanto en cu谩nto va salteando.


```python
jaja = [1,4,6,8]
jaja.append(1)
jaja.append(2)
jaja.append(3)
print(jaja)
```

    [1, 4, 6, 8, 1, 2, 3]



```python
listaNormal = []

for numeroInsertar in range(-4,-60,-2):
        listaNormal.append(numeroInsertar)

print(listaNormal)
```

    [-4, -6, -8, -10, -12, -14, -16, -18, -20, -22, -24, -26, -28, -30, -32, -34, -36, -38, -40, -42, -44, -46, -48, -50, -52, -54, -56, -58]



```python
a = range(10)
b = range(-10,10)
c = range(-10,10,2)

print("Primer ciclo")
for i in a:
    print(i)

print("\nSegundo ciclo")
for i in b:
    print(i)

print("\nTercer ciclo")
for i in c:
    print(i)
```

    Primer ciclo
    0
    1
    2
    3
    4
    5
    6
    7
    8
    9
    
    Segundo ciclo
    -10
    -9
    -8
    -7
    -6
    -5
    -4
    -3
    -2
    -1
    0
    1
    2
    3
    4
    5
    6
    7
    8
    9
    
    Tercer ciclo
    -10
    -8
    -6
    -4
    -2
    0
    2
    4
    6
    8


**Los ciclos for pueden implementarse con range() o con una colecci贸n (lista, tupla o diccionario) para que sea recorrido. No es necesario colocar contadores adicionales.** 


```python
for i in [1,5,9,2,6,9,0]:
    print(i)
```

    1
    5
    9
    2
    6
    9
    0



```python
jaja2 = [1,4,6,8]
for i in range(0,3,1): # 驴C贸mo modifico 茅sto para que sea m谩s sencillo?
    jaja2.append(i)
print(jaja2)
```

    [1, 4, 6, 8, 0, 1, 2]



```python
## Para recorrer un diccionario el for ir谩 recorriendo las llaves, ser谩 nuestro deber colocar
## el nombre del diccionario con la clave para que nos traiga el valor.

frutas = {'Fresa':'Roja','Lim贸n':'Verde','Papaya':'Naranja','Manzana':'amarilla','Guayaba':'rosa'}
for llave in frutas:
    print(llave, 'es de color', frutas[llave])
    
```

    Fresa es de color Roja
    Lim贸n es de color Verde
    Papaya es de color Naranja
    Manzana es de color amarilla
    Guayaba es de color rosa


## Ciclos while 鉃?

El ciclo while permite ejecutar un bloque de instrucciones mientras se cumpla la condici贸n dada. Primero comprueba que en efecto se cumple la condici贸n dada y entonces, ejecuta el segmento de c贸digo correspondiente hasta que la condici贸n no se cumpla.


```python
numero = 0
while numero <= 10:
    print(numero)
    numero += 1
```

    0
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


### Ejercicio: 驴Qu茅 sucede en estos 2 casos?


```python
nombre = ""

while not nombre:
    nombre = input('Escribe tu nombre: ')
```

    Escribe tu nombre: Samuel



```python
while True:
    entrada = input('Escibe tu nombre: ')
    if not entrada: 
        break
```

    Escibe tu nombre: 


## Controles de bucles 馃洃 鈿狅笍

### Break:  Rompe el ciclo en determinada condici贸n


```python
for number in range(10):
    if number == 5:
        break    # se rompe al contar a 5
    print('El n煤mero es: ',number) 
print('Se muri贸')
```

    El n煤mero es:  0
    El n煤mero es:  1
    El n煤mero es:  2
    El n煤mero es:  3
    El n煤mero es:  4
    Se muri贸



```python
ejemplo = 0
## Un ciclo infinito puede darse con while True
while True:   
    if ejemplo == 6:
        break
    print(ejemplo)
    ejemplo += 1
```

    0
    1
    2
    3
    4
    5


### Continue: Omite o anula la ejecuci贸n del c贸digo debajo de 茅l en caso de una condici贸n pero se va a la siguiente iteraci贸n. No rompe el ciclo


```python
for numero in range(10):
    if numero == 5 or numero == 4:
        continue    # No imprime ni el 5 ni el 4
    print(numero)
```

    0
    1
    2
    3
    6
    7
    8
    9


### Pass: Operaci贸n nula, o sea que no pasa nada cuando se ejecuta. 

Se utiliza cuando se requiere por sintaxis una declaraci贸n pero no se quiere ejecutar ning煤n comando o c贸digo. Tambi茅n se utiliza en lugares donde donde el c贸digo ir谩 finalmente, pero no ha sido escrita todav铆a o se quisiera hacer un debug del programa


```python
for number in range(10):
    if number == 5:
        print("Hola")
        pass
        print("Adi贸s")
    print('N煤mero: ' + str(number))
```

    N煤mero: 0
    N煤mero: 1
    N煤mero: 2
    N煤mero: 3
    N煤mero: 4
    Hola
    Adi贸s
    N煤mero: 5
    N煤mero: 6
    N煤mero: 7
    N煤mero: 8
    N煤mero: 9


### Listas por comprensi贸n 馃

No, no es comprender literalmente las listas o tuplas o lo que sea, significa que podemos ahorrarnos unas l铆neas de c贸digo escribiendo o creando una lista con un for dentro. Veamos un ejemplo:


```python
saludo = "ola ke ace"
print(saludo)
## Primero como par茅ntesis: el m茅todo capitalize pone la primera letra en may煤scula
print(saludo.capitalize())
```

    ola ke ace
    Ola ke ace



```python
## TODA ESTAS L脥NEAS DE C脫DIGO

lenguajes = ["python", "c", "c++", "java","swift","kotlin","c#","shell","php","js"]
lenguajesEnMayusculas = []

for cadaUno in lenguajes:
    lenguajesEnMayusculas.append(cadaUno.capitalize())

print(lenguajesEnMayusculas)
```

    ['Python', 'C', 'C++', 'Java', 'Swift', 'Kotlin', 'C#', 'Shell', 'Php', 'Js']



```python
## PODEMOS REDUCIRLO A 脡STO

otraVezEnMayusculas = [cadaLenguaje.capitalize() for cadaLenguaje in lenguajes]
print(otraVezEnMayusculas)
```

    ['Python', 'C', 'C++', 'Java', 'Swift', 'Kotlin', 'C#', 'Shell', 'Php', 'Js']


Por ejemplo, quiero una lista con todos los n煤meros al cuadrado, podemos hacerlo con una lista de comprensi贸n


```python
numeros = [1, 2, 3, 4, 5]
alcuadrado = [n ** 2 for n in numeros]
print(alcuadrado)
```

    [1, 4, 9, 16, 25]


## Preparados listos: Funciones 猸愶笍

Una funci贸n es un bloque de c贸digo con un nombre asociado, que recibe cero o m谩s argumentos como entrada, sigue una secuencia de sentencias, la cuales ejecuta una operaci贸n deseada y devuelve un valor y/o realiza una tarea.

La sentencia def es una definici贸n de funci贸n usada para crear objetos funciones definidas por el usuario.


```python
 def hola(nombre):   # def: Se utiliza siempre que queramos definir una funci贸n
        print("Hola", nombre, "!")
```


```python
hola("Alicia")
```

    Hola Alicia !


### 驴C贸mo se le conoce a lo que va entre par茅ntesis? 
Al definir una funci贸n los valores los cuales se reciben se denominan par谩metros, pero durante la llamada los valores que se env铆an se denominan argumentos


```python
def suma(a,b): ## Aqu铆 a y b se le conoce como par谩metros
    print(a+b)

suma(5,2) ## aqu铆 a 5 y 2 se le denomina argumentos
```

    7



```python
def f(x,y):
    print(x**2 + 2*x + 1 + y**2)

f(2,4)
```

    25


### Valores de retorno
Qu茅 tal si queremos lo que suceda dentro de la funci贸n para otras cosas, no s茅 digamos que hace una operaci贸n matem谩tica y queremos el resultado para otras cuentas. Existe algo que se llama return o valor retorno que quiere decir lo que devuelve la funci贸n



```python
def suma(a, b):
    return a + b

print(suma(5,3))
```

    8



```python
## Achis achis y mi suma?

print(suma(5,3))
```

    8



```python
#Vamos a ver un ejemplo matem谩tico x^2

def f(x):
    y = x**2
    return y

operacion = f(5) + 10 # Devolvemos 5**2 + 10
print(operacion) 
```

    35


#### Se puede llamar a los par谩metros de una funci贸n por posici贸n o por nombre:
#### Y  puede tener par谩metros por defecto:


```python
def algo(a,b):
    print("Resta de "+str(a)+" - "+str(b)+" = ",a-b)
    
algo(5,1)
algo(b=5,a=1)
```

    Resta de 5 - 1 =  4
    Resta de 1 - 5 =  -4



```python
## Par谩metros por defecto, en caso que no pongas nada se toma el valor indicado al definir
def cosa(a=0,b=5):
    print("Resta de "+str(a)+" - "+str(b)+" = ",a-b)
    
cosa() ## 0 - 5
cosa(b=5,a=1) ## 1 - 5
cosa(10,1) ## 10 - 1
```

    Resta de 0 - 5 =  -5
    Resta de 1 - 5 =  -4
    Resta de 10 - 1 =  9


#### Una funci贸n dentro de otra

Es posible tener un def dentro de otro pero para mandar a llamar a una funci贸n primero debes mandar a llamar a la que lo contiene. Si mandamos a llamar a la `funcion( )` esta a su vez mandar谩 a llamar a la `funcion2()`


```python
def funcion(p,q):
    r = p + q
    
    def funcion2(s):
        print(s)
        
    funcion2(5)

funcion(8,8)
```

    5



```python
#Funci贸n para saber si un n煤mero es m煤ltiplo de otro. El primer argumento
## indica la funci贸n interna y el otro argumento la funci贸n externa

def multiplo(n):
    def multiploDe(num):
        return num%n == 0
    return multiploDe
print("驴Es 9 m煤ltiplo de 3?",(multiplo(9))(3))
```

    驴Es 9 m煤ltiplo de 3? False



```python
print("驴Es 9 m煤ltiplo de 3?",(multiplo(3))(9))
```

    驴Es 9 m煤ltiplo de 3? True



```python
##Podemos mandar de lo que sea a los par谩metros, hasta listas:

def sumar(numbers):
    result = 0
    for number in numbers:
        result += number
    return result

print("Suma de 4 + 5 = ",sumar([4,5]))
```

    Suma de 4 + 5 =  9


## Ejercicio: Hacer una calculadora 馃М

Con lo aprendido hasta ahora, realizar una calculadora que haga las siguientes operaciones:

- Suma
- Resta
- Multiplicaci贸n
- Divisi贸n
- Cuadrado
- Residuo


### Recursividad: Llamada a s铆 misma de una funci贸n 馃對

![](img/remote.jpg)

Recursi贸n o recursividad es la forma en la cual se especifica un proceso basado en su propia definici贸n. 鈥? La recursi贸n tiene esta caracter铆stica discernible en t茅rminos de autorreferencialidad, autopoiesis, fractalidad, o, en otras palabras, construcci贸n a partir de un mismo tipo.

**Podemos hacer una cuenta regresiva para mandar misiles:**


```python
print("Trump: Hey siri, how many miles did i ran today?")
print("Siri: ok, sending missiles to Iran today!")

def cuenta_regresiva(numero):
    numero -= 1
    if numero > 0:
        print(numero)
        cuenta_regresiva(numero)
    else:
        print(numero)

cuenta_regresiva(5)
print("Boom!")
```

    Trump: Hey siri, how many miles did i ran today?
    Siri: ok, sending missiles to Iran today!
    4
    3
    2
    1
    0
    Boom!


Un cl谩sico ejemplo es realizar el factorial de un n煤mero


```python
def factorial(numero):
    if numero > 1:
        numero = numero * factorial(numero -1)
    print(numero)
    return numero
print("El factorial de 9 es: ",factorial(9))
```

    1
    2
    6
    24
    120
    720
    5040
    40320
    362880
    El factorial de 9 es:  362880


## Iteradores y generadores 馃崊

Los "iteradores" y "generadores" son objetos que cuentan con el m茅todo __next__(), el cual regresa una serie de objetos de uno en uno cada vez que es invocado.


```python
lista = ['1', 2, 'tres', 4.0]
print(lista)
```

    ['1', 2, 'tres', 4.0]


Creamos un iterador para ir pasando los elementos de una lista


```python
iterador = iter(lista)
print(iterador)
```

    <list_iterator object at 0x108093dd8>



```python
next(iterador)
```




    '1'




```python
next(iterador)
```




    2




```python
next(iterador)
```
    'tres'

### Yield 馃崐

B谩sicamente los generadores se escriben funciones normales, pero usan la sentencia yield en vez de un return dentro de un bucle. Yield funciona de manera similar al return, pero la gracia de usar el yield es que conserva la iteraci贸n del bucle para la siguiente vez que se le invoque.


```python
def contador(max):
    n=0
    while n < max:
            yield n
            n=n+1

miCuenta = contador(5)
print(miCuenta)
for i in miCuenta: ## Mandamos a traer lo que nos devuelve yield en cada ciclo
    print(i)
```

    <generator object contador at 0x10805bd58>
    0
    1
    2
    3
    4


El resultado es el mismo que si, en lugar de mycont = contador(5) hubi茅ramos instanciado una lista: mycont = [0,1,2,3,4] o mycont = range(0,5). Pero de hecho lo que ocurre es muy diferente.

Cuando el int茅rprete Python encuentra una funci贸n que incluye un yield (o varios), entiende que al llamar esta funci贸n no obtendremos un valor devuelto con un return, sino que obtendremos un generador (generator).

Un generador se comporta parecido a una lista, en el sentido que puede ser recorrida con un iterador - la diferencia es que los valores no est谩n almacenados en una colecci贸n, sino que se generan "on the fly".

## Decoradores 馃暞

Los decoradores son en s铆 mismos funciones, que toman como argumento una funci贸n y retornan otra funci贸n. No es m谩s que una funci贸n la cual toma como input una funci贸n y a su vez retorna otra funci贸n. Puede sonar algo confuso 驴no? lo que nos debe quedar claro es que al momento de implementar un decorador estaremos trabajando, con por lo menos, 3 funciones. El input, el output y la funci贸n principal. 


```python
def decorador(pasadaSuma):
    def function(a, b):
        print("Funci贸n sumar() llamada!")
        return pasadaSuma(a, b)
    return function

@decorador
def sumar(a, b):
    return a + b

print(sumar(7, 5)) ## Si mando a llamar a sumar, tambi茅n mandar茅 a llamar al decorador
```

    Funci贸n sumar() llamada!
    12


## Lambdas 馃崚

Se trata de crear funciones de manera r谩pida, just in time, sobre la marcha, para prototipos ligeros que requieren 煤nicamente de una peque帽a operaci贸n o comprobaci贸n.

```python
lambda argumentos: resultado
```


```python
def f(x, y, z):
    return (x+y) * z

print("(5+6) * 4 =",f(5,6,4))
```

    (5+6) * 4 = 44



```python
g = lambda x, y, z: (x+y) * z

print("(5+6) * 4 =",(g(5,6,4)))
```

    (5+6) * 4 = 44


En el ejemplo anterior, un lambda nos permite definir tanto a f y g en una sola l铆nea y ambos tienen el mismo resultado.


```python
def Multiplo(n):
    return lambda a : a * n

productoCon = Multiplo(3)

print("11 * 33 =",productoCon(11)) 

## Podemos incluso devolver una funci贸n lambda para pasarle par谩metros de otra funci贸n en este caso
```

    11 * 33 = 33


# Programaci贸n Orientada a Objectos  馃悊

La Programaci贸n Orientada a Objetos (POO u OOP seg煤n sus siglas en ingl茅s) es un paradigma de programaci贸n que usa objetos y sus interacciones para dise帽ar aplicaciones y programas de computadora. Est谩 basado en varias t茅cnicas, incluyendo herencia, modularidad, polimorfismo, y encapsulamiento. Su uso se populariz贸 a principios de la d茅cada de 1990. Actualmente son muchos los lenguajes de programaci贸n que soportan la orientaci贸n a objetos.

La programaci贸n Orientada a objetos (POO) es una forma especial de programar, m谩s cercana a como se expresan las cosas en la vida real que otros tipos de programaci贸n.

## Definiciones 猸愶笍

#### Clase
Definiciones de las propiedades y comportamiento de un tipo de objeto concreto. La instanciaci贸n es la lectura de estas definiciones y la creaci贸n de un objeto a partir de ellas.

#### Objeto
Instancia de una clase. Entidad provista de un conjunto de propiedades o atributos (datos) y de comportamiento o funcionalidad (m茅todos), los mismos que consecuentemente reaccionan a eventos. Se corresponden con los objetos reales del mundo que nos rodea, o con objetos internos del sistema (del programa). Es una instancia a una clase.

#### M茅todo
Algoritmo asociado a un objeto (o a una clase de objetos), cuya ejecuci贸n se desencadena tras la recepci贸n de un 鈥渕ensaje鈥?. Desde el punto de vista del comportamiento, es lo que el objeto puede hacer. Un m茅todo puede producir un cambio en las propiedades del objeto, o la generaci贸n de un 鈥渆vento鈥? con un nuevo mensaje para otro objeto del sistema.

#### Comportamiento
Est谩 definido por los m茅todos o mensajes a los que sabe responder dicho objeto, es decir, qu茅 operaciones se pueden realizar con 茅l.

#### Atributos
Caracter铆sticas que tiene la clase

#### Componentes de un objeto
Atributos, identidad, relaciones y m茅todos.

#### Identificaci贸n de un objeto
Un objeto se representa por medio de una tabla o entidad que est茅 compuesta por sus atributos y funciones correspondientes.


```python
class Coche:
    
    def __init__(self, rueditas,puertitas):
        self.ruedas = rueditas
        self.puertas = puertitas
    def desplazarse(self):
        print("El coche se esta desplazando sobre ruedas")

unCoche = Coche(4,5)
print("Mi coche tiene ", unCoche.ruedas ,"ruedas")
```

    Mi coche tiene  4 ruedas


## Pilares de la programaci贸n orientada a objetos 馃

### Abstracci贸n 馃尮
permite identificar las caracter铆sticas y comportamientos de un objeto y con los cuales se construir谩 la clase (plantilla).  Esto quiere decir que a trav茅s de este pilar o fundamento es posible reconocer los atributos y m茅todos de un objeto.

### Encapsulamiento 馃崉
Es la caracter铆stica de la POO que permite el ocultamiento de la complejidad del c贸digo, pertenece a la parte privada de la clase y que no puede ser vista desde ning煤n otro programa.

### Herencia 馃拹
Es el pilar m谩s fuerte que asegura la reutilizaci贸n de c贸digo, ya que a partir de esta caracter铆stica es posible reutilizar (heredar) las caracter铆sticas y comportamientos de una clase superior llamada clase padre, a sus clases hijas, denominadas clases derivadas. Esto implica que una vez desarrollado el c贸digo de una clase base, su c贸digo puede ser reutilizado por las clases derivadas.

### Polimorfismo 馃崁
A trav茅s de esta caracter铆stica es posible definir varios m茅todos o comportamientos de un objeto bajo un mismo nombre, de forma tal que es posible modificar los par谩metros del m茅todo, o reescribir su funcionamiento, o incrementar m谩s funcionalidades a un m茅todo.


```python
class Persona:
    cedula = "V-13458796"
    nombre = "Leonardo"
    apellido = "Caballero"
    sexo = "M"
    
    def saludar(self):
        print("Hola soy ",self.nombre,", mi c茅dula es: ",self.cedula," y mi sexo es: ",self.sexo)

#Crear una persona
PersonaCreada = Persona()

#Llamar a un m茅todo
PersonaCreada.saludar()

## Lllamar a un atributo
print("Mi Sexo es:",PersonaCreada.sexo)
```

    Hola soy  Leonardo , mi c茅dula es:  V-13458796  y mi sexo es:  M
    Mi Sexo es: M


## Atributos y m茅todos 馃悩

### Atributos: caracter铆sticas con las que cuenta un objeto -> Adjetivos calificativos
### M茅todos: cosas que puede hacer el objecto -> verbos

### Atributos de instancia
Atributos de Instancia

Los atributos de instancia son aplicables a un solo objeto. Determinan el estado en el que se encuentra un objeto.

**Ejemplo:**
El atributo altura en la clase Persona es de instancia, debido a que cada persona tendr谩 su propia altura.

### Atributos de clase

  Un atributo de clase es un atributo com煤n a todos los objetos instanciados de la clase. Al estar definido en la clase no hace falta instanciar la clase para utilizarlo. Las constantes se suelen definir como atributos de clase.

**Ejemplo:**
El atributo cantidadDeOjos en la clase Persona es de clase, debido a que todas las instancias de la clase persona tendr谩n igual cantidad de ojos.


```python
class Empleado:
    cedula = "V-13458796" ## Atributo de clase
    def inicializar(self,nombreInsertado):
        self.nombre = nombreInsertado ## Atributo de instancia

juanito = Empleado()
juanito.inicializar("Juan")

## La c茅dula es incorrecta ya que no ser谩 la misma en todos los empleados
print("La c茅dula de todos es:",juanito.cedula) 


## Nombre es correcto ya que existe y es diferente para cada objeto
print("El nombre del empleado es:",juanito.nombre)
```

    La c茅dula de todos es: V-13458796
    El nombre del empleado es: Juan


### M茅todos de clase -> Puede o no existir el objeto 馃惓
Un m茅todo de clase puede modificar el estado de una clase, accediendo a los atributos de dicha clase, a煤n cuando el m茅todo es invocado desde una clase. En lugar de definirse utilizando self como primer par谩metro, se utiliza cls.

### M茅todos de instancia -> Tiene a fuerzas que existir el objeto 馃尡
Son los que hemos visto def(self):

### M茅todos est谩ticos -> Puede o no existir el objeto pero no puede acceder a los atributos del mismo 馃悪
Los m茅todos est谩ticos est谩n restringidos en su 谩mbito, de tal manera que no tienen acceso a los atributos del objeto. Se definen de forma id茅ntica a una funci贸n, sin necesidad de ingresar el par谩metro inicial self.



```python
class PoblacionCensada:
    poblacion = 0
    nombre = ""
    poblacion = 0
    @classmethod
    def opera_poblacion(cls, operador, cantidad):
        cls.poblacion = eval(str(cls.poblacion) + operador + str(cantidad))
    
    @classmethod
    def despliega_total(cls):
        return cls.poblacion
    
    def __init__(self, nombre, numero=0):
        print("Se ha creado la poblaci贸n",nombre," con ",numero," habitantes")
        self.nombre = nombre
        self.poblacion = numero
        self.opera_poblacion('+', self.poblacion)   
    
    
    def imprimirHola(self):
        print("Hola mi nombre es: ",self.nombre," y mi n煤mero de habitantes es: ",self.poblacion)
```


```python
print("M茅todo de clase: ",PoblacionCensada.despliega_total())
```

    M茅todo de clase:  0



```python
print("M茅todo de clase: ",PoblacionCensada.imprimirHola()) ## No se puede ya que imprimirHola
#No tiene ning煤n decorador para indicar que es de clase
```


```python
Chalco = PoblacionCensada("Valle de Chalco",1000000)
Chalco.imprimirHola()
```

    Se ha creado la poblaci贸n Valle de Chalco  con  1000000  habitantes
    Hola mi nombre es:  Valle de Chalco  y mi n煤mero de habitantes es:  1000000



```python
## Probamos un m茅todo est谩tico para traer una direcci贸n ip
class Servidor:
    usuarios_activos = set(())
    
    def __init__(self, dominio, lista):
        self.lista_usuarios = lista
        self.dominio = dominio
    
    def conexion(self, usuario):
        if usuario in self.lista_usuarios:
            self.usuarios_activos.add(usuario)
        else:
            return False
        
    @staticmethod
    def ping(ip):
        return ip
    
    @staticmethod
    def ImprimirHola():
        print("Hola")
```


```python
Servidor.ping("192.168.17.8")
```




    '192.168.17.8'



### M茅todo init 馃惗

El m茅todo __init__ es el primer m茅todo que se ejecuta cuando se crea un objeto.
El m茅todo __init__ se llama autom谩ticamente. Es decir es imposible de olvidarse de llamarlo ya que se llamar谩 autom谩ticamente.


```python
class Empleado:

    def __init__(self):
        self.nombre=input("Ingrese el nombre del empleado:")
        self.sueldo=float(input("Ingrese el sueldo:"))

    def imprimir(self):
        print("Nombre:",self.nombre)
        print("Sueldo:",self.sueldo)

    def paga_impuestos(self):
        if self.sueldo>3000:
            print("Debe pagar impuestos")
        else:
            print("No paga impuestos")
```


```python
sam = Empleado()
```

    Ingrese el nombre del empleado:Sam
    Ingrese el sueldo:10



```python
print("Primer d铆a de explotaci贸n de Samuel")
sam.imprimir()
```

    Primer d铆a de explotaci贸n de Samuel
    Nombre: Sam
    Sueldo: 10.0



```python
print("驴Samuel debe pagar impuestos?")
sam.paga_impuestos()
```

    驴Samuel debe pagar impuestos?
    No paga impuestos


### Otro ejemplo: puntos en un plano XY


```python
# otro ejemplo

class Punto:

    def __init__(self,x,y):
        self.x=x
        self.y=y

    def imprimir(self):
        print("Coordenada del punto")
        print("(",self.x,",",self.y,")")

    def imprimir_cuadrante(self):
        if self.x>0 and self.y>0:
            print("Primer cuadrange")
        else:
            if self.x<0 and self.y>0:
                print("Segundo cuadrante")
            else:
                if self.x<0 and self.y<0:
                    print("Tercer cuadrante")
                else:
                    if self.x>0 and self.y<0:
                        print("Cuarto cuadrante")

punto1=Punto(3,4)
punto2 = Punto(-5,6)
punto3 = Punto(7,-9)
punto4 = Punto(-6,-6)
##Puede iniciarlizarse en el objeto

punto1.imprimir_cuadrante()
punto2.imprimir_cuadrante()
punto3.imprimir_cuadrante()
punto4.imprimir_cuadrante()
```

    Primer cuadrange
    Segundo cuadrante
    Cuarto cuadrante
    Tercer cuadrante


## Abstracci贸n : Ejercicio -> Abstraigan a un animal y luego a un perro


```python
### Encapsulamiento:

class Ejemplo():
    __luces = 100
    def publico(self):
        return "Soy un m茅todo p煤blico, a la vista de todo"
    def __privado(self):
        return 418046193
    def regresarCuenta(self):
        return "6363434582"+str(self.__privado())+"6277841"
```


```python
miEjemplito = Ejemplo()
print(miEjemplito.publico())
```

    Soy un m茅todo p煤blico, a la vista de todo



```python
# Cuando intente ejecutar un atributo privado, marca error
miEjemplito.privado()
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    <ipython-input-88-5acc7d98f3c9> in <module>()
          1 # Cuando intente ejecutar un atributo privado, marca error
    ----> 2 miEjemplito.privado()
    

    AttributeError: 'Ejemplo' object has no attribute 'privado'



```python
print("N煤mero de cuenta oculto:",miEjemplito.regresarCuenta())
```

    N煤mero de cuenta oculto: 63634345824180461936277841


#### Otro ejemplo de Encapsulamiento: Caja Registradora 馃捇


```python
class CajaDeSeguridad:
    __contraclave = "123qwe"
    
    def seguro(self, clave):
        if self.__contraclave == clave:
            print("Acceso concedido.")
        else:
            print("Acceso denegado.")
```


```python
unaCaja = CajaDeSeguridad()
unaCaja.seguro("123456")
```

    Acceso denegado.



```python
unaCaja.seguro("123qwe")
```

    Acceso concedido.



```python
class SerVivo():
    def __init__(self, tipo, reino):
        self.tipo = tipo
        self.reino = reino
```


```python
class Persona:
    def __init__(self, cedula, nombre, apellido, sexo):
        self.cedula = cedula
        self.nombre = nombre
        self.apellido = apellido
        self.sexo = sexo

    def hablar(self, mensaje):
        return mensaje

    def getGenero(self, sexo):
        genero = ('Masculino','Femenino')
        if sexo == "M":
            return genero[0]
        elif sexo == "F":
            return genero[1]
        else:
            return "Desconocido"
```

## Herencia 鉂勶笍

La herencia hace que se puedan declarar nuevas clases basadas en otras para poder reutilizar el c贸digo, generando as铆 una jerarqu铆a de clases dentro de una aplicaci贸n. Si una clase deriva de otra, esta hereda sus atributos y m茅todos y puede a帽adir nuevos atributos, m茅todos o redefinir los heredados.

#### Terminolog铆a:

- **Superclase:** La clase cuyas caracter铆sticas se heredan se conoce como superclase (o una clase base o una clase principal).

- **Subclase:** La clase que hereda la otra clase se conoce como subclase (o una clase derivada, clase extendida o clase hija). La subclase puede agregar sus propios campos y m茅todos, adem谩s de los campos y m茅todos de la superclase.

- **Reutilizaci贸n:** La herencia respalda el concepto de 鈥渞eutilizaci贸n鈥?, es decir, cuando queremos crear una clase nueva y ya hay una clase que incluye parte del c贸digo que queremos, podemos derivar nuestra nueva clase de la clase existente. Al hacer esto, estamos reutilizando los campos/atributos y m茅todos de la clase existente.



```python
class Supervisor(Persona):

    def __init__(self, cedula, nombre, apellido, sexo, rol):
        Persona.__init__(self, cedula, nombre, apellido, sexo)
        self.rol = rol
        self.tareas = ['10','11','12','13']

    def consulta_tareas(self):
        return self.tareas
```


```python
Fulano = Supervisor(123,"Erick","Aguilar","M","supervisor de caja 1")
print(Fulano.consulta_tareas())
```

    ['10', '11', '12', '13']


Los casos de herencia m煤ltiple en python se dan cuando una clase secundaria o hija hereda atributos y metodos de mas de una clase principal o padre. Basta con separar con una coma ambas principales a la hora de crear la clase secundaria:


```python
class Chalan(Persona,SerVivo):
    def __init__(self, cedula, nombre, apellido, sexo, rol,tipo,reino):
        Persona.__init__(self, cedula, nombre, apellido, sexo)
        SerVivo.__init__(self,tipo,reino)
        self.rol = rol
        self.tareas = ['Cargar bultos','Tirar losa',"Alinear"]
        
    def consulta_tareas(self):
        return self.tareas
```


```python
ElCarlangas = Chalan(1234,"Carlos","De Dios","M","Chalanazo","Humano","Animal")
```


```python
ElCarlangas.tipo
```




    'Humano'




```python
ElCarlangas.consulta_tareas()
```




    ['Cargar bultos', 'Tirar losa', 'Alinear']




```python
ElCarlangas.getGenero('M') ## C贸mo arreglar铆an este error??
```




    'Masculino'



## Polimorfismo 鈽勶笍

El polimorfismo es una relajaci贸n del sistema de tipos, de tal manera que una referencia a una clase (atributo, par谩metro o declaraci贸n local o elemento de un vector) acepta direcciones de objetos de dicha clase y de sus clases derivadas (hijas, nietas, 鈥?).


M煤ltiples formas. Un le贸n es a la vez un animal.

Tal como funcionan los lenguajes fuertemente tipados, una variable siempre deber谩 apuntar a un objeto de la clase que se indic贸 en el momento de su declaraci贸n



```python
class Persona():
    def __init__(self):
        self.cedula = 13765890
    def mensaje(self):
        print("mensaje desde la clase Persona")

class Obrero(Persona):
    def __init__(self):
        self.__especialista = 1
    def mensaje(self):
        print("mensaje desde la clase Obrero")

class Ingeniero(Persona):
    def __init__(self):
        self.__especialista = 2
    def mensaje(self):
        print("Mensaje desde la clase Ingeniero")

class Arquitecto(Persona):
    def __init__(self):
        self.__especialista = 3
    def mensaje(self):
        print("Mensaje desde la clase Arquitecto馃拝")

obrero_planta = Obrero()
ingeniero_fresa = Ingeniero()
arquitecto_pirruris = Arquitecto()

obrero_planta.mensaje()
ingeniero_fresa.mensaje()
arquitecto_pirruris.mensaje()

print("\n")

super(Arquitecto, arquitecto_pirruris).mensaje()
super(Ingeniero, ingeniero_fresa).mensaje()
super(Obrero, obrero_planta).mensaje()


```

    mensaje desde la clase Obrero
    Mensaje desde la clase Ingeniero
    Mensaje desde la clase Arquitecto馃拝
    
    
    mensaje desde la clase Persona
    mensaje desde la clase Persona
    mensaje desde la clase Persona



```python
class Perros(object): #Declaramos la clase principal Perros, todas heredan de la clase object
    def ladrar (self):
        print ("""GUAAAUU GUAAAUU!""")
    def grunir (self):
        print ("""GRRRRRR GRRRRR""")

class Caniche (Perros):#La clase secundaria hereda de la clase principal perros
    def ladrar(self):
        print ("""guau guau guau""")
        
    def grunir(self):
        print ("""g帽帽帽帽iii g帽帽帽iiii""")

class Pastor_Aleman(Perros):#La clase secundaria hereda de la clase principal perros
    def ladrar(self):
        print ("""GuaUUU GUAAAUUU GuaUUU""")
        
    def grunir(self):
        print ("Agrfgregreff aggrrfsgrrr")
 
    
class Shepadoodle (Caniche,Pastor_Aleman):#La clase hereda de las clases hijas de su padre Perros
    def ladrarx(self, veces):
        for cuantas in range(veces):
            super(Shepadoodle, self).ladrar()

Tommy = Pastor_Aleman()
Piny = Caniche()
Cuchele = Shepadoodle()
Cuchele.ladrarx(5)
```

    guau guau guau
    guau guau guau
    guau guau guau
    guau guau guau
    guau guau guau


### Ejercicio si no tienen nada qu茅 hacer en casa, el primero que lo env铆e ya tiene su constacia:

Si enlistamos los n煤meros primos: 2, 3, 5, 7, 11, y 13, vemos que el 13 es el 6to primo.

驴Cu谩l es el primo de la posici贸n 10 001?

### Soluci贸n al reto de primos 馃:



```python
limite = 100001
i = 3
cuenta = 1
primo = 2
while cuenta < limite:
    for x in range(3, int(i ** 0.5) + 1, 2):
        if i % x == 0:
            break
    else:
        primo = i
        cuenta += 1
    i += 2
print(primo)
```

    1299721


# Archivos 馃梼

Python incorpora un tipo integrado llamado file, el cual es manipulado mediante un objeto archivo el cual fue generado a trav茅s de una funci贸n integrada.

La biblioteca OS nos permite manipular archivos del sistema operativo. Como eliminarlos, moverlos y otras cosas que podr铆amos hacer desde shell.


```python
#Listar el contenidos de una carpeta
import os
print("Contenido de la carpeta:",os.listdir("./"))

#Mostrar el actual directorio de trabajo
print("Directorio actual:",os.getcwd())

#Mostrar el tama帽o del archivo en bytes del archivo pasado en par谩metro

print("Este documento pesa en bytes:",os.path.getsize("El lenguaje de programaci贸n Python - B谩sico.ipynb"))

#Para renombrar un archivo
# os.rename("Ana_Poleo","Ana_Carolina")

```

    Contenido de la carpeta: ['.DS_Store', 'El lenguaje de programaci贸n Python - B谩sico.ipynb', 'img', '.gitignore', '.ipynb_checkpoints']
    Directorio actual: /Users/samuelarturogarridosanchez/Desktop/Proteco/Python2020-2/Teor铆a/B谩sico
    Este documento pesa en bytes: 123819


### Manipulaci贸n de archivos y su contenido


```python
import os

print("Creaci贸n de un archivo")

nombre = 'ejemplo.txt'

archivo = open(nombre, 'w') # abre el archivo datos.txt en formato w de escritura
archivo.write('Prueba para ver si se escribe en el archivo.\nY otra l铆nea\nY otra') ## String que se escribe
archivo.close() ## Cerramos el puntero

## Determinar si el archivo fue creado o no
if nombre in os.listdir("."):
    print("\nArchivo creado en la ruta:"+os.getcwd()+"/"+nombre)
else:
    print("No se encontr贸 al archivo")

print("\nLectura de archivo")

archivo = open(nombre, 'r') ## Se apertura el archivo en formato de lectura
contenido = archivo.read() ## Leemos
print(contenido) # Imprimimos el contenido
archivo.close() ## Cerramos el puntero


print("\nImprimir l铆nea por l铆nea")

archivo = open(nombre, 'r') ## Se apertura el archivo en formato de lectura
for linea in archivo: ## Tiene un iterador interno para recorrer l铆nea por l铆nea
    print("L铆nea: ",linea)
print("\n")
archivo.close() # Cerramos el puntero


print("Eliminar un archivo")

#os.remove(os.getcwd()+"/"+NOMBRE_ARCHIVO)
```

    Creaci贸n de un archivo
    
    Archivo creado en la ruta:/Users/samuelarturogarridosanchez/Desktop/Proteco/Python2020-2/Teor铆a/B谩sico/ejemplo.txt
    
    Lectura de archivo
    Prueba para ver si se escribe en el archivo.
    Y otra l铆nea
    Y otra
    
    Imprimir l铆nea por l铆nea
    L铆nea:  Prueba para ver si se escribe en el archivo.
    
    L铆nea:  Y otra l铆nea
    
    L铆nea:  Y otra
    
    
    Eliminar un archivo


# FIN 馃弫
