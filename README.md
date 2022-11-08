#include<stdio.h>  
#define N 6                                                                           
int main ()
{
 int i,j,k;
 int a[N][N];
 for (i=0;i<N;i++){
  a[i][0]=1;
  a[i][i]=1;
 }
 
 for(i=2;i<N;i++)
 {
  for (j=1;j<i;j++)
  {
  a[i][j]=a[i-1][j]+a[i-1][j-1]; 
   
  }
 }
 for (i=0;i<N;i++){
  for(k=N-i;k>0;k--){
   printf("  ");
  }
  for (j=0;j<i+1;j++){
  printf("%4d",a[i][j]);
  }
  printf("\n");
 }
 
 return 0;
