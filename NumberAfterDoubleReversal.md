A Number After a Double Reversal
Solved
Easy
Topics
Companies
Hint
Reversing an integer means to reverse all its digits.

For example, reversing 2021 gives 1202. Reversing 12300 gives 321 as the leading zeros are not retained.
Given an integer num, reverse num to get reversed1, then reverse reversed1 to get reversed2. Return true if reversed2 equals num. Otherwise return false.

```csharp
public class Solution
{
    public bool IsSameAfterReversals(int num)
    {
        int rev = int.Parse(new string(num.ToString().Reverse().ToArray()));
        int numrev = int.Parse(new string(rev.ToString().Reverse().ToArray()));
        if(num == numrev)
        {
            return true;
        }
        else
        {
            return false;
        }
    }
}
