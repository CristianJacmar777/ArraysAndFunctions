# ArraysAndFunctions
C language pass an array with 6 integers to a function
/*Within this program, we will pass an array with 6 integers to a function, have the function swap the first and last integer,
the second and the second to last integer, the third and the third to last integer.

The function is called reverseArray and doesn't return anything (void). It should take one parameter, representing the array of integers.

The main function first reads 6 integers from the input, and assigns them to the array. The main function then calls reverseArray, passing the array as an argument.

The main function then prints the reversed array.

*/


#include <stdio.h>
void reverseArray(int *);
int main() {

    int arr[6] = {0, 0, 0, 0, 0, 0};
    int j =0;
    for(j=0;j<6;j++){

        scanf("%d", &arr[j]);
    }
    reverseArray(arr);
    j=0;
    for(j=0;j<6;j++){

        printf("%d ", arr[j]);
    }
    return 0;
}
void reverseArray(int * ptr){
    int i = 0;
    int temp[6] = {0, 0, 0, 0, 0, 0};
    for(i=0;i<6;i++){

      *(temp + 5 -i) = *(ptr +i);
    }
    i =0;
    for(i=0;i<6;i++){

        *(ptr +i) = *(temp +i);
    }
}
//Write your function here
