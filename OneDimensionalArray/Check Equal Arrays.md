[Check Equal Arrays](https://www.geeksforgeeks.org/problems/check-if-two-arrays-are-equal-or-not3847/1?itm_source=geeksforgeeks&itm_medium=Article&itm_campaign=bottom_sticky_on_Article)

```
class Solution 
{
    public static boolean checkEqual(int[] a, int[] b) 
    {
        HashMap<Integer, Integer> map = new HashMap<>();
        
        for(int i = 0 ; i < a.length ; i++)
        {
            if(map.containsKey(a[i]))
            {
                int count = map.get(a[i]);
                map.put(a[i], count + 1);
            }
            else
            {
                map.put(a[i], 1);
            }
        }
        
        for(int i = 0 ; i < b.length ; i++)
        {
            if(map.containsKey(b[i]))
            {
                int count = map.get(b[i]);
                if(count == 0)
                {
                    return false;
                }
                map.put(b[i], count - 1);
            }
            else
            {
                return false;
            }
        }
        
        return true;
    }
}
```

```
Strengths of this algorithm:

⭐️ Avoids multiple unnecessary checks.
⭐️ Using a single HashMap.
⭐️ Modifying the existing HashMap to solve the problem efficiently.
```

```
Pattern of the above question:

Count of a key
      ↓
Incrementing and decrementing counts

```      
