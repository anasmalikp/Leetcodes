Number of Days Between Two Dates

Write a program to count the number of days between two dates.

The two dates are given as strings, their format is YYYY-MM-DD as shown in the examples.

```csharp
public class Solution
{
    public int DaysBetweenDates(string date1, string date2)
    {
        DateTime dateA = DateTime.Parse(date1);
        DateTime dateB = DateTime.Parse(date2);
        TimeSpan diff = dateA - dateB;
        return Math.Abs(diff.Days);
    }
}
