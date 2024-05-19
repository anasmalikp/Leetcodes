Maximum Product of Two Elements in an Array

Given the array of integers nums, you will choose two different indices i and j of that array. 
Return the maximum value of (nums[i]-1)*(nums[j]-1).

```csharp
public class Solution
{
    public int MaxProduct(int[] nums)
    {
        if(nums.Length > 1)
        {
            Array.Sort(nums, (a,b)=> b.CompareTo(a));
            int first = nums[0] - 1;
            int second = nums[1] - 1;
            return first * second;
        } else
        {
            return nums[0];
        }

    }
}
