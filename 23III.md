<b> PETLE WARUNKOWE </b><br><br>
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
