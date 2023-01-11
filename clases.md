# Clase 1 
## Introducción a la programación
En el curso se utilizarán dos programas para programar, **C** y **C++**

C será utilizado para programación estructurada, mientras que C++ se empleará para programación orientada a objetos.

Para empezar a programar es necesario tener claros varios puntos
- Nuestro *script* será el código como tal.
- Hay compiladores exclusivos para cada SO, nosotros utilizaremos **tdm-gcc**
- El compilador es el encargado de traducir el lenguaje natural a lenguaje binario.

Antes de programar deberemos crear un Workspace, que será la ruta donde todos nuestros archivos estén almacenados.

Los programas que más utilizaremos para crear código serán **Virtual Studio Code** y **GitBash**. Virtual Studio Code nos servirá para poder crear y editar cógidos, mientras que GitBash nos ayudará a integrar diversas versiones de nuestros proyectos.

Algunas extensiones útiles para VSC son:
- C/C++ Runner
- C/C++ Compile Run
- C/C++ Extensio Pack
- Draw.io
- C/C++ Project Generator
- Markdown
  
# Clase 2
## Comandos de Git y Markdown

Los siguientes comandos son los más comunes e útiles de Git 

- ***git version*** para comprobar la versión del Git.
- ***gcc --version*** para comprobar la versión del compilador.
- ***pwd*** para verificar el directorio en el que estamos trabajando.
- ***ls*** para revisar las carpetas de nuestro directorio.
- ***git init*** crea la carpeta .git
- ***git status*** notifica los cambios dentro del código.
- ***git add*** añade todos los documentos a la carpeta *.git* 
- ***gcc carpeta/archivo*** para compilar nuestro código.
  
  
Markdown es utilizado para realizar anotaciones dentro de nuestro código. 
Se denota con la extensión **.md**

Estos son los comando más utilizados de Markdown

  - "#" para crear un título.
  - "##" para crear un subtítulo.
  - Para marcar un texto con negrita se encierra dicho texto entre dos asteriscos, ** texto ** 
  - Para marcar un texto con cursiva se encierra dicho texto entre astericos, * texto *
  - Para resaltar texto se utilizan dos signos de igual, == texto ==
  - Para tachar texto se usan dos tildes, ~~ texto ~~
  - Para agregar viñetas se utiliza un guión, -
  - Para crear separaciones entre el texto se utilizan tres guiones bajos, ___
  - Para crear un cuadro de texto se utilizan tres acentos graves, ```
  - Para colocar una franja en el texto se utiliza el símbolo de mayor que, >
  - Para hipervincular cualquier enlace se utilizan corchetes y paréntesis de la siguiente manera, [texto] (enlace).
  
# Clase 3
Antes de escribir nuestro primer código, debemos saber que:

- En las primeras líneas del código se escriben las librerías.
- Las librerías tienen extensión **.h** y se encierran entre signos de mayor y menor que **< lib >**
- Después de las librerías, escribimos las variables globales y declaramos los procedimientos y funciones.
- Ya por último escribimos todo nuestro código.

```
Hola mundo en C
#include <stdio.h>

void main()
{
    printf("Hola mundo");
}
```
La palabra reservada *void* se utiliza para procedimientos, los procedimientos son tipos de códigos que no devuelven nada.

## Tipos de datos
- int
- float
- double
- char
- smallint
- byte
  
```
#include <stdio.h>

void main ()
{
    char [] nombre="gabriel";
    printf ("Hola %s",nombre);
}
```
```
Sumar dos números

#include <stdio.h>

void main ()
{
    int n1; n2; rta;
    n1 = 10;
    n2= 4;
    rta= n1+n2;
    printf ("La suma es:%i",rta);
}
```
# Clase 4
## Algoritmia
 
Pseudocódigo para determinar el área de un rectángulo.

```
imprimir: "ingrese la base del rectángulo"
leer: base
imprimir: "ingrese la altura del rectángulo"
leer: altura
área= base x altura
imprimir: "El área es "área"
```
**INCLUIR LOS DIAGRAMAS DE FLUJO Y LA TEORÍA**

# Clase 5

Calcular el mayor de dos números
```
#include <stdio.h>

void main()
{
    int a=10, b=20;
    if (a>b)
    {
        printf ("El mayor es %i",a);
    }
    else
    {
        printf ("El mayor es%i", b);
    }
    
}
```
```
#include <stdio.h>

void main ()
{
    int a=7, b=7;
    if (a>b)
    printf ("El mayor es: %i", a);
    else
    print ("El mayor es: %i, b);
    if (a==b)
    printf ("Los números son iguales");
}
```
# Clase 6
## Bucles
**BUSCAR TEORÍA DE BUCLES**

El siguiente código genera una serie de caracteres del tamaño deseado.
```
#include <stdio.h>

void generarSerieSigno(int nroTerminos)
{
    for (int i = 0; i < nroTerminos; i++)
        printf("+ ");
}

void generarSerieSignoAlternos(int nroTerminos)
{
    for (int i = 0; i < nroTerminos; i++)
    {
        if(i%2==0)
            printf("+ ");
        else
            printf("- ");
    }
}

void showCuadrado(int tamano){
    for (int f = 0; f < tamano; f++)
    {
        for (int c = 0; c < tamano; c++)
            if((f==0) || (c==0) || (f==tamano-1) || (c==tamano-1))
                printf("+ ");
            else
                printf("  ") ;
        printf("\n");
    }
}
void showCuadradoSignoAlterno(int tamano){
    char car = '+';
    //int con=0;
    for (int f = 0; f < tamano; f++)
    {
        for (int c = 0; c < tamano; c++)
        {
            car = ((c+f)%2==0)?'+':'-';
            //car = ((con++)%2==0)?'+':'-';
            if((f==0) || (c==0) || (f==tamano-1) || (c==tamano-1))
                    printf("%c ",car);
            else
                printf("  ") ;
        }
        printf("\n");
    }
}

int main(void)
{
    int nroSigno=0;

    printf("Ingrese cantidad de signos: ");
    scanf("%i", &nroSigno);

    // generarSerieSigno(nroSigno);
    // printf("\n\n");
    // generarSerieSignoAlternos(nroSigno);    
    // printf("\n\n ");
    // showCuadrado(nroSigno);
    showCuadradoSignoAlterno(nroSigno);
    return 0;
}
```
# Funciones y modularización
La modularización es una tecnica empleada en programacion para poder crear códigos más cortos.

 Consiste en reducir el código en distintas partes, para poder concentrarse en cada parte por separado.

 En C, denonimamos funciones a aquellas partes del código que utilizamos para dividir un programar para que cada bloque de código realice una tarea determinada.

 ```
 #include <stdio.h>


// función : Tipo de Dato (no void) -> int, float, loble long, short,  ......  [return]
int Suma()
{
    int n1, n2, rta;
    n1 = 10;
    n2 = 23;
    rta = n1 + n2;
    return rta;
}

// función + parametros
int SumaPara(int n1, int n2)
{
    int rta;
    rta = n1 + n2;
    return rta;
}
// funcin que suma nuemros enteros
int SumaParaShort(int n1, int n2)
{
    // forma corta de sumar sin variobles
    return n1 + n2;
}
```

# Clase 7
## Arrays

Los arrays nos ayudan para crear listas.
Se caracterizan por el uso de corchetes [].

_int a: 10;_ Declara una sola variable, mientras que

_int A [n]_ declara un n número de variables.

```
for (int i=0; i<n; i++);
```
Cuando trabajamos con arrays podemos generalizar una variable para evitar escribir demasiado en nuestro código

```
int lenC=15; \\ declaramos la variable
char C [lenC]; \\ creamos el array
```

```
El siguiente código es un ejemplo de el uso de arrays para comprobar si una contraseña es correcta o no

#include <stdio.h>
#include <string.h>

void validaClave()
{
   char clave[10];
   printf("Escriba su clave: ");
   scanf("%9s", clave); 

   if (strcmp(clave, "itsa")==0){
      printf("La clave es correcta");
   }
   else{
      printf("La clave es incorrecta");
   }
}
void showEdades()
{
    char contrasena[]="patoo";
    printf("Contrasena logitud: %i \n",sizeof(contrasena));
    
    int edades[] = {1,2,9,8,16,32,9,50,36,20,1,87};
    int limite = (sizeof(edades)/sizeof(edades[0]));
    printf("Edades logitud: %i \n ",limite);
    for (int i = 0; i < limite; i++)
      printf("%i \n ",edades[i]);
}
```
```
#include <stdio.h>

void main ()
{
    int ParesLong=10;
    int Pares [ParesLong];
    for (int i=0, i<ParesLong, i++)
    {
        Pares [i]=i*2
    }
    ParesMax=Pares[0];
    for (int=1m i<ParesLong;i++)
    {
        if (ParesMax<Pares[i])
        ParMax=Par[i]
    }
    printf ("El mayor número del arrat es: %i", ParesMax);
}
```
# Matrices 
Una matriz es un array multidimensional. Se definen de misma manera que los vectores excepto que se requiere un índice por cada dimensión.
Su sintaxis es la siguiente:

```
tipo nombre [tamaño 1][tamaño 2];
```
Por ahora solo utilizaremos matrices bidimensionales.

```
//Ejemplo de código
#include <stdio.h>
#include <string.h>

void validaClave()
{
   char clave[10];
   printf("Escriba su clave: ");
   scanf("%9s", clave); 

   if (strcmp(clave, "itsa")==0){
      printf("La clave es correcta");
   }
   else{
      printf("La clave es incorrecta");
   }
}
void showEdades()
{
    char contrasena[]="patoo";
    printf("Contrasena logitud: %i \n",sizeof(contrasena));
    
    int edades[] = {1,2,9,8,16,32,9,50,36,20,1,87};
    int limite = (sizeof(edades)/sizeof(edades[0]));
    printf("Edades logitud: %i \n ",limite);
    for (int i = 0; i < limite; i++)
      printf("%i \n ",edades[i]);
}
```

#### Comandos importantes
'a' \\ una sola comilla para caracteres

"abc" \\ dos comillas para cadenas de caracteres

\b retroceso

\n nueva línea

\t tabulador horizontal

\r retroceso de carro

# Clase 8

## Combintoria
La combintaoria es una herramienta que nos permite contar el número de situaciones posibles que se pueden dar al someter un conjunto de datos a ciertas acciones de ordenar sus elementos.
```
#include <stdio.h>
// conbinaciones sin repeticion nCk
long factorial(int numero)
{
	if (numero <= 1) 
		return 1;
	else 
		return (numero * factorial(numero-1));
}
char showArrAsc(char arr[], int inicio)
{
	printf("%c",arr[inicio]);
	if (inicio < sizeof(arr)) 
		return showArrAsc(arr, inicio +1);
}
char showArrDesc(char arr[],int len)
{
	printf("%c",arr[len-1]);
	if (len > 0) 
		return showArrDesc(arr, len-1);
}
int main()
{	
	char alfa[] ={'a','b','c','d'};
	int length = sizeof(alfa);

	int result, number =3;
    result = factorial( number );
	printf("factoria de %i es: %i \n", result, number );

	showArrAsc(alfa, 0);
	printf("\n\n");
	showArrDesc(alfa, sizeof(alfa));
	printf("\n\n");

	for (size_t i = 0; i < length -1 ; i++)
		for (size_t j = i+1; j < length ; j++)
			printf("%c%c \t", alfa[i],alfa[j]);

	for (size_t i = 0; i < length -1 ; i++)
		for (size_t j = i+1; j < length ; j++)
			for (size_t k = j+1; k < length ; k++)
				printf("%c%c%c \t", alfa[i],alfa[j],alfa[k]);

	return (0);
}
```
## Programación en C++

Para empezar a programar en C++ hay que tener en cuenta ciertos aspectos que varían con respecto a C.

Ahora, la extensión de los archivos de código será ***.cpp***

En lugar de usar *printf* utilizaremos ***std::cout<<"texto";***

En lugar de usar *scan* utilizaremos ***std::cin>>i;***

Nuestra librería estándar de C++ será ***#include <iostream>***

Como consejo, podemos incluir al inicio de nuestro código la línea 

```
using namespace std;
```
para evitar escribir ***std*** siempre que lo necesitemos.

# Clase 9
## Archivos

En C, un archivo es un concepto lógico que puede aplicarse a una variedad de campos, desde archivos de disco hasta terminales o una impresora. 

