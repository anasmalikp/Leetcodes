Truncate Sentence

A sentence is a list of words that are separated by a single space with no leading or trailing spaces. Each of the words consists of only uppercase and lowercase English letters (no punctuation).

For example, "Hello World", "HELLO", and "hello world hello world" are all sentences.
You are given a sentence s​​​​​​ and an integer k​​​​​​. You want to truncate s​​​​​​ such that it contains only the first k​​​​​​ words. Return s​​​​​​ after truncating it.

```csharp
public class Solution
{
    public string TruncateSentence(string s, int k)
    {
        List<string> sentence = new List<string>(s.Split(' '));
        List<string> result = new List<string>();
        if(sentence.Count > k  )
        {
        for(int i = 0; i < k; i++)
        {
            result.Add(sentence[i]);
        }

        } else
        {
            result = sentence;
        }
        string resultstr = string.Join(' ', result);
        return resultstr;
    }
}
