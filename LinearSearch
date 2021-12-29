#include<stdio.h>
int LinearSearch(int a[],int n,int x)
{
    int i,flag=0;
    for(i=0;i<n;i++)
    {
        if(a[i]==x)
        {
            flag=1;
            break;
        }
    }
    if(flag==1)
    {
        return 1;
    }
    else
    {
        return 0;
    }
}
void main()
{
    int n,x;
    printf("Enter size of the array:\n");
    scanf("%d",&n);
    printf("Enter elements in the array\n");
    int a[n];
    for(int i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    printf("Enter an element to search:\n");
    scanf("%d",&x);
    if(LinearSearch(a,n,x))
    {
        printf("%d element is found\n",x);
    }
    else
    {
        printf("%d element is not found\n",x);
    }
}
