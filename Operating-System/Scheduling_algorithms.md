# Scheduling Algorithms

``` C
#include<stdio.h>
int main()
{
	int pro[]={1,2,3,4};
	int sum=0,n,i,s;
	n=sizeof(pro)/sizeof(pro[0]);
	int bt[]={12,5,10,20};
	int wt[4];
	wt[0]=0;
	for(i=0;i<n;i++)
	{
		wt[i]=bt[i-1]+wt[i-1];
	}
	printf("process\t\tBurst time\t\t Waiting time\n");
	for(i=0;i<n;i++)
	{
		sum+=wt[i];
		printf("%d\t\t%d\t\t%d\n",pro[i],bt[i],wt[i]);
	}
	printf("Total waiting time:%d\n",sum);
	float avg=sum/4;
	printf("Average waiting time%.2f",avg);
	return 0;
	
}
```
