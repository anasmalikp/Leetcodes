2544. Alternating Digit Sum

You are given a positive integer n. Each digit of n has a sign according to the following rules:

The most significant digit is assigned a positive sign.
Each other digit has an opposite sign to its adjacent digits.
Return the sum of all digits with their corresponding sign.

```csharp
public class Solution
{
    public int AlternateDigitSum(int n)
    {
        List<int> list = new List<int>(n.ToString().Select(x => int.Parse(x.ToString()))).ToList();
        int sum = 0;
        for(int i = 0; i < list.Count; i++)
        {
            if(i % 2 == 0)
            {
                sum += list[i];
            }
            else
            {
                sum -= list[i];
            }
        }

        return sum;
        
    }
}
