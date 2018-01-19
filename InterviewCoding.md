# This is some interview notes

* [sqrt without using sqrt function](#sqrt-without-using-sqrt-function)

## sqrt without using sqrt function
**use Newton's method**
refer [Newton's method](https://en.wikipedia.org/wiki/Newton%27s_method)
'''csharp
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
'''
