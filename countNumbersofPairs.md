Given an integer array nums and an integer k, 
return the number of pairs (i, j) where i < j such that |nums[i] - nums[j]| == k.
(Beats 91.76% of users in runtime)
```csharp
public class Solution
{
    public int CountKDifference(int[] nums, int k)
    {
        int count = 0;

        Array.Sort(nums);

        for(int i = 0; i < nums.Length; i++)
        {
            for(int j = 0; j < nums.Length; j++)
            {
                if (nums[j] - nums[i] == k)
                {
                    count++;
                }
            }
        }
        return count;
    }
}
