Find the Peaks

You are given a 0-indexed array mountain. 
Your task is to find all the peaks in the mountain array.

Return an array that consists of indices of peaks in the given array in any order.

```csharp
public class Solution
{
    public IList<int> FindPeaks(int[] mountain)
    {
        List<int> peaks = new List<int>();
        for(int i = 1; i < mountain.Length - 1; i++)
        {
            if (mountain[i] > mountain[i-1] && mountain[i] > mountain[i+1])
            {
                peaks.Add(i);
            }
        }
        return peaks;
    }
}
