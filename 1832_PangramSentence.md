 Check if the Sentence Is Pangram

A pangram is a sentence where every letter of the English alphabet appears at least once.

Given a string sentence containing only lowercase English letters, return true if sentence is a pangram, or false otherwise.

(Beats 87.14% of Users)

```csharp
public class Solution
{
    public bool CheckIfPangram(string sentence)
    {
        char[] alphabets = new char[26];
        List<char> letters = sentence.ToCharArray().ToList();
        List<char> newList = new List<char>();
        int result = 0;
        for (int i = 0; i < 26; i++)
        {
            alphabets[i] = (char)('a' + i);
        }
        for (int i = 0; i < sentence.Length; i++)
        {
            if (!newList.Contains(letters[i]))
            {
                newList.Add(letters[i]);
            }
        }
        newList.Sort();
        for (int i = 0; i < newList.Count; i++)
        {
            if (newList[i] == alphabets[i])
            {
                result++;
            }
        }
        if (result == 26)
        {
            return true;
        }
        return false;
    }
}
