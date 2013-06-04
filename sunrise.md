Obliczanie azymutu wschodu Slońca dla dowolnej szerokoci geograficznej i dnia.

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
Po poprawkach. Dzień podawany w normalnej notacji dd m rrrr. Azymut astronomiczny i geograficzny.
```c
#include <stdio.h>
#include <math.h>
int main(){
    int i=0,dd=0, mm=0, m=0, rr=0,r=0, rrr=0;
    double  b=0, x=0, y=0, a=0, n=0, g=0;
    printf ("podaj szerokosc geograficzna w stopniach w przypadku S ze znakiem minus %lf\n", y);
    scanf ("%lf", &y);
    printf ("podaj date dd m rrrr oddzielona spacjami  %d\t %d\t %d\n", dd, mm, rr);
    scanf ("%d %d %d", &dd,&mm,&rr);
     switch (mm)
           {
               case 1:  m=0;
               break;
               case 2 : m=31;
               break; 
               case 3 : m=59;
               break; 
               case 4 : m=90;
               break; 
               case 5 : m=120;
               break; 
               case 6 : m=151;
               break; 
               case 7 : m=181;
               break; 
               case 8 : m=212;
               break; 
               case 9 : m=243;
               break; 
               case 10 : m=273;
               break; 
               case 11 : m=304;
               break; 
               case 12 : m=334;
               break;
           }
          if (rr%4==r)/*sprawdzenie przestepnosci roku*/
             rrr=1;
           else
               rrr=0;
           i=dd+m+rrr;/*numer dnia w roku*/
             x=(y/180)*M_PI;/*zamiana szerokości geograficznej na radiany*/
             b=(23.45*sin(((i-80)*360/365)*M_PI/180))*M_PI/180;/* deklinacja Slonca*/
             a=acos((-(cos(x)*sin(b)))+((sin(x)*cos(b))*(-(tan(x)*tan(b)))));/*azymut wschodu Slonca w radianach*/
             n=a*180/M_PI;/*azymut astronomiczny w stopniach*/
             g=180-n;/*azymut geograficzny*/
             printf(" Azymut wschodu Slonca:\n");
             printf(" astronomiczny /liczony w lewo od kierunku S/  =  %6.2lf\n ", n); 
             printf("geograficzny /liczony w prawo od kierunku N/  =  %6.2lf\n ", g); 
          getchar(),getchar();
          }
```

Dodany komunikat o braku wschodu Slońca, sprawdza cos(azymutu) i szerokoć geograficzna na podstawie których wywietla komunikat "Slonce nie przecina linii horyzontu ".

```c
#include <stdio.h>
#include <math.h>
int main(){
    int i=0,dd=0, mm=0, m=0, rr=0,r=0, rrr=0;
    double  b=0, x=0, y=0, a=0, n=0, g=0, an;
    printf ("podaj szerokosc geograficzna w stopniach w przypadku S ze znakiem minus %lf\n", y);
    scanf ("%lf", &y);
    printf ("podaj date dd m rrrr oddzielona spacjami  %d\t %d\t %d\n", dd, mm, rr);
    scanf ("%d %d %d", &dd,&mm,&rr);
     switch (mm)
           {
               case 1:  m=0;
               break;
               case 2 : m=31;
               break; 
               case 3 : m=59;
               break; 
               case 4 : m=90;
               break; 
               case 5 : m=120;
               break; 
               case 6 : m=151;
               break; 
               case 7 : m=181;
               break; 
               case 8 : m=212;
               break; 
               case 9 : m=243;
               break; 
               case 10 : m=273;
               break; 
               case 11 : m=304;
               break; 
               case 12 : m=334;
               break;
           }
          if (rr%4==r)/*sprawdzenie przestepnosci roku*/
             rrr=1;
          else
               rrr=0;
           i=dd+m+rrr;/*numer dnia w roku*/
             x=(y/180)*M_PI;/*zamiana szerokości geograficznej na radiany*/
             b=(23.45*sin(((i-80)*360/365)*M_PI/180))*M_PI/180;/* deklinacja Slonca*/
             an=((-(cos(x)*sin(b)))+((sin(x)*cos(b))*(-(tan(x)*tan(b)))));
             a=acos((-(cos(x)*sin(b)))+((sin(x)*cos(b))*(-(tan(x)*tan(b)))));/*azymut wschodu Slonca w radianach*/
             n=a*180/M_PI;/*azymut astronomiczny w stopniach*/
             g=180-n;/*azymut geograficzny*/
              if ( y >= 66.56 || y <= -66.56 )
                {
                     if (an<=-1.0 ||an >=1.0)
                     printf("Slonce nie przecina linii horyzontu ");
                     else
                     {
                      printf(" Azymut wschodu Slonca:\n");
                      printf(" astronomiczny /liczony w lewo od kierunku S/  =  %6.2lf\n ", n); 
                      printf("geograficzny /liczony w prawo od kierunku N/  =  %6.2lf\n ", g); 
                      }
                }
              else
              {
             printf(" Azymut wschodu Slonca:\n");
             printf(" astronomiczny /liczony w lewo od kierunku S/  =  %6.2lf\n ", n); 
             printf("geograficzny /liczony w prawo od kierunku N/  =  %6.2lf\n ", g); 
                            /*  printf("a  =  %6.2lf\n ", a); do sprawdzenia popawności wyników   */
                             /*  printf("deklinacja  =  %6.2lf\n ", b); do sprawdzenia popawności wyników   */
                             /*  printf("an = %6.2lf\n", an);    do sprawdzenia popawności wyników   */
              }
          getchar(),getchar();
          }
```
