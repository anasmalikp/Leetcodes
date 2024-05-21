 Add to Array-Form of Integer

The array-form of an integer num is an array representing its digits in left to right order.

For example, for num = 1321, the array form is [1,3,2,1].
Given num, the array-form of an integer, and an integer k, return the array-form of the integer num + k.


```csharp
public class Solution
{
    public IList<int> AddToArrayForm(int[] num, int k)
    {
        BigInteger number = BigInteger.Parse(string.Concat(num.Select(x => x.ToString())));
        BigInteger result = number + k;
        List<int> list = new List<int>(result.ToString().Select(x=> int.Parse(x.ToString())));
        return list;
    }
}
