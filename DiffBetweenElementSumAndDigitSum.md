You are given a positive integer array nums.

The element sum is the sum of all the elements in nums.
The digit sum is the sum of all the digits (not necessarily distinct) that appear in nums.
Return the absolute difference between the element sum and digit sum of nums.

Note that the absolute difference between two integers x and y is defined as |x - y|.

```csharp
public class Solution
{
    public int DifferenceOfSum(int[] nums)
    {
        int sum = 0;
        int sumofdigits = 0;

        for(int i = 0; i < nums.Length; i++)
        {
            if (nums[i].ToString().Length > 1)
            {
                List<int> dp = nums[i].ToString().Where(char.IsDigit).Select(x=> int.Parse(x.ToString())).ToList();
                for (int j = 0; j < dp.Count; j++)
                {
                    sumofdigits += dp[j];
                }
            } else
            {
                sumofdigits += nums[i];
            }
            sum += nums[i];
        }
        return sum - sumofdigits;
    }
}
