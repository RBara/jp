<b>JEZYKI   PROGRAMOWANIA</b><br><br>
<b>ZAJECIA 1<br><br>
Zad 1<br>
Wyswietl sume, różnice, iloczyn i iloraz dwóch liczb calkowitych.<br></b>
<br>
<b>Wersja 1</b><br>
pokaże  błąd przy dzieleniu, bo zadeklarowano liczby calkowite int a,b
```c
#include <stdio.h>
int main(){
 int a,b;
 a=3;
 b=7;
 printf ("%d*%d=%d\n", a,b, a*b);
 printf ("%d/%d=%d\n", a,b, a/b);
 printf ("%d+%d=%d\n", a,b, a+b);
 printf ("%d-%d=%d\n", a,b, a-b);
 getchar();
 return 0;
}
```

<b>Wersja 2</b><br>
pokaże wszystkie odpwiedzi jako zmiennoprzecinkowe np. 21.000000, bo zadeklarowano zmiennoprzecinkowe double a,b
```c
#include <stdio.h>
int main(){
 double a,b;
 a=3;
 b=7;
 printf ("%lf*%lf=%lf\n", a,b, a*b);
 printf ("%lf/%lf=%lf\n", a,b, a/b);
 printf ("%lf+%lf=%lf\n", a,b, a+b);
 printf ("%lf-%lf=%lf\n", a,b, a-b);
 getchar();
 return 0;
}
```

<b>Wersja 3</b><br>
pokaże sumę, różnicę, iloczyn jako liczby całkowite /zmiennoprzecinkowe ale z zerem miejsc po przecinku, <br>a dzielenie z miejscami po przecinku.
```c
#include <stdio.h>
int main(){
 double a,b;
 a=3;
 b=7;
 printf ("%.0lf*%.0lf=%.0lf\n", a,b, a*b);
 printf ("%lf/%lf=%lf\n", a,b, a/b);
 printf ("%.0lf+%.0lf=%.0lf\n", a,b, a+b);
 printf ("%.0lf-%.0lf=%.0lf\n", a,b, a-b);
 getchar();
 return 0;
}
```
<b><br>Zad 2<br>
Oblicz obwód kola o promieniu r<br>
<br>
Wersja 1</b><br>
z dolaczona #include <math.h>, żeby liczylo pi /jako M_PI/, czyli podstawi samodzielnie wartosć pi<br>
Poda wartosc obwodu kola wraz z obliczeniami 
```c
#include <stdio.h>
#include <math.h>
int main(){
 double r;
 int a;
 a=2;
 printf ("podaj promień okręgu %lf\n", r);
 scanf ("%lf", &r);
 printf ("%d*%lf*%lf=%lf\n", a, M_PI, r, a*M_PI*r);
 getchar();
 getchar();
 return 0;
}
```

<b>Wersja 2</b><br>
z dolaczeniem #include <math.h><br>
Poda wartosci obwodu i pola kola wraz z obliczeniami
```c
#include <stdio.h>
#include <math.h>
int main(){
 double r;
 int a;
 a=2;
 printf ("podaj promień okręgu r %lf\n", r);
 scanf ("%lf", &r);
 printf ("%d*%lf*%lf=%lf\n", a, M_PI, r, a*M_PI*r);
 printf ("%lf*%lf=%lf\n", M_PI, r*r, M_PI*r*r);
 getchar();
 getchar();
 return 0;
}
```

<b>Wersja 3</b><br>
z dolaczeniem #include <math.h><br>
Poda wartosci obwodu i pola kola wraz z obliczeniami i tekstem
```c
#include <stdio.h>
#include <math.h>
int main(){
 double r;
 int a;
 a=2;
 printf ("podaj promień okręgu r %lf\n", r);
 scanf ("%lf", &r);
 printf ("%d*%lf*%lf=%lf Obwod kola\n", a, M_PI, r, a*M_PI*r);
 printf ("%lf*%lf=%lf Pole kola\n", M_PI, r*r, M_PI*r*r);
 getchar();
 getchar();
 
 return 0;
}
```

<b>Wersja 4</b><br>
z dolaczeniem #include <math.h><br>
Poda wartosci obwodu i pola kola wraz z obliczeniami i tekstem wyswietlonym przy zastosowaniu puts <br>i podwójnego getchar do przechodzenia dalej enterem
```c
#include <stdio.h>
#include <math.h>
int main(){
 double r;
 int a;
 a=2;
 printf ("podaj promień okręgu r %lf\n", r);
 scanf ("%lf", &r);
  puts("Obwod kola");
 printf ("%d*%lf*%lf=%lf\n", a, M_PI, r, a*M_PI*r);
 getchar();
 getchar();
 puts("Pole kola");
 printf ("%lf*%lf=%lf\n", M_PI, r*r, M_PI*r*r);
 getchar();

 return 0;
}
```

<b>Wersja 5</b><br> 
z dolaczeniem #include <math.h><br>
Poda wartosci obwodu i pola kola bez widocznych obliczen, tylko wynik i tekst
```c
#include <stdio.h>
#include <math.h>
int main(){
 double r;
 int a;
 a=2;
 printf ("podaj promień okręgu r %lf\n", r);
 scanf ("%lf", &r);
 printf ("Obwod kola %lf\n", a*M_PI*r);
 getchar();
 getchar();
 printf ("Pole kola %lf\n", M_PI*r*r);
 getchar();

 return 0;
}
```

<b>Wersja 6</b><br>
z dolaczeniem #include <math.h><br>
Poda wartosci obwodu i pola kola bez widocznych obliczen, <br>tylko wynik i opis wraz z podaniem dla jakiego promienia r
```c
#include <stdio.h>
#include <math.h>
int main(){
 double r;
 int a;
 a=2;
 printf ("podaj promień okręgu r %lf\n", r);
 scanf ("%lf", &r);
 printf ("Obwod kola o promieniu %lf wynosi %lf\n", r, a*M_PI*r);
 getchar();
 getchar();
 printf ("Pole kola o promieniu %lf wynosi %lf\n", r, M_PI*r*r);
 getchar();

 return 0;
}
```
<br>
<b>Zad 3<br>
Przelicz  F na C<br>
<br>
Wersja 1</b><br>
Zastosowanie while,<br> 
Zamieni F na C w zakresie od 0F do 300F z krokiem 20F int czyli tylko wartosci cakowite
```c
#include <stdio.h>
int main(){
int fahr, celsius;
int lower, upper, step;
lower=0;
upper=300;
step=20;
fahr=lower;
while (fahr<=upper){
      celsius=5*(fahr-32)/9;
      printf("%d\t %d\n", fahr, celsius);
      fahr=fahr+step;
                     }
 getchar();

 return 0;
}
```

<b>Wersja 2</b><br>
Zastosowanie while,<br> 
Zamieni stopnie F na C od 0F do 50F ale wynik z dokladnocia do jednego miejsca po przecinku, <br>czyli używamy zmiennoprzecinkowych - zamieniamy int na double i %d na %lf

```c
#include <stdio.h>
int main(){
double fahr, celsius;
int lower, upper, step;
lower=0;
upper=50;
step=1;
fahr=lower;
while (fahr<=upper){
      celsius=5*(fahr-32)/9;
      printf("%.1lf\t %.1lf\n", fahr, celsius);
      fahr=fahr+step;
                     }
 getchar();

 return 0;
}
```

<b>Wersja 3</b><br>
Zastosowanie while,<br> 
To samo co Wersja 2, ale ladnie wyswietli wyniki przecinkami jeden pod drugim
```c
#include <stdio.h>
int main(){
double fahr, celsius;
int lower, upper, step;
lower=0;
upper=50;
step=1;
fahr=lower;
while (fahr<=upper){
      celsius=5*(fahr-32)/9;
      printf("%5.1lf\t %7.1lf\n", fahr, celsius);
      fahr=fahr+step;
                     }
 getchar();
 return 0;
}
```

<b>Wersja 4</b><br>
Zastosowanie for , #define LOWER 0 itd<br> 
Jak w Wersji 1, ale przy #define STEP 0 daje niekonczaca sie petle <br>
wywietlac bedzie zera w nieskonczonosc i żeby wyjsc to wcisnac ctrl+c<br> 
Zmiana STEP na np. 20 da normalna petle<br> 
i zamieni F na C w zakresie od 0F do 300F z krokiem 20F 
```c
#include <stdio.h>
#define LOWER 0
#define UPPER 300
#define STEP 0
int main(){
int fahr, ;
for(fahr=LOWER; fahr<=UPPER; fahr=fahr+STEP)
printf("%3d %6.1lf\n", fahr,(5.0/9.0)*(fahr-32.0));
 getchar();
 return 0;
}
```
<br>
<b>Zad 4<br>
Oblicz n-ty wyraz (Un) ciagu Fibonacciego.</b><br>
<br>
Petla do-while <br>
```c
#include <stdio.h>
int main()
{
int u1, u2, u3;/*na kolejne wyrazy ciągu*/
int n;  /*nr wyrazu*/
int i; /*licznik*/
do
  { printf ("podaj numer wyrazu (co najmniej 3): ");
   scanf ("%d", &n);
  }
  while (n<3);
  u2=u1=1; /*dwa pierwsze wyrazy*/
  i=2;
  while (i++ < n) /*dziala tylko dla n>2 i++ najpierw sdprawdza i z n potem zwieksz o jeden*/
   {u3=u1+u2;
    u1=u2;
    u2=u3;
   }
   /*inna możliwość*/
   /*for (i=3; i<=2; i++, u1=u2, u2=u3) u3=u1+u2; */
   printf ("Wyraz o numerze %d ma wartość %d" , n, u3);
 getchar(); getchar();
 return 0;
}
```

<br>
<b>Zad 5<br>
Zbuduj trojkat  - choinke zudowana ze znakow * o zadeklarowanej liczbie wierszy.</b><br> 
Petla for. 
```c
#include <stdio.h>
#define znak '*' /*znak wypelnienia*/
int main()
{
int lbwier;/*calkowita liczba wierszy*/
int lw;  /*licznik wierszy*/
int lodst; /*liczba odstepow poprzedzajacych gwiazdke*/
int j;

  printf ("ile wierszy? ");
   scanf ("%d", &lbwier);
   
   for (lw=0 ; lw<lbwier ; lw++)
   { lodst = lbwier-lw-1;
     for (j=0 ; j<lodst ; j++) putchar (' '); /* putchar-wstaw (' ')-puste miejsce*/
     for (j=0 ; j<2*lw+1 ; j++) putchar (znak); /* (znak)-wstaw * */
     putchar('\n');
   }
 getchar(); getchar();
 return 0;
}
```

<br>
<b>Zad 6 </b><br>
<i>/jest to zadanie nr 1 z kartki nr 1/</i><br>
<b>Wyswietl liczby od 0 do 23</b><br>
<br>
Wersja z petla for.
```c
#include <stdio.h>
int main()
{
int i;
i=0;
 for( i=0; i<24; i++)
 {
    printf ("%d\n", i);
 }
 getchar(); getchar();
 return 0;
}  
```

Wersja z petla while.
```c
#include <stdio.h>
int main()
{
int i;
i=0;
 while( i<24)
 {
      printf ("%d\n", i);
      i++;
 }
 getchar(); getchar();
 return 0;
}
```

Wersja z petla do-while.
```c
#include <stdio.h>
int main()
{
int i,;
i=0;
do
  { printf ("%d\n", i);
  i++;
  }
  while (i<24);
 getchar(); getchar();
 return 0;
} 
```

<br>
<b>Zad 7</b><br>
<i>/jest to zadanie nr 2 z kartki nr 1/</i><br>
<b>Wypisz liczby od - 3.5 do 7.5 z krokiem co 0.5 za pomoca petli do-while.</b><br>
Petla do-while. 
```c
#include <stdio.h>
int main()
{
double i,n;
i=-3.5;
n=7.5;
do
  { printf ("%.1lf\n", i);
  i=i+0.5;
  }
  while (i<=n);
 getchar(); getchar();
 return 0;
} 
```
<br>
<b>Zad 8</b><br>
<i>/jest to zadanie nr 3 z kartki nr 1/</i><br>
<b>wczytaj n liczb i wyswietl ich sume i srednia arytmetyczna</b><br>
<b> zapis srednia=suma/(double)n;  oznacza, ze od tego miejsca liczba n jest traktowana jako zmiennoprzecinkowa</b><br>
<b>wersja z petla while</b><br>
```c
#include <stdio.h>
int main(){
    int i, n , suma, x;
    double srednia;
    suma=0;
    i=0;
    puts("podaj ilosc liczb n");
    scanf("%d",&n);
    while (i<n){
          printf("podaj liczbe");
          scanf("%d",&x);
          i++;
          suma=suma+x;
          }
          puts("suma");
          printf("%d\n", suma);
          srednia=suma/(double)n;
          puts("srednia");
          printf("%.2lf\n", srednia);
          getchar(),getchar();
}
```
<b>wersja druga z petla do-while</b><br>
```c
#include <stdio.h>
int main(){
    int i, n;
    double srednia, suma=0.0, x ;
    do{
    printf("podaj ilosc liczb n");
    scanf("%d",&n);
}
    while (n<1);
    for(i=1; i<=n; i++){
          printf("podaj %d liczbe:",i);
          scanf("%lf",&x);
          suma=suma+x;
          }
          srednia=suma/n;
          printf("suma podanych %d liczb wynosi: %.3lf",n, suma);
          printf("srednia wynosi: %.3lf",srednia);
          getchar(),getchar();
}
```
