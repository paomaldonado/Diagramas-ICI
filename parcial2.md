# Primeros problemas Parcial 2
## 1. Contar del 1 al 10 y sumar los valores. 
### 1.1 Analisis
El algoritmo debe contar desde el 1 hasta el 10 y posteriormente sumar cada valor. 
#### 1.2 Dfd
While: 
[![1-ER-PRBLEMA-WHILE.jpg](https://i.postimg.cc/027n7JRn/1-ER-PRBLEMA-WHILE.jpg)](https://postimg.cc/GHhvCtpT)
Do/While: 
[![1-ER-PROBLEMA-DOWHILE.jpg](https://i.postimg.cc/s2x5HM8t/1-ER-PROBLEMA-DOWHILE.jpg)](https://postimg.cc/9434rQcp)
For:
[![1-ER-PROBLEMA-FOR.jpg](https://i.postimg.cc/C5gB05PM/1-ER-PROBLEMA-FOR.jpg)](https://postimg.cc/wywTcqYn)
##### 1.3 Entrada
Ninguna
##### 1.4 Salida
Conteo del 1 al 10 y suma de estos
###### 1.5 Prueba de escritorio
|Entrada | Salida |
| ----------- | ----------- |
| - | 50 |
###### 1.6 Código
// Contar del 1 hasta el 10 y sumar los valores.
While:
void main(List<String> args) {
  int s = 0, c = 1;

  while (c <= 10) {
    s += c;
    c++;
  }
  print("El resultado de la suma de los valores es:$s");
} //while
For:                
void main(List<String> args) {
  int s = 0;
  for (var i = 1; i <= 10; i++) {
    s += i;
  }
  print("La suma de los valores es: $s");
}//for
    
Do while: 
void main(List<String> args) {
  int s = 0, c = 1;

  do {
    s += c;
    c++;
  } while (c <= 10);
  print("El resultado de la suma de los valores es:$s");
}//Do whilesss


                   

## 2. Obtener la suma de los primeros 5 numeros pares
### 2.1 Analisis
El algoritmo debe sumar 2, 4, 6, 8 y 10.
#### 2.2 Dfd
While: 
[![2-DO-PROBLEMA-WHILE.jpg](https://i.postimg.cc/Cx5x8k9n/2-DO-PROBLEMA-WHILE.jpg)](https://postimg.cc/mPx4fzLT)
Do/While: 
[![2-DO-PROBLEMA-DO-WHILE.jpg](https://i.postimg.cc/Z54rz7Bt/2-DO-PROBLEMA-DO-WHILE.jpg)](https://postimg.cc/jL3Wzh4Z)
For:
[![2-DO-PROBLEMA-FOR.jpg](https://i.postimg.cc/d1y7yrkj/2-DO-PROBLEMA-FOR.jpg)](https://postimg.cc/MMzKkcYn)
##### 2.3 Entrada
Ninguna
##### 2.4 Salida
Resultado de la suma
###### 2.5 Prueba de escritorio
|Entrada | Salida |
| ----------- | ----------- |
| - | 30 |
###### 2.6 Código
//Suma de 5 primeros numeros pares

For:
void main (List<String> args) [
  int s = 0
  for (var i = 2; i <= 10; i+2) [
    s = s + i;
    ]
 print("Resultado de la suma es: $s");
 ]

While: 
void main(List<String> args) {
  int s = 0, c = 0;
  
  while (c <= 5) {
    s = s + c * 2;
    c = c + 1;
    }
  
    print("suma de pares es: $s");

  }
               
 Do while:               
void main(List<String> args) [
  int s = 0, c = 0;

  do [
    s = s + c * 2;
    c= c + 1;
    ] while (c <= 5);
    print("numeros $s");
] 

                    
                    
## 3. Almacenar en un array el numero leído en el teclado. Tamaño del array 10
### 3.1 Analisis
El algoritmo debe almacenar un número en array.
#### 3.2 Dfd
While: 
[![3-ER-PROBLEMA-WHILE.jpg](https://i.postimg.cc/7hCfk7D2/3-ER-PROBLEMA-WHILE.jpg)](https://postimg.cc/p5H2QmmW)
Do/While: 
[![3-ER-PROBLEMA-DOWHILE-1.jpg](https://i.postimg.cc/W4MGBBSv/3-ER-PROBLEMA-DOWHILE-1.jpg)](https://postimg.cc/3yx0pbPS)
For:
[![3-ER-PROBLEMA-FOR.jpg](https://i.postimg.cc/c15nb1Z3/3-ER-PROBLEMA-FOR.jpg)](https://postimg.cc/dDr37YhQ)
##### 3.3 Entrada
Numero
##### 3.4 Salida
Numero almacenado en array
###### 3.5 Prueba de escritorio
|Entrada | Salida |
| ----------- | ----------- |
| 5 | 5 |
###### 3.6 Código
//Leer 10 numeros del teclado y ponerlos en una lista.
                    
While:
  void main() {
  var arra = new List.filled(10, 0);
  stdout.write("Dame diez numeros\n ");
  stdout.write("----------\n");
  int i = 0;
  while (i <= 9) {
    String? s = stdin.readLineSync();
    if (s != null) {
      int ner = int.parse(s);
      arra[i] = ner;
    }
    i++;
  }
  stdout.write("Tu lista es, $arra ");
}

For: 
void main() {
  var arra = new List.filled(10, 0);
  stdout.write("Dame diez numeros\n ");
  stdout.write("----------\n");
  for (var i = 0; i <= 9; i++) {
    String? s = stdin.readLineSync();
    if (s != null) {
      int n = int.parse(s);
      arra[i] = n;
    }
  }
  stdout.write("aqui esta la lista, $arra");
}

Do While:
  void main() {
  var arra = new List.filled(10, 0);
  stdout.write("Dame diez numeros\n ");
  stdout.write("----------\n");
  int i = 0;
  do {
    String? s = stdin.readLineSync();
    if (s != null) {
      int n = int.parse(s);
      arra[i] = n;
      i++;
    }
  } while (i <= 9);
  stdout.write("Tu lista es $arra ");
}                      
  
  
## 4. Almacenar n numeros leídos en el teclado en un vector.
### 4.1 Analisis
El algoritmo debe almacenar todos los números en un vector
#### 4.2 Dfd
While: 
[![4-TP-PROBLEMA-WHILE.jpg](https://i.postimg.cc/CMNNLnDf/4-TP-PROBLEMA-WHILE.jpg)](https://postimg.cc/Yjvgd9dp)
Do/While: 
[![4-TP-PROBLEMA-DOWHILE.jpg](https://i.postimg.cc/BQbxSY4d/4-TP-PROBLEMA-DOWHILE.jpg)](https://postimg.cc/bsXGLRGT)
For:
[![4-TP-PROBLEMA-FOR.jpg](https://i.postimg.cc/50mw0DHM/4-TP-PROBLEMA-FOR.jpg)](https://postimg.cc/dkL7NHmW)
##### 4.3 Entrada
n numeros
##### 4.4 Salida
Numeros almacenado en un vector
###### 4.5 Prueba de escritorio
|Entrada | Salida |
| ----------- | ----------- |
| n | numeros en vector |
###### 4.6 Código
Do while: 
  void main() {
  var arra = new List.filled(10, 0);
  stdout.write("Dame diez numeros\n ");
  stdout.write("----------\n");
  int i = 0;
  do {
    String? s = stdin.readLineSync();
    if (s != null) {
      int n = int.parse(s);
      arra[i] = n;
      i++;
    }
  } while (i <= 9);
  stdout.write("Tu lista es $arra ");
}

While:
void main() {
  var arra = new List.filled(10, 0);
  stdout.write("Dame diez numeros\n ");
  stdout.write("----------\n");
  int i = 0;
  while (i <= 9) {
    String? s = stdin.readLineSync();
    if (s != null) {
      int ner = int.parse(s);
      arra[i] = ner;
    }
    i++;
  }
  stdout.write("Tu lista es, $arra ");
}                  

For:
void main() {
  var arra = new List.filled(10, 0);
  stdout.write("Dame diez numeros\n ");
  stdout.write("----------\n");
  for (var i = 0; i <= 9; i++) {
    String? s = stdin.readLineSync();
    if (s != null) {
      int n = int.parse(s);
      arra[i] = n;
    }
  }
  stdout.write("aqui esta la lista, $arra");
}  
  
  
## 5. Almacenar un contador negativo
### 5.1 Analisis
El algoritmo debe almacenar un conteo del 10 al 0 en un vector
#### 5.2 Dfd
While: 
[![5-TO-PROBLEMA-WHILE.jpg](https://i.postimg.cc/nr3cwfzT/5-TO-PROBLEMA-WHILE.jpg)](https://postimg.cc/K3g2RVtg)
Do/While: 
[![5-TO-PROBLEMA-DOWHILE.jpg](https://i.postimg.cc/ZqzZH5H4/5-TO-PROBLEMA-DOWHILE.jpg)](https://postimg.cc/759pYDjW)
For:
[![5-TO-PROBLEMA-FOR.jpg](https://i.postimg.cc/V61ffk0D/5-TO-PROBLEMA-FOR.jpg)](https://postimg.cc/VSGQ41RC)
##### 5.3 Entrada
ninguna
##### 5.4 Salida
Numeracion del 10 al 0 en un vector.
###### 5.5 Prueba de escritorio
|Entrada | Salida |
| ----------- | ----------- |
| - | 10 9 8 7 6 5 4 3 2 1 0 |
###### 5.6 Código
 While: 
 void main() {
  var arr = <int>[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
  int c = 10;
  while (c >= 0) {
    arr[10 - c] = c;
    c = c - 1;
  }
  print(arr);
}                       

For:   
void main() {
  var arr = <int>[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
  int c = 10;
  for (var i = 10; i >= 0; i--) {
    arr[10 - i] = i;
  }
  print(arr);
}
  
Do While: 
  void main() {
  var arr = <int>[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
  int c = 10;
  do {
    arr[10 - c] = c;
    c = c - 1;
  } while (c >= 0);
  print(arr);
}
                        

## 6. Almacenar en un vector tamaño 10 todos los numeros pares capturados.
### 6.1 Analisis
El algoritmo debe almacenar los numerospares introducidos en un vector de tamaño 10.
#### 6.2 Dfd
While: 
[![6-TO-PROBLEMA-WHILE.jpg](https://i.postimg.cc/J4CvMccc/6-TO-PROBLEMA-WHILE.jpg)](https://postimg.cc/mhV8S9nt)
Do/While: 
[![6-TO-PROBLEMA-DOWHILE.jpg](https://i.postimg.cc/KzRS3GRP/6-TO-PROBLEMA-DOWHILE.jpg)](https://postimg.cc/DJkYtKQ0)
For:
[![6-TO-PROBLEMA-FOR.jpg](https://i.postimg.cc/PqV0jg2P/6-TO-PROBLEMA-FOR.jpg)](https://postimg.cc/FfcTbBt4)
##### 6.3 Entrada
Numeros pares
##### 6.4 Salida
Numeros introducidos en un vector
###### 6.5 Prueba de escritorio
|Entrada | Salida |
| ----------- | ----------- |
| 2,4,6,8,10 | 2 4 6 8 10 |
###### 6.6 Código

 While: 
 listanumeros = []
numerousuario = int(input("introduzca un numero: "))
listanumeros.append(numerousuario)
decision = input("¿desea añadir mas numeros?: ")

while decision == "s" or decision == "s":
    numerousuario = int(input("introduzca otro numero: "))
    listanumeros.append(numerousuario)
    decision = input("¿desea añadir otro numero?: ")


print(f"los numeros son {listanumeros}")
for n in listanumeros:
    if n % 2 == 0:
        print("Este numero de la lista es par" + str(n))
        


input("por favor, precione una tecla para salir.")
  
 Do While: 
  print("PARES")
numero_1 = int(input("Escriba un número entero: "))
numero_2 = int(input(f"Escriba un número entero mayor o igual que {numero_1}: "))

if numero_2 < numero_1:
        print(f"¡Le he pedido un número entero mayor o igual que {numero_1}!")
else:
        for i in range(numero_1, numero_2 + 1):
            if i % 2 == 0:
                print(f"El número {i} es par.")
                       
  For: 
 listanumeros = []
numerousuario = int(input("introduzca un numero: "))
listanumeros.append(numerousuario)
numerousuario = int(input("introduzca otro numero: "))
listanumeros.append(numerousuario)
numerousuario = int(input("introduca un numero: "))
listanumeros.append(numerousuario)
numerousuario = int(input("introduzca otro numero: "))
listanumeros.append(numerousuario)
numerousuario = int(input("introduzca un numero: "))
listanumeros.append(numerousuario)
numerousuario = int(input("introduzca otro numero: "))
listanumeros.append(numerousuario)
numerousuario = int(input("introduzca un numero: "))
listanumeros.append(numerousuario)
numerousuario = int(input("introduzca otro numero: "))
listanumeros.append(numerousuario)
numerousuario = int(input("introduzca un numero: "))
listanumeros.append(numerousuario)
numerousuario = int(input("introduzca otro numero: "))
listanumeros.append(numerousuario)

print(f"los numeros son {listanumeros}")

def pares(listanumeros):
    listanumeros = []


for n in listanumeros:
    if n % 2 == 0:
        print("Estos numeros son pares"+ "  " + str(n))                      
