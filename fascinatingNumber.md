
Check if The Number is Fascinating
Solved
Easy
Topics
Companies
Hint
You are given an integer n that consists of exactly 3 digits.

We call the number n fascinating if, after the following modification, the resulting number contains all the digits from 1 to 9 exactly once and does not contain any 0's:

Concatenate n with the numbers 2 * n and 3 * n.
Return true if n is fascinating, or false otherwise.

```csharp
public class Solution
{
    public bool IsFascinating(int n)
    {
        string concatenated = n.ToString() + (n * 2).ToString() + (n * 3).ToString();
        return checking(concatenated);
    }

    public bool checking(string concatenated)
    {
        if (concatenated.Length != 9 || concatenated.Contains('0'))
        {
            return false;
        }
        HashSet<char> newSet = new HashSet<char>();

        foreach (char c in concatenated)
        {
            if (newSet.Contains(c))
            {
                return false;
            }
            newSet.Add(c);
        }
        return true;
    }
}

class Program
{
    static void Main(string[] args)
    {
        Solution s = new Solution();
        Console.WriteLine(s.IsFascinating(100));
    }
}
