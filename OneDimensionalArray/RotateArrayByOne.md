Left Rotation:


```
package RotateArrayByOne;

import java.util.Scanner;

public class Optimal
{
    public static void main(String[] args)
    {
        Scanner input = new Scanner(System.in);
        int size = input.nextInt();
        int[] arr = new int[size];
        for(int i = 0 ; i < arr.length ; i++)
        {
            arr[i] = input.nextInt();
        }
        rotate(arr);
    }

    static void rotate(int[] arr)
    {
        int temp = arr[0];
        for(int i = 1 ; i < arr.length ; i++)
        {
            arr[i - 1] = arr[i];
        }
        arr[arr.length - 1] = temp;
    }
}

```
