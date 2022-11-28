# 23.-odev

//ekrana y�ld�zlarla x harfi yazan kod

#include<stdio.h>

int yildiz2(int n,int i,int j)
{
	if(j==n+1)
	return 1;
	
	if((i+j)==n+1 || i==j)
	{
		printf("*");
	}
	
	else
	printf(" ");
	yildiz2(n,i,j+1);
}

int yildiz(int n,int i)
{
	if(i==n+1)
	return 1;
	yildiz2(n,i,1);
	printf("\n");
	yildiz(n,i+1);
}

int main(void)
{
	printf("bir tam sayi giriniz:");
	int n;
	scanf("%d" , &n);
	yildiz(n,1);
}
