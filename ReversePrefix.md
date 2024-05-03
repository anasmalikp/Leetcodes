Reverse Prefix of Word

Given a 0-indexed string word and a character ch, reverse the segment of word that starts at index 0 and ends at the index of the first occurrence of ch (inclusive). If the character ch does not exist in word, do nothing.

For example, if word = "abcdefd" and ch = "d", then you should reverse the segment that starts at 0 and ends at 3 (inclusive). The resulting string will be "dcbaefd".
Return the resulting string.

```csharp
public class Solution
{
    public string ReversePrefix(string word, char ch)
    {
        int index = word.IndexOf(ch);
        string firstPart = word.Substring(0, index + 1);
        char[] chars = firstPart.ToCharArray();
        Array.Reverse(chars);
        string secondPart = word.Substring(index + 1);
        string first = new string(chars);
        return first + secondPart;
    }
}
