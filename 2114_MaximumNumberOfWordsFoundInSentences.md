Maximum Number of Words Found in Sentences

A sentence is a list of words that are separated by a single space with no leading or trailing spaces.

You are given an array of strings sentences, where each sentences[i] represents a single sentence.

Return the maximum number of words that appear in a single sentence.

```csharp
public class Solution
{
    public int MostWordsFound(string[] sentences)
    {
        int maximumWords = 0;
        for (int i = 0; i < sentences.Length; i++)
        {
            List<string> words = new List<string>(sentences[i].Split(' '));
            if(words.Count > maximumWords )
            {
                maximumWords = words.Count;
            }
        }
        return maximumWords;
    }
}
