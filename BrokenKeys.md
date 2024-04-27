Maximum Number of Words You Can Type

There is a malfunctioning keyboard where some letter keys do not work. All other keys on the keyboard work properly.

Given a string text of words separated by a single space 
(no leading or trailing spaces) and a string brokenLetters of all distinct letter keys that are broken, 
return the number of words in text you can fully type using this keyboard.

```csharp
public class Solution
{
    public int CanBeTypedWords(string text, string brokenLetters)//ab
    {
        List<string> words = new List<string>(text.Split(" "));
        List<char> letters = brokenLetters.ToList();
        int count = 0;
        foreach (string word in words)
        {
            if (letters.Any(x => word.Contains(x)))
            {
                continue;
            }
            else
            {
                count++;
            }
        }
        return count;
    }
}
