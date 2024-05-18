Faulty Keyboard

Your laptop keyboard is faulty, and whenever you type a character 'i' on it, it reverses the string that you have written. Typing other characters works as expected.

You are given a 0-indexed string s, and you type each character of s using your faulty keyboard.

Return the final string that will be present on your laptop screen.

```csharp
public class Solution
{
    public string FinalString(string s)
    {
        List<char> schars = new List<char>(s);
        List<char> result = new List<char>();
        foreach (char c in schars)
        {
            if(c == 'i')
            {
                result.Reverse();
            } else
            {
                result.Add(c);
            }

        }
        char[] arr = result.ToArray();
        return string.Join("", arr);
    }
}
