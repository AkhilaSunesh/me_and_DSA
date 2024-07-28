# PROBLEM -1
## Stack Operations
Perform basic stack operations like push, pop, display and exit
``` C
// DSA=PROBLEM 1
// Stack operations
//AKHILA SUNESH

#include <stdlib.h>
# include <stdio.h>
void main()
{   int b,c,top,i,n,y;
    top=-1;
    y=1;
    printf("Enter the size of the array");
    scanf ("%d",&n);
    int a[n];
    while (y==1) {
        printf("STACK OPERATIONS \n");
        printf("1. Push \n");
        printf("2. Pop \n");
        printf("3. Display \n");
        printf("4. Exit \n");
        printf("Enter the value ");
        scanf ("%d",&c);
        switch (c)
        {
            case 1:
            if (top>=(n-1)){
                printf("STACK OVERFLOW \n");
                break;
            }
            else
            {
                printf("OPTION 1 : PUSH \n");
                printf("Enter the element to be added");
                scanf("%d",&b);
                top=top+1;
                a[top]=b;
                printf ("top =%d \n",top);
                break;
            }
            case 2:
            if (top<=-1){
                printf("STACK UNDERFLOW \n");
                break;
            }
            else
            {
                printf("OPTION 2 : POP \n");
                top=top-1;
                printf("top =%d \n", top);
                break;
            }
            case 3:
            {
                printf("OPTION 3 : DISPLAY \n");
                for (i=top; i>=0;i--)
                {
                    printf("%d \n",a[i]);
                }
                printf("top =%d \n", top);
                break;
            }
            case 4:
            {
                printf("OPTION 4 : EXIT \n");
                exit(1);
            }
            default: 
            {
                printf("INVALID OPTION \n");
                break;
            }
            
            
        }
    }
    
}
```
