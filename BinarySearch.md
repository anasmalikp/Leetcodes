Binary Search

Given an array of integers nums which is sorted in ascending order, and an integer target, write a function to search target in nums. If target exists, then return its index. Otherwise, return -1.

```csharp
public class Solution
{
    public int Search(int[] nums, int target)
    {
        return new List<int>(nums).IndexOf(target);
    }
}
