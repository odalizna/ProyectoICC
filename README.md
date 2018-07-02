#para agregar al comienzo
from datetime import datetime, date, time, timedelta

ahora = datetime.now()

print ("************************")
print ("¡Bienvenido a DeliRico!")
print("Fecha y Hora:", ahora)
print ()
nombre =  input('Dinos cómo te llamas: ')

print ('Hola', nombre, ', selecciona qué tipo de comida quieres llevar.')
print ()
print ('¿Prefieres comida rápida y al instante? ¡Snack! o ¿comidas para tu día? ¡Almuerzos!')
print ('        Opción 1: Snack')
print ('        Opción 2: Almuerzos')
firstoption= int (input('Inserta la opción que prefieras: '))
print ()



# ProyectoICC
lista=[1,2,3,4,5,6]
n=0
if 1 in lista:
    n=lista.index(3)
    print('3 está en la lista y su posición es {}'.format(n))
else:
    n=-1
    print("NO existe")

#suma del 1 al n
def suma_consecutiva(x):
    cont=0
    suma=0
    for y in range(1,x+1):
        cont=cont+1
        suma=suma+cont
    return(suma)
n=int(input("Ingrese su número: "))
a=suma_consecutiva(n)
print(a)

#hipotenusa
def hipo (a,b):
    h=(a**2+b**2)**0.5
    return int((h))
c1=int(input("Ingrese cateto 1: "))
c2=int(input("Ingrese cateto 2: "))
s=hipo(c1,c2)
print(s)

#area círculo
import math
def CalcularAreaCirculo(r):
    area=(r**2)*math.pi
    return(area)
n=int(input("Ingrese el radio: "))
a=CalcularAreaCirculo(n)
print(a)

def f(x):
    return((g(x))*3+5)
def g(x):
    return(x**2)
n=int(input())
a=f(n)
print(a)

#farenheit a celsius
def convertir (a,b):
    if a==1:
        if 0<b<100:
            c=b+273
            return(c)
        else:
            return("Error")
    elif a==2:
        if 0<b<373:
            c=b-273
            return(c)
        else:
            return("Error")

opcion=int(input("celsius-f: 1, f-celsius: 2"))
n=int(input("Ingrese su número: "))
s = convertir(opcion,n)
print(s)

#palíndroma
def invertir(cadena):
    invertido = ""
    tamano = len(cadena)
    a = 0
    while a < tamano:
        invertido = cadena[a] + invertido
        a += 1
        return(invertido)
def espalindromo(cadena):
    if cadena == invertir(cadena):
        return(True)
    else:
        return (False)
print(espalindromo("qwertytrewq"))

#factorial
def factorial(x):
    cont=0
    por=1
    while cont<x:
        cont=cont+1
        por=por*cont
    return(por)
n=int(input("Ingrese el número: "))
s=factorial(n)
print(s)

#líneadecodigo combinatoria
def combinatoria(x,y):
    diferencia=0
    diferencia=x-y
    if diferencia>0:
        valor=factorial(x)/(factorial(y)*factorial(diferencia))
        return(valor)
    else:
        return("El segundo valor ingresado es errado")
def factorial (a):
    cont=0
    por=1
    while cont<a:
        cont=cont+1
        por=por*cont
    return(por)
entrada1=int(input("ingresa: "))
entrada2=int(input("Ingresa: "))
valortotal=combinatoria(entrada1,entrada2)
print(valortotal)


#Evaluadora la parte 1:
def evaluadora(s):
    l = []
    l = [str(x) for x in s]
    balance = 0
    while len(l) > 0:
        token = l.pop(0)
        if token == '(':
            balance = balance+1
        elif token == ')':
            balance = balance-1
    if balance != 0:
        return False
    else:
        return True

#evaluadora la parte 2:
def equilibrio(a):
    lista=[]
    lista=[str(x) for x in a]
    cont=0
    cont1=0
    for y in lista:
        if "("==y:
            cont=cont+1
        if ")"==y:
            cont1=cont1+1
    diferencia=cont-cont1
    if diferencia==0:
        return("True")
    else:
        if diferencia<0:
            return('Falta {} "("'.format(abs(diferencia)))
        else:
            return('Falta {} ")"'.format(diferencia))
list=str(input())
a=equilibrio(list)
print(a)


#lo que necesito saber para diccionarios

dic={"a":1,"b":2,"c":3}
dic['d']=4
dic['b']=6
del dic['b']
dic.update({'e':7})
if "c" in dic.keys():
    print("true")
else:
    print("no")

if 1 in dic.values():
    print("True")
else:
    print("False")
print(dic)
for k in dic.keys():
    print('Para cada {}, existe un {}'. format(k,dic[k]))
for k,v in dic.items():
    print('Para cada {}, existe un {}'.format(k,v))
# impirmir a tabla
for k, n in dic.items():
    print('{:>10} {:>10}'.format(k,n))
print("")
for valor in dic.items():
    print(valor, end=" ")

# impirmir a tabla
for k, n in dic.items():
    print('{:>10} {:>10}'.format(k,n))

#diccionario
traductor={
            1:"huk",
            2:"iskay",
            3:"kimsa",
            4:"tawa",
            5:"pichqa",
            6:"soqta",
            7:"qanchis",
            8:"pusaq",
            9:"isqon",
            10:"chunqa"}
n=int(input())
if 0<n<11:
    palabra=traductor[n]
    print(palabra)
else:
    print("Valor no encontrado")

#se repiten las personas

nombrerepet={}
s=0
while s!="#":
    s =input("Ingrese el nombre: ")
    if s!="#":
        if s not in nombrerepet.keys():
            nombrerepet[s]=1
        else:
            nombrerepet[s]=nombrerepet[s]+1
print(nombrerepet)

#otro diccionaripo
nombredic={}
x=0
while x ==0:
    nombre =str(input("Ingrese el nombre: "))
    if nombre not in nombredic.keys():
        edad=int(input("Ingrese la edad: "))
        nombredic[nombre]=edad
    else:
        print("El nombre no es válido")
        x=1
else:
    a=0
    a=sum(nombredic.values())/len(nombredic.values())
    print(a, min(nombredic.values()), max(nombredic.values()))

n = int(input())
colores = {}
cont = 1
while cont <= n:
    color = str(input())
    colores[cont]=color
    cont = cont + 1
colorespecial = str(input())
cont = 1
salida = ""
for x in colores.values():
    if x == colorespecial:
        salida = salida+str(cont)+" "
    cont = cont+1
print(salida)

def factorial(n):
    if n == 0:
        return 1
    else:
        fact = n * factorial(n-1)
        return fact
def combinatoria(n, k):
    comb = (factorial(n))/(factorial(k)*factorial(n-k))
    return comb
a = int(input())
a1 = int(input())
b = combinatoria(a, a1)
print(b)


dicnombres = {}
pos = ""
while pos != #:
    pos = input()
    if pos != #:
        if pos not in dicnombres:
            dicnombres[pos]= 1
        else:
            dicnombres = dicnombres[pos]+1
           
for k, v in dicnombres.items():
    print(k, v)

dicalumnos = {}
n = int(input("N de alumnos: "))
for x in range(1, n+1, 1):
    notas = []
    contNot = 1
    y = input()
    while contNot <= 4:
        nota = int(input())
        notas.append(nota)
        contNot = contNot+1
    dicalumnos.update({y:notas})
for k, v in dicalumnos.items():
    print(k, (sum(v))/4)
#
