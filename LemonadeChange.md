Lemonade Change

At a lemonade stand, each lemonade costs $5. Customers are standing in a queue to buy from you and order one at a time (in the order specified by bills).
Each customer will only buy one lemonade and pay with either a $5, $10, or $20 bill.
You must provide the correct change to each customer so that the net transaction is that the customer pays $5.

```csharp
public class Solution
{
    public bool LemonadeChange(int[] bills)
    {
        int fivedollarbills = 0;
        int tendollarbills = 0;

        for (int i = 0; i < bills.Length; i++)
        {
            if (bills[i] == 5)
            {
                fivedollarbills++;
            } else if (bills[i] == 10)
            {
                tendollarbills++;
                if (fivedollarbills > 0)
                {
                    fivedollarbills--;
                }
                else
                {
                    return false;
                }
            } else
            {
                if(tendollarbills > 0 && fivedollarbills > 0)
                {
                    tendollarbills--;
                    fivedollarbills--;
                } else if (fivedollarbills >=3)
                {
                    fivedollarbills -= 3;
                } else
                {
                    return false;
                }
            }
        }
        return true;
    }
}
