#include <stdio.h>
void QuickSort(int *arr,int left,int right)
{
int j = right;
int i = left;
int key = *(arr+i);
if(left >= right)
	return;
while(i<j)
{
while((i<j)&& (key>=arr[j]))
	j--;
*(arr+i)=*(arr+j);
while((i<j)&&(key<=arr[i]))
	i++;
*(arr+j)=*(arr+i);
}
*(arr+i) =key;
QuickSort(arr,left,i-1);
QuickSort(arr,i+1,right);
}
