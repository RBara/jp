jp
==

Języki programowania
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
Zbuduj trójkat  - choinkę zudowaną ze znaków * o zadeklarowanej liczbie wierszy.</b><br> 
Pętla for. 
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
<b>Wyświetl liczby od 0 do 23</b><br>
<br>
Wersja z pętlą for.
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

Wersja z pętlą while.
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

Wersja z pętlą do-while.
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
<b>Wypisz liczby od - 3.5 do 7.5 z krokiem co 0.5 za pomocą pętli do-while.</b><br>
Pętla do-while. 
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
<b>Wczytaj n liczb i wyświetl ich sumę i średnią arytmetyczną</b><br>
 zapis srednia=suma/(double)n;  oznacza, że od tego miejsca liczba n jest traktowana jako zmiennoprzecinkowa<br>
wersja z pętlą while<br>
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
wersja druga z pętlą do-while<br>
```c
#include <stdio.h>
int main(){
    int i, n;
    double srednia, suma=0.0, x ;
```
<i>pętla do-while
jeżeli n<1 powtórzy pętlę, bo warunek sprawdzany jest na koncu pętli, a potem i++</i>
```c
    do{
    printf("podaj ilosc liczb n");
    scanf("%d",&n);
}
    while (n<1);
```
<i>pętla for </i>  
```c
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
<br>
<b>Zad 9</b><br>
<i>/jest to zadanie nr 4 z kartki nr 1/</i><br>
<b>Wypisz kwadraty i sześciany liczb naturalnych od 1 do n </b><br>
 pętla for<br>
```c
#include <stdio.h>
int main(){
    int i, n;
    do{
    printf("podaj liczbe n: ");
    scanf("%d",&n);
}
    while (n<1);
    
    for(i=1; i<=n; i++){
          printf("liczba \t %d \t kwadrat \t %d \t szescian \t %d \n",i,
          i*i, i*i*i );
          }
          getchar(),getchar();
}
```

<i>wersja z pętlą do-while </i>
```c
#include <stdio.h>
int main(){
    int i=1, n;
    do{
    printf("podaj liczbe n: ");
    scanf("%d",&n);
}
    while (n<1);
    do{
    printf("liczba \t %d \t kwadrat \t %d \t szescian \t %d \n",i,
          i*i, i*i*i );
          i++;
          }          
    while (i<=n);
          getchar(),getchar();
}
```
   
 <i>wersja z pętlą while </i>  
```c
#include <stdio.h>
int main(){
    int i=1, n;
    do{
    printf("podaj liczbe n: ");
    scanf("%d",&n);
}
    while (n<1);
    while (i<=n){
    printf("liczba \t %d \t kwadrat \t %d \t szescian \t %d \n",i,
          i*i, i*i*i );
          i++;
          }          
          getchar(),getchar();
}
```
          
<br>
<b>Zad 10</b><br>
<i>/jest to zadanie nr 5 z kartki nr 1/</i><br>
<b>Oblicz za pomocą pętli for i while sume kwadratow liczb  od 3 do 15 </b><br>
x - oznacza sume kwadratow<br>
petla for
```c
#include <stdio.h>
int main(){
    int i, x=0,;
    for(i=3; i<=15; i++){
             x=x+(i*i);  
           }
           printf(" %d \n",x);
          getchar(),getchar();
}
```
petla while
```c
#include <stdio.h>
int main(){
    int i=3, x=0,;
    while (i<=15){
             x=x+(i*i); 
             i++; 
           }
           printf(" %d \n",x);
          getchar(),getchar();
}
``` 

<br>
<b>Zad 11</b><br>
<i>/jest to zadanie nr 6 z kartki nr 1/</i><br>
<b>Wypisz sin i cos katow 0-180 stopni z krokiem co 30 stopni za pomoca petli for </b><br>
```c
#include <stdio.h>
#include <math.h>
int main(){
    double  i, x=0;
    for(i=0; i<=180; i=i+30){
             x=(i/180)*M_PI;
              printf(" kat %4.0lf stopni \t  sin %5.2lf  \t cos %5.2lf\n ", i, sin(x), cos(x) ); 
           }  
          getchar(),getchar();
          }
```
<br>
<b>Zad 12</b><br>
<i>/jest to zadanie nr 7 z kartki nr 1/</i><br>
<b>Wypisz znaki od 'a' do 'k' wraz z ich kodem ASCII dziesietnie dec i szesnastkowo hex w kolejnosci rosnacej i malejacej</b><br>
char - znak
%c - znak
%d - kod ASCII dec
%x - kod ASCII hex
rosnaco

```c
#include <stdio.h>
int main(){
    char i;
    for(i='a'; i<='k'; i++){
              printf(" %c w ASCII w dec to: %3.0d w hex to: %3.0x \n", i,i,i); 
           }  
          getchar(),getchar();
          }

```
wersja ze znakami od 32 do 127 - petla sie nie konczy bo 127 to 01111111 jak zwiekszymy o 1 czyli dodamy 0000001 to wyjdzie 1000000 czyli (-128), a to jest mniejsze od 127 i program leci od poczatku
```c
#include <stdio.h>
int main(){
    char i;
    for(i=32; i<=127; i++){
              printf(" %c w ASCII w dec to: %3.0d w hex to: %3.0x \n", i,i,i); 
           }  
          getchar(),getchar();
          }
```
zeby zadzialalo mozna np. zmniejszyc zakres i do 126

<br>
<b>Zad 12</b><br>
<i>/jest to zadanie nr 7 z kartki nr 1/</i><br>
<b>Wnapisz pętlę while wypisującą na ekran znaki podane przez uzytkownika, aż do napotkania znaku 'x'</b><br>
c=getchar(); - pobiera znak z klawiatury
```c
#include <stdio.h>
int main(){
    char  c;
   while(c!= 'x'){
              printf(" podaj litere\n"); 
               c=getchar();
               getchar();
           }  
          getchar();
          return 0;
          }
```
można też tak:
```c 
while((c=getchar())!= 'x')
```

<br>
<b>Zad 12</b><br>
<i>/jest to zadanie nr 7 z kartki nr 1/</i><br>
<b>Napisz program wyświetlający tabliczkę mnożenia do 13 - użyj pętli</b><br>
} putchar('\n'); - to oznacza żeby po wykonaniu pętli zagnieżdżonej pszeszedł do następnej linijki<br>
pętla for wewnątrz pętli for daje mnożenie wierszami i przeskok o jeden wiersz
```c
#include <stdio.h>
int main(){
    int i,n;
    for(i=1; i<=13; i++){ 
             for(n=1; n<=13; n++){
             printf("%4d",i*n);
             } putchar('\n');
             }
          getchar(),getchar();
}
```
<b> PĘTLE WARUNKOWE </b><br><br>
<b>
Zad 1<br>
Napisz program liczący pierwiastki trójmianu kwadratowego ax^2+bx+c=0</b><br>
pętla while dla pozbycia się przypadku a=0, czyli braku trójmianu kwadratowego 
```c
#include <stdio.h>
#include <math.h>
int main() {
double a=0,b=0,c=0, d, x ,x1, x2;
printf("podaj wspolczyniki trojmianu kwadratowego  ax^2+bx+c, \n");
scanf("%lf %lf %lf" , &a, &b, &c);
while (a==0){
printf("podaj a rozne od zera, \n");
scanf ("%lf" , &a);
}
d=(b*b)-(4*a*c);
    if (d>0){
    x1=((-b)-(sqrt(d)))/(2*a);
    x2=((-b)+(sqrt(d)))/(2*a);
    printf("pierwiastek  x1 = %lf\n", x1);
    printf("pierwiastek  x2 = %lf", x2);
    }
    else {if (d==0){
        x=(-b)/(2*a);
        printf("pierwiastek  x1=x2= %lf", x);
        }
        else 
        printf("brak pierwiastkow rzeczywistych");
        }
getchar(), getchar() ;
}
```
<b>Zad 2<br>
Znajdź liczby o tej własności, że suma dzielników właściwych liczby jest równa zadanej liczbie, np. 6=1+2+3. Są to tzw. liczby doskonałe.</b>
```c
#include <stdio.h>
#include <math.h>
int main() {
int i,s,n;
for (n=2; n<10000; n++){
    s=0;
    for(i=1; i<n; i++){
         if (n%i==0){
         s=s+i;
             }
    }
    if(s==n)
             printf("%d \n" , n);
}
getchar(), getchar() ;
return 0;
}
```
<b>Zad 3<br>
Wyświetl 20 róznych (bez permutacji) trójek pitagorejskich, tzn. takich liczb całkowitych dodatnich a, b, c, że a^2+b^2=c^2</b>


```c
#include <stdio.h>
#include <math.h>
int main(){
    int a,b,c,i;
    i=1;
   
    for(c=1; c<=100; c++){ 
             for(b=1; b<c; b++)
                      for(a=1; a<b; a++){
                               if (a*a+b*b==c*c && i<=20){
             printf("%d %d %d\n",a,b,c);
           i++;
               } 
             }
             }
                  
          getchar(),getchar();
          return 0;
}
```

```c
#include <stdio.h>
#include <math.h>
int main(){
    double zero=0.0;
    double max=-1/zero; 
    double min=1/zero; 
    double x;
    int n, i;
    printf("podaj ilosc liczb n:");
    scanf("%d", &n);
  
    for(i=1; i<=n; i++){
    printf("podaj liczbe");
    scanf("%lf", &x);
    if (x<max){        
    printf("najwieksza %5.5lf\n",max);
    }
    else { 
         printf("najwieksza %5.5lf\n",x);
        max=x;
         }
            if (x>min){        
    printf("najmniejsza %5.5lf\n",min);
    }
    else { 
         printf("najmniejsza %5.5lf\n",x);
        min=x;
         }
          }      
          getchar(),getchar();
          return 0;
}
```
<b>
Zad 5<br>
Napisz program wypisujący słownie dzień tygodnia, jeżeli nr dnia tygodnia jest znany jako liczba.</b><br>
Użycie instrukcji warunkowej <b>switch-case</b>
```c
#include <stdio.h>
int main() {
int n;
printf("podaj numer dnia tygodnia, \n");
scanf("%d" , &n);
switch (n)
{
       case 1:  printf ("poniedzialek");
       break;
        case 2 : printf ("wtorek");
       break; 
       case 3 :printf ("sroda");
       break; 
       case 4 : printf ("czwartek");
       break; 
       case 5 : printf ("piatek");
       break; 
       case 6 : printf ("sobota");
       break; 
       case 7 : printf ("niedziela");
       break;
       default: printf ("nie ma takiego dnia tygodnia");
    break;
}
getchar (),getchar ();
return 0;
}
```
<b> ZADANIA</b><br><br>
<b>
Zad 1<br>
Napisz funkcję obliczająca pole koła</b><br>
```c
#include <stdio.h>
#include <math.h>
int main() {
double n=0,s=0;
printf("podaj promien kuli  r: \n");
scanf("%lf" , &n);
       s=4*M_PI*n*n;
       printf("Powierzchna kuli %lf ", s);
getchar (),getchar ();
return 0;
}
```
<b>Zad 2 <br>
Napisz funkcję wartBezwzgledna zwracającą wartość bezwzględną z liczby całkowitej</b>
```c
#include <stdio.h>
int wartBezwzgledna(int n);
int main() {
       int n=0;
       printf("podaj liczbę calkowita : \n");
       scanf("%d" , &n);
       n=wartBezwzgledna (n);
       printf("Wartosc bezwzgledna %d \n" , n);
       getchar ();
       getchar ();
       return 0;
}
int wartBezwzgledna(int n){
       if (n<=0)
       n=-n; 
       return n;
}
```
<b>Zad 3<br>
Napisz funkcję obliczającą a^n dla n należącego do N za pomocą pętli.</b>
```c
#include <stdio.h>
double potega(double a, int n);
int main() {
int n;
double a, w;
printf("podaj liczbe a: \a");
scanf("%lf" , &a);
printf("do jakiej potegi chcesz podniesc: ");
scanf("%d" , &n);
w=potega(a,n);
printf("Wartosc  a^n=%lf " , w);
getchar (),getchar ();
return 0;
}
double potega(double a, int n){
int k=0;
double iloczyn=1;
while (k<n) {
      iloczyn=iloczyn*a;
k++;
}
return iloczyn;
}
```
<b>Zad 4<br>
Napisz funkcję obliczającą pierw a algorytmem Harona</b>
```c
#include <stdio.h>
#include <math.h>
double pierw(double a);
int main (){
    double a, x, z;
printf("podaj liczbę a : \n");
scanf("%lf" , &a);
x=pierw(a);
printf(" wartosc pierwiastka %lf", x);  
for(z=1e-5; z<=1e15; z=z*10){
            printf("pierw(%lf)=%lf\n",z,pierw(z));  
            printf("-sqrt(%lf)=%lf\t",z,sqrt(z)); 
            printf("blad wzgledny=%.15le\n",(pierw(z)-sqrt(z))/sqrt(z)); 
            }
getchar();
getchar();
return 0;
}         
double pierw(double a){
   double x=1,eps=1e-11 ;   
  do{
          x=(x+a/x)*0.5; 
          }
          while (fabs(x-a/x)>eps*x);
          return x; 
          }
```
<b>Zad 5<br>
Algorytm na a^n zamienić na funkcję</b>
```c
#include <stdio.h>
#include <math.h>
double pierw(double a);
int main (){
    double a,p=1,q;
    int n,i;
printf("podaj liczbę a : \n");
scanf("%lf" , &a);
printf("podaj liczbę n : \n");
scanf("%d" , &n);
   q=a;
 i=n;
while(i>0){ 
if (i%2!=0)p=p*q;
q=q*q;
i=i/2;
}
printf("a^n=%lf", p);
getchar();
getchar();
return 0;
}   
```
