Separate the Digits in an Array

Given an array of positive integers nums, return an array answer that consists of the digits of each integer in nums after separating them in the same order they appear in nums.

To separate the digits of an integer is to get all the digits it has in the same order.

For example, for the integer 10921, the separation of its digits is [1,0,9,2,1].

```csharp
public class Solution
{
    public int[] SeparateDigits(int[] nums)
    {
        List<int> result = new List<int>();
        for(int i = 0; i < nums.Length; i++)
        {
            if (nums[i].ToString().Length > 0 )
            {
                List<int> subnums = nums[i].ToString().Select(x=> int.Parse(x.ToString())).ToList();
                for (int j = 0; j <subnums.Count; j++ )
                {
                    result.Add(subnums[j]);
                }
            }
            else
            {
                result.Add(nums[i]);
            }
        }
        return result.ToArray();
    }
}
