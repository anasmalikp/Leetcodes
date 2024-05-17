Make Two Arrays Equal by Reversing Subarrays

You are given two integer arrays of equal length target and arr. In one step, you can select any non-empty subarray of arr and reverse it. You are allowed to make any number of steps.

Return true if you can make arr equal to target or false otherwise.

```csharp
public class Solution
{
    public bool CanBeEqual(int[] target, int[] arr)
    {
        int count = 0;
        Array.Sort(target);
        Array.Sort(arr);
        for (int i = 0; i < target.Length; i++)
        {
            if (target[i] == arr[i])
            {
                count++;
            }
        }
        if(count == target.Length)
        {
            return true;
        }
        return false;
    }
}
