[Sort 0s, 1s and 2s](https://www.geeksforgeeks.org/problems/sort-an-array-of-0s-1s-and-2s4231/1?itm_source=geeksforgeeks&itm_medium=Article&itm_campaign=bottom_sticky_on_Article)

```
class Solution 
{
    public void sort012(int[] arr) 
    {
       int mid = 0;
       int low = 0;
       int high = arr.length - 1;
       
       while(mid <= high)
       {
           if(arr[mid] == 0)
           {
            int temp = arr[low];
            arr[low] = arr[mid];
            arr[mid] = temp;
            mid = mid + 1;
            low = low + 1;
           }
           else if(arr[mid] == 1)
           {
               mid = mid + 1;
           }
           else
           {
               int temp = arr[high];
               arr[high] = arr[mid];
               arr[mid] = temp;
               high = high - 1;
           }
       }
    }
}
```
