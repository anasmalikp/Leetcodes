Richest Customer Wealth

You are given an m x n integer grid accounts where accounts[i][j] is the amount of money the i​​​​​​​​​​​th​​​​ customer has in the j​​​​​​​​​​​th​​​​ bank. Return the wealth that the richest customer has.

A customer's wealth is the amount of money they have in all their bank accounts. The richest customer is the customer that has the maximum wealth.

(Beats 95.87% of users in Runtime (59ms))
```chsarp
public class Solution
{
    public int MaximumWealth(int[][] accounts)
    {
        int res = 0;
        List<int> sums = new List<int>();
        foreach (var arr in accounts)
        {
            for(int i = 0; i< arr.Length; i++)
            {
                res += arr[i];
            }
            sums.Add(res);
            res = 0;
        }

        var max = sums.Max();
        return max;
    }
}
