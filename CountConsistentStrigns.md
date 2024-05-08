Count the Number of Consistent Strings

You are given a string allowed consisting of distinct characters and an array of strings words.
A string is consistent if all characters in the string appear in the string allowed.

```csharp
public class Solution
{
    public int CountConsistentStrings(string allowed, string[] words)
    {
        HashSet<char> allowedList = new HashSet<char>(allowed);
        int final = 0;
        foreach (string word in words)
        {
            bool isContain = true;
            foreach (char c in word)
            {
                if(!allowedList.Contains(c))
                {
                    isContain = false;
                    break;
                }
            }
            if (isContain)
            {
                final++;
            }
        }
        return final;
    }
}
