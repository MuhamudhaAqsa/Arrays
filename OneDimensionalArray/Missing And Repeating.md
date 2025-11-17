[Missing And Repeating](https://www.geeksforgeeks.org/problems/find-missing-and-repeating2512/1)

```
class Solution 
{
    ArrayList<Integer> findTwoElement(int arr[]) 
    {
        long n = arr.length;
        
        long sum = (n * (n + 1)) / 2;
        
        long sqSum = (n * (n + 1) * ((2 * n) + 1)) / 6;
        
        long arrSum = 0;
        long arrSqSum = 0;
        for(int i = 0 ; i < arr.length ; i++)
        {
            arrSum = arrSum + arr[i];
            long num = (long) arr[i];
            arrSqSum = arrSqSum + (num * arr[i]);
        }
        
        long diff = arrSum - sum;
        
        long sqDiff = arrSqSum - sqSum;
        
        long xPlusY = sqDiff / diff;
        
        long x = (xPlusY + diff) / 2;
        
        long y = xPlusY - x;
        
        ArrayList<Integer> list = new ArrayList<>();
        
        list.add((int) x);
        
        list.add((int) y);
        
        return list;
        
    }
}
```
