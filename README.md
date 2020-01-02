# coding-add 1
#include<stdio.h>
int main()
{
    int n,i,temp,temp1=0,j=0;
    scanf("%d",&n);
    int a[n],b[n];
    for(i=0;i<n;i++)
    {
        scanf("%d",&temp);
        temp1=temp1+temp;
        if(temp1>0)
        {
            b[j++]=temp;
        }
    }
    b[j-1]=b[j-1]+1;
    for(i=j-1;i>=0;i--)
    {
        if(b[i]==10 && i!=0)
        {
            b[i]=0;
            b[i-1]=b[i-1]+1;
        }
    }
    for(i=0;i<j;i++)
    { 
        if(b[i]==10)
        {
            printf("1 0 ");
        }
        else
        printf("%d ",b[i]);
    }
}

