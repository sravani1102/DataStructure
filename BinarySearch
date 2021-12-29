#include<stdio.h>
int BinarySearch(int a[],int n,int x)
{
    int mid,low=0,high=n-1,flag=0;
    while(low<=high)
    {
        mid=(low+high)/2;
        if(a[mid]==x)
        {
            flag=1;
            break;
        }
        else
        {
            if(a[mid]>x)
            {
                high=mid-1;
            }
            else
            {
                low=mid+1;
            }
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
    if(BinarySearch(a,n,x))
    {
        printf("%d element is found\n",x);
    }
    else
    {
        printf("%d element is not found\n",x);
    }
}
