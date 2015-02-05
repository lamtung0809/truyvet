# truyvet
#include <stdio.h>
#include <conio.h>

 
int main()
{
int a[n];
int l[n]; 
int t[n]; 
l[0] = 1;
	t[0] = -1; 
for (int i=1; i<n; i++)
{
 int max = 0; 
for (int j=0; j<i; j++)
if (a[j] < a[i] && max < l[j] + 1)
{
max = l[j] + 1;
t[i] = j; 
}
l[i] = max;
}


int lMax = 0; 
int viTriMax = 0; 
for (int i=1; i<n; i++)
if (l[i] > lMax)
{
lMax = l[i];
viTriMax = i;
}


int kq[n]; 
int k = lMax-1;
do {
kq[k] = a[viTriMax];
k--;
viTriMax = t[viTriMax];
}while (k>=0);


printf("\n- Day A: "); 
for (int i=0; i<n; i++) printf("%d ", a[i]);
printf("\n- Day con don dieu tang dai nhat: "); 
for (int i=0; i<lMax; i++) printf("%d ", kq[i]);
printf("\n  (gom %d phan tu)", lMax);
getch(); 
}
