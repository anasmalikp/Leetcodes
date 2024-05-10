Calculate Money in Leetcode Bank

Hercy wants to save money for his first car. He puts money in the Leetcode bank every day.

He starts by putting in $1 on Monday, the first day. Every day from Tuesday to Sunday, he will put in $1 more than the day before. 
On every subsequent Monday, he will put in $1 more than the previous Monday.
Given n, return the total amount of money he will have in the Leetcode bank at the end of the nth day.

(Beats 91.01% of users in runtime speed)

```csharp
public class Solution
{
    public int TotalMoney(int n)
    {
        int count = 0;
        int total = 0;
        for(int i = 1; i < n; i++)
        {
            for(int j = i; j <= 6 + i ; j++)
            {
                if(count == n)
                {
                    break;
                }
                total += j;
                count++;
            }
        }
        return total;
    }
}
