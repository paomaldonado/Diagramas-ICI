# Segundos problemas Parcial 2.
## 7 Calcular el promedio de calificaciones aprobatorias y reprobadas. 
### 7.1 Análisis
El algoritmo debe leer las calificaciones aprobadas (Menor a 6) y reprobadas (Mayor a 6)
### 7.2 Entrada 
Calificaciones, máximo 15
### 7.3 Salida
Promedio de calificaciones reprobadas y aprobadas
### 7.4 DFD
Do While:
![7MO PROBLEMA DOWHILE](https://user-images.githubusercontent.com/113482337/198404541-84dff5e4-e99a-4007-bb2d-9008c1516159.jpg)
While:
![7MO PROBLEMA WHILE](https://user-images.githubusercontent.com/113482337/198404612-cf0ac7e8-c28b-4a62-bf91-43d9454d4a9c.jpg)
For:
![7MO PROBLEMA FOR](https://user-images.githubusercontent.com/113482337/198404626-b2cf9051-09db-49d5-b59d-1103f8359db5.jpg)
### 7.5 Prueba de escritorio 
|Entrada | Salida |
| ----------- | ----------- |
| 7, 8, 5, 6, 4, 8, 9, 5 | Promedio aprobados 7.6 Promedio reprobados 4.6 |
### 7.6 Código
_Ciclo For:_
alumnos = list(range(15))
p_aprobados = 0
j = 0

for i in alumnos: 
    while(True):
        calificacion = int(input("Ingresa la calificación >>"))
        if (calificacion >= 0 and calificacion <= 10):
            break
        else:
            print("Calificación fuera de rango. Intenta de nuevo")
 
    if (calificacion < 6):
     alumnos[i] = "R"
    else:
     p_aprobados = calificacion + p_aprobados
     j = j + 1
     alumnos[i] = "A"

print("\033[33;1m",alumnos,"\033[39m")
print("El promedio de calificación de los aprobados es de >>",round(p_aprobados/j,2))
print("El total de aprobados fueron >> ",j)
print("El total de reprobados fueron >> ",(len(alumnos)-j))

_Ciclo while:_
alumnos = list(range(15))
p_aprobados = 0
j = 0

for i in alumnos: 
    while(True):
        calificacion = int(input("Ingresa la calificación >>"))
        if (calificacion >= 0 and calificacion <= 10):
            break
        else:
            print("Calificación fuera de rango. Intenta de nuevo")
 
    if (calificacion < 6):
     alumnos[i] = "R"
    else:
     p_aprobados = calificacion + p_aprobados
     j = j + 1
     alumnos[i] = "A"

print("\033[33;1m",alumnos,"\033[39m")
print("El promedio de calificación de los aprobados es de >>",round(p_aprobados/j,2))
print("El total de aprobados fueron >> ",j)
print("El total de reprobados fueron >> ",(len(alumnos)-j))

_Ciclo do while:_ 
void main() {
  double PromA = 0;
  var contr = 0;
  double sumaA = 0;
  double contA = 0;
  double cal1 = 0;
  double cal2 = 1;
  var cont = 0;
  stdout.write("Dame las calificaciones\n ");
  stdout.write("----------\n");
  do {
    double c = double.parse(stdin.readLineSync()!);
    cont = cont +1;
    if (c > 10) {
      print('La calificacion no puede ser mayor a 10');
      cont = cont - 1;
    }
    if (c < 0) {
      print('La calificacion no puede ser menor a 0');
      cont = cont - 1;
    }
    if (c < 6 && c > 0) {
      contr = contr + 1;
    }
    if (c <= 10 && c >= 6) {
      cal1 = c;
      sumaA = sumaA + cal1;
      contA++;
    }
    if (cal1 > cal2) {
      cal2 = cal1;
    }
  } while (cont <= 14);
  PromA = sumaA / contA;
  print('El promedio de aprobados es $PromA');
  print('La calificacion mas alta es $cal2');
  print('La cantidad de reprobados son $contr');
}
## 8 Capture n números en el rango [Li,Ls] donde: -Li = Limite inferior -Ls limite superior para li<ls y l0, obtenga: Cantidad de números pares y su promedio, Cantidad de números impares y su promedio y ¿Qué promedio es mayor?
### 8.1 Análisis
El algoritmo debe leer amnos limites, posteriormente leer una serie de números, validando que estén dentro de los límites y obtener lo requerido.
### 8.2 Entrada 
Límites inferior, superior y serie de números. 
### 8.3 Salida 
Pares y su promedio.
Impares y su promedio.
Promedio mayor
### 8.4 Prueba de escritorio
|Entrada | Salida |
| ----------- | ----------- |
| 7, 8, 5, 6, 4, 8, 9, 5 | Promedio aprobados 7.6 Cantidad 5 Promedio reprobados 4.6 Cantidad 3 El promedio mayor es el de aprobados |
### 8.5 DFD
Do While:
![E8_dowhile](https://user-images.githubusercontent.com/113482337/198408915-0f901423-f901-4647-8bea-8e0e780c1222.png)
While:
![E8_while](https://user-images.githubusercontent.com/113482337/198408938-5fc16787-b950-4a43-82a4-be4d73e50975.png)
For: 
![E8_for](https://user-images.githubusercontent.com/113482337/198408972-952eb438-e835-4921-ae90-475c4692ddc6.png)

###### 8.5 Código
_Ciclo for:_
sp=0
cp=0
pp=0
si=0
ci=0
pi=0
li=-1
ls=-1
n=-1
num=-1

while(li<0):
    li = int(input("Limite inferior: "))
    
    if(li<0):
        print("Tiene que ser mayor a 0")
        
while(ls<li):
    ls = int(input("Limite superior: "))
    
    if(ls<li):
        print("Tiene que ser mayor que el limite inferior")
        
while(n<0):
    n = int(input("¿Cuantos numeros? "))
    
    if(n<0):
        print("Tiene que ser mayor a 0")
    
for i in range(n): 
    while(num<=li or num>=ls):
        num = int(input("Dame un numero de LI y LS: "))
        
        if(num<=li or num>=ls):
            print("Tiene que estar dentro del LI al LS")

    if(num%2==0):
        sp=sp+num
        cp=cp+1
    else:
        si=si+num
        ci=ci+1
        
    num=-1       
         
if(sp==0 or cp==0):
    pp=0
else:
    pp=sp/cp
    
if(si==0 or ci==0):
    pi=0
else:
    pi=si/ci
    
if(pp>pi):
    print("El PP es mayor que el PI")
else:
    print("El PI es mayor que el PP")
    
_Ciclo while:_
print("Dame Límite inferior: ")
Li = int(input())
while Li<0:
    print("El límite inferior debe ser mayor a 0")
    print("Dame Límite inferior: ")
    Li = int(input())

print("Dame límite superior: ")
Ls = int(input())
while Ls<=Li:
    print("El límite superior no puede ser menor o igual al limite inferior")
    print("Dame límite superior: ")
    Ls = int(input())

pares = 0
impares = 0

lista=[]
for x in range(10):
    valor=int(input("Ingrese un valor entero: "))
    lista.append(valor)
print(lista)

for a in lista:
    if a % 2 == 0:
        pares = pares + a
    else:
        impares = impares + a
print("La suma de los números pares es: ",pares)
print("La suma de los números impares es: ",impares)

prom_pares = pares / a
prom_impares = impares / a

print("El promedio de los números pares es: ",prom_pares)
print("El promedio de los números impares es: ",prom_impares)

if prom_pares > prom_impares:
    print("El promedio de los pares es mayor que el promedio de los impares.")
else:
    print("El promedio de los números impares es mayor que el promedio de los pares.")

_Ciclo do while:_
void main() {
  double sumap = 0;
  double sumai = 0;
  var contp = 0;
  var conti = 0;
  double promp = 0;
  double promi = 0;
  print('Introduce el limite inferior, mayor a 0');
  var li = int.parse(stdin.readLineSync()!);
  if (li < 0) {
    print('tu limite inferior debe ser mayor a 0');
  }
  if (li > 0) {
    print('Ahora introduce un limite superior');
    var ls = int.parse(stdin.readLineSync()!);
    if (ls < li) {
      print('tu limite superior debe ser mayor a tu limite inferior');
    }
    var cont = li;
    do {
      if (cont <= ls) {
        sumai = sumai + cont;
        conti = conti + 1;
      }
      if (cont % 2 == 0) {
        sumap = sumap + cont;
        contp = contp + 1;
        sumai = sumai - cont;
        conti = conti - 1;
      }
      cont = cont + 1;
    } while (cont <= ls);

    promi = sumai / conti;
    print('los impares son $conti y su promedio es $promi');
    promp = sumap / contp;
    print('los pares son $contp y su promedio es $promp');
    if (promp < promi) {
      print('$promi es mayor');
    }
    if (promp > promi) {
      print('el promedio $promp es mayor');
    }
  }
}

## 9. Obtener la frecuencia de n calificaciones entre [1,10]. Indique la cantidad de aprobados, la cantidad de reprobados, el promedio de aprobados y promedio general.
### 9.1 Análisis
El algoritmo debe contener un array entre 1 y 10, leer las calificaciones ingresadas  y comprobar si son calificaciones aprobatorias o reprobatorias.
### 9.2 Entrada
Calificaciones
### 9.3 Salida
Cuáles son las calificaciones aprobatorias y cuáles las reprobatorias. 
### 9.4 DFD
While:
![E9_while](https://user-images.githubusercontent.com/113482337/198413262-0a16912d-ceb5-47d1-9d6d-1bbfc270f540.png)
Do while:
![E9_dowhile](https://user-images.githubusercontent.com/113482337/198413274-ec42230e-d2fe-49d0-9186-bbaaf01f93f8.png)
For:
![E9_for](https://user-images.githubusercontent.com/113482337/198413302-f629ca11-06de-45bc-921c-828cf2a7337c.png)
### 9.5 Código
_Do while:_
Calificaciones=int(input("Ingrese la cantidad de calificaciones"))
vec=[]
n=0

cont = 0
while(True):
    calificacion=int(input("Calificacion: "))
    n=n+calificacion
    vec.append(calificacion)
    cont += 1
    if(cont>=Calificaciones):
        break;
        
aprobado=0

promedioAprobados = 0
for h in vec:
    if h>=5:
        aprobado=aprobado+1
        promedioAprobados = promedioAprobados + h

promedioAprobados = promedioAprobados / aprobado

reprobado=0
for k in vec:
    if k<=5:
        reprobado=reprobado+1

print("Cantidad de aprobados:", aprobado)
print("Cantidad de reprobados:", reprobado)
print("Promedio de aprobados:", promedioAprobados)

_While:_
Calificaciones=int(input("Ingrese la cantidad de calificaciones"))
vec=[]
n=0
cont = 0
while(cont < Calificaciones):
    calificacion=int(input("Calificacion: "))
    n=n+calificacion
    vec.append(calificacion)
    cont += 1

promedio=n/len(vec)

npromedio=0
for j in vec:
    if j>promedio:
        npromedio=npromedio+1

aprobado=0

#Primero inicializas el contador
promedioAprobados = 0
for h in vec:
    if h>5:
        aprobado=aprobado+1
        #Va sumando cada unas de las notas
        promedioAprobados = promedioAprobados + h

#Luego saca el promedio sumatoria / cantidad de aprobados 
promedioAprobados = promedioAprobados / aprobado

reprobado=0
for k in vec:
    if k<5:
        reprobado=reprobado+1

print("Max Calificacion", max(vec))
print("Min calificacion", min(vec))
print("Promedio:", promedio)
print("Superiores a promedio:", npromedio)
print("Cantidad de aprobados:", aprobado)
print("Promedio de aprobados:", promedioAprobados)
print("Desaprobados:", reprobado)

_For:_
Calificaciones=int(input("Ingrese la cantidad de calificaciones"))
vec=[]
n=0

for i in range(1,Calificaciones+1):
    calificacion=int(input("Calificacion: "))
    n=n+calificacion
    vec.append(calificacion)

promedio=n/len(vec)

npromedio=0
for j in vec:
    if j>promedio:
        npromedio=npromedio+1

aprobado=0

#Primero inicializas el contador
promedioAprobados = 0
for h in vec:
    if h>5:
        aprobado=aprobado+1
        #Va sumando cada unas de las notas
        promedioAprobados = promedioAprobados + h

#Luego saca el promedio sumatoria / cantidad de aprobados 
promedioAprobados = promedioAprobados / aprobado

reprobado=0
for k in vec:
    if k<5:
        reprobado=reprobado+1

print("Max Calificacion", max(vec))
print("Min calificacion", min(vec))
print("Promedio:", promedio)
print("Superiores a promedio:", npromedio)
print("Cantidad de aprobados:", aprobado)
print("Promedio de aprobados:", promedioAprobados)
print("Desaprobados:", reprobado)







