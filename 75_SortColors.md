Sort Colors

Given an array nums with n objects colored red, white, or blue, sort them in-place so that objects of the same color are adjacent, with the colors in the order red, white, and blue.

We will use the integers 0, 1, and 2 to represent the color red, white, and blue, respectively.

You must solve this problem without using the library's sort function.

```csharp
public class Solution {
    public void SortColors(int[] nums) {
        for(int i = 0; i<nums.Length; i++) {
            for(int j = i + 1; j < nums.Length ; j++) {
                if(nums[i] > nums[j]) {
                    int x = nums[i];
                    nums[i] = nums[j];
                    nums[j] = x;
                }
            }
        }
    }
}
