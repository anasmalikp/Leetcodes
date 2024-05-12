Merge Strings Alternately

You are given two strings word1 and word2. Merge the strings by adding letters in alternating order, starting with word1.
If a string is longer than the other, append the additional letters onto the end of the merged string.

Return the merged string.

```csharp
public class Solution
{
    public string MergeAlternately(string word1, string word2)
    {
        List<char> chars = new List<char>();
        List<char> word1list = new List<char>(word1);
        List<char> word2list = new List<char>(word2);
        if(word1list.Count > word2list.Count)
        {
            for(int i = 0; i < word1list.Count; i++)
            {
                chars.Add(word1list[i]);
                if (word2list.Count - 1 >= i)
                {
                    chars.Add(word2list[i]);
                    
                }
            }
        } else if(word2list.Count > word1list.Count)
        {
            for (int i = 0; i < word2list.Count; i++)
            {
                if (word1list.Count - 1 >= i)
                {
                    chars.Add(word1list[i]);

                }
                chars.Add(word2list[i]);
            }
        } else
        {
            for (int i = 0; i < word1list.Count; i++)
            {
                chars.Add(word1list[i]);
                chars.Add(word2list[i]);
            }
        }
        return new string(chars.ToArray());
    }
}
