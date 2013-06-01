Obliczanie azymutu wschodu Slonca

```c
#include <stdio.h>
#include <math.h>
int main(){
    int i;
    double  b, x, y, a, n ;
    printf ("podaj szerokosc geograficzna w stopniach w przypadku S ze znakiem minus %lf\n", y);
    scanf ("%lf", &y);
    printf ("podaj dzien liczony jako nr dnia od poczatku roku %lf\n", i);
    scanf ("%d", &i);
             x=(y/180)*M_PI;
             b=(23.45*sin(((i-81)*360/365)*M_PI/180))*M_PI/180;
             a=acos((-(cos(x)*sin(b)))+((sin(x)*cos(b))*(-(tan(x)*tan(b)))));
             n=a*180/M_PI;
             printf(" azymut wschodu Slonca liczony w stopniach od kierunku S w lewo   %5.2lf\n ", n); 
       
          getchar(),getchar();
          }
```
