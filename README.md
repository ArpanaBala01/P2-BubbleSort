# Bubble Sort
<h3>Write a function to sort an array of n elements.<br></h3>

<strong><i>Bubble Sort</i></strong>:<p style="font-size:79px"> Bubble sort, sometimes referred to as sinking sort, is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements and swaps them if they are in the wrong order. The pass through the list is repeated until the list is sorted. The time complexity is O(n²) in the average case.  <br>
</p>

Input:

```c#
arr = [2,1,6,4,9,7,5]
```

Output:

```c#
arr = [1,2,4,5,6,7,9]
```

Time Complexity:

```python
O(n²)
```

public class bubbleSort {
    public static void bubbleSorting(int[] arr){
        int n = arr.length;
        int temp = 0;

        /* Loop to access each element of array*/
        for(int i = 0; i < n; i++){

            // Loop to compare the element of array
            for(int j=1; j < (n-i); j++){
                // compare two adjacent elements
                if(arr[j-1] > arr[j]) {

                    // Swapping the elements if elements are not in intended order
                    temp = arr[j-1];
                    arr[j-1] = arr[j];
                    arr[j] = temp;
                }
            }
            }
    }

    public static void main(String[] args){
        int arr[] = {2,1,6,4,9,7,5};

        // printing the array elements before sorting
        for(int i=0; i < arr.length; i++)
            System.out.print(arr[i] + " ");

        System.out.println();

        // Sorting array elements using Bubble Sorting
        bubbleSorting(arr);

        // Printing array elements after sorting
        for(int i=0; i<arr.length; i++)
            System.out.print(arr[i] + " ");
    }
}

