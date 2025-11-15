[Third largest element](https://www.geeksforgeeks.org/problems/third-largest-element/1)

```
class Solution 
{
    int thirdLargest(int arr[]) 
    {
        if(arr.length < 3)
        {
            return -1;
        }
        int largest = 0;
        int secondLargest = 0;
        int thirdLargest = 0;
        
        for(int i = 0 ; i < arr.length ; i++)
        {
            if(arr[i] > largest)
            {
                thirdLargest = secondLargest;
                secondLargest = largest;
                largest = arr[i];
            }
            else if(arr[i] > secondLargest)
            {
                thirdLargest = secondLargest;
                secondLargest = arr[i];
            }
            else if(arr[i] > thirdLargest)
            {
                thirdLargest = arr[i];
            }
        }
        
        return thirdLargest;
    }
}
```
