[Right Rotation By One](https://www.geeksforgeeks.org/problems/cyclically-rotate-an-array-by-one2614/1?itm_source=geeksforgeeks&itm_medium=Article&itm_campaign=bottom_sticky_on_Article)

```
class Solution 
{
    public void rotate(int[] arr) 
    {
        int temp = arr[arr.length - 1];
        for(int i = arr.length - 2 ; i >= 0 ; i--)
        {
            arr[i + 1] = arr[i];
        }
        arr[0] = temp;
    }
}
```

