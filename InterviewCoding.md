# This is some interview notes

* [sqrt without using sqrt function](#sqrt-without-using-sqrt-function)

## sqrt without using sqrt function
** Method1: use Newton's method **
refer [Newton's method](https://en.wikipedia.org/wiki/Newton%27s_method)
```csharp
private static double sqrt(int num)
{
        double x1 = (num * 1.0) / 2;
        double x2 = (x1 + (num / x1)) / 2;
        while (Math.Abs(x1-x2)>=0.0000001)
        {
                x1 = x2;
                x2 = (x1 + (num / x1)) / 2;
        }
        return x2;
}
```

** Method2 **
```
1 = 1  square of 1
1 + 3 = 4 square of 2,,adding two times
1 + 3 + 5 = 9 square of 3 adding three times
```
The code is:
```csharp
private static int sqrt2(int num)
{
    int x = 1;
    int nextPlus = 1;
    int result = 0;
    while (x <= num)
    {
        result += 1;
        nextPlus += 2;
        x = x + nextPlus;
    }
    return result;
}
```
