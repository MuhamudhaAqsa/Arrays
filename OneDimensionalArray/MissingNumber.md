[Missing in Array](https://www.geeksforgeeks.org/problems/missing-number-in-array1416/1)

```
Sum of numbers from 1 to n formula:

sum = n(n + 1) / 2;
```

```
class Solution 
{
    int missingNum(int arr[]) 
    {
        long n = arr.length + 1;
        
        long num = (n * (n + 1)) / 2;
        
        for(int i = 0 ; i < arr.length ; i++)
        {
            num = num - arr[i];
        }
        
        int ans = (int) num;
        
        return ans;
    }
}
```
