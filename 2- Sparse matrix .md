# Sparse matrix
``` C
// DSA=PROBLEM 2
// Sparse Matrix
//AKHILA SUNESH

#include <stdio.h>

void main() {

        
        
     int r, c, count = 0, i, j;
    
    // Input the number of rows
    printf("Enter the number of rows: ");
    scanf("%d", &r);
    
    // Input the number of columns
    printf("Enter the number of columns: ");
    scanf("%d", &c);
    
    int a[r][c];
    
    // Input the elements of the matrix
    for (i = 0; i < r; i++) {
        for (j = 0; j < c; j++) {
            printf("Enter the element: ");
            scanf("%d", &a[i][j]);
            if (a[i][j] == 0) {
                count++;
            }
        }
    }
    
    // Check if the matrix is sparse
    if (count < ((r * c) / 2)) {
        printf("THIS IS NOT A SPARSE MATRIX\n");
    } else {
        int b[((r * c) - count) + 1][3];
        int c1 = 3, r1 = (((r * c) - count) + 1), s = 1;
        
        // First row of sparse matrix representation
        b[0][0] = r;
        b[0][1] = c;
        b[0][2] = ((r * c) - count);
        
        // Fill the sparse matrix representation
        for (i = 0; i < r; i++) {
            for (j = 0; j < c; j++) {
                if (a[i][j] != 0) {
                    b[s][0] = i;
                    b[s][1] = j;
                    b[s][2] = a[i][j];
                    s++;
                }
            }
        }
        
        // Print the sparse matrix representation
        for (i = 0; i < r1; i++) {
            for (j = 0; j < 3; j++) {
                printf("%d\t", b[i][j]);
            }
            printf("\n");
        }
    }

  }
```
```
/tmp/QmjgAg206V.o
Enter the number of rows: 4
Enter the number of columns: 5
Enter the element: 0
Enter the element: 0
Enter the element: 1
Enter the element: 0
Enter the element: 3
Enter the element: 0
Enter the element: 0
Enter the element: 0
Enter the element: 4
Enter the element: 0
Enter the element: 0
Enter the element: 7
Enter the element: 0
Enter the element: 0
Enter the element: 0
Enter the element: 0
Enter the element: 0
Enter the element: 6
Enter the element: 0
Enter the element: 0
4	5	5	
0	2	1	
0	4	3	
1	3	4	
2	1	7	
3	2	6	


=== Code Exited With Errors ===
```
