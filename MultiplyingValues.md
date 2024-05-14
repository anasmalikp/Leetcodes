Keep Multiplying Found Values by Two

You are given an array of integers nums. You are also given an integer original which is the first number that needs to be searched for in nums.

You then do the following steps:

If original is found in nums, multiply it by two (i.e., set original = 2 * original).
Otherwise, stop the process.
Repeat this process with the new number as long as you keep finding the number.
Return the final value of original.

```csharp
public class Solution
{
    public int FindFinalValue(int[] nums, int original)
    {
        int targ = original;
        List<int> ints = new List<int>(nums);

        for(int i = 0;i < nums.Length; i++)
        {
            if(ints.Contains(targ)) {
                targ = targ * 2;
            } else
            {
                break;
            }
        }
        return targ;
    }
}
