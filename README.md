# DAA-codetantra
DAA codetantra programmes for selection sort

#include<stdio.h>
void selection(int arr[],int n)
{
	for(int i=0;i<n;i++)
	{
		for(int j=i+1;j<n;j++)
		{
			if(arr[i]>arr[j])
			{
				arr[i]=arr[i]^arr[j];
				arr[j]=arr[i]^arr[j];
				arr[i]=arr[i]^arr[j];
			}
		}
	}
}
int main()
{
	int n;
	printf("How many numbers u are going to enter?: ");
	scanf("%d",&n);
	int arr[n];
	printf("Enter %d elements: ",n);
	for(int i=0;i<n;i++)
	{
		scanf("%d",&arr[i]);
		
	}
	selection(arr,n);
	printf("Sorted elements are: ");
	for(int i=0;i<n;i++)
	printf("%d ",arr[i]);
	return 0;
}