# cpractice
#include<stdio.h>
#include<stdlib.h>

int check(int num){
	int flag=0;
	for(int i=2; i<=num/2; i++){
		if(num%i==0){
			flag=1;
			break;
		}
	}
	return flag;
}

void print(int num){
	int arr[100];
	int i,j, k=0;
	for(int i=2; i<=num; i++){
		j= check(i);
		if(j==0){
			arr[k] = i;
			k++;
		}
	}
	printf("all prime numbers are:\n");
	for(int i=0; i<k; i++)
	{
		printf("%d\t",arr[i]);
	}
	printf("\n");
}

int main(){
	int num;
	printf("enter the number\n");
	scanf("%d", &num);
	print(num);
	return 0;
} 
