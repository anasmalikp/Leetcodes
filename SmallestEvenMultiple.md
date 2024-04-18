

2413. Smallest Even Multiple

Given a positive integer n, return the smallest positive integer that is a multiple of both 2 and n.

```csharp
public class Solution
{
    public int SmallestEvenMultiple(int n)
    {
        int result = 0;
        for(int i = n ; ; i++)
        {
            if(i % 2 == 0 && i % n == 0)
            {
                result = i;
                break;
            }
        }
        return result;
    }
}
