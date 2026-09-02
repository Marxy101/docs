---
Title: 'Round'
Description: 'Rounds a number to the nearest integer or to a specified number of decimal places.'
Subjects:
  - 'Computer Science'
Tags:
  - 'Methods'
  - 'Numbers'
CatalogContent:
  - 'learn-c-sharp'
  - 'paths/computer-science'
---

The **`.Round()`** method, part of the `Math` class in C#, rounds a numeric value to the nearest integer or to a specified number of decimal places.

By default, `.Round()` uses **banker's rounding** (round-half-to-even), meaning a value exactly halfway between two numbers rounds to the nearest even number rather than always rounding up.

## Syntax

```pseudo
Math.Round(value);
Math.Round(value, digits);
```

- `value`: The `double` or `decimal` number to round. Required.
- `digits`: The number of decimal places to round to. Optional; defaults to `0` if omitted.

`.Round()` returns the rounded value as the same type (`double` or `decimal`) that was passed in.

## Example

The following example rounds a `double` to the nearest whole number and to two decimal places:

``` cs
double num1 = 4.7;
double num2 = 2.5;
double num3 = 3.14159;

Console.WriteLine(Math.Round(num1));
Console.WriteLine(Math.Round(num2));
Console.WriteLine(Math.Round(num3, 2));
```

This produces the following output:

``` shell
5
2
3.14
```

Note that `num2` (`2.5`) rounds down to `2` instead of up to `3` because of banker's rounding: `2` is the nearest even number.

## Codebyte Example

The following Codebyte example demonstrates rounding a value to different numbers of decimal places:

```codebyte/csharp
using System;

public class RoundExample
{
  public static void Main()
  {
    double price = 19.98765;

    Console.WriteLine(Math.Round(price));
    Console.WriteLine(Math.Round(price, 1));
    Console.WriteLine(Math.Round(price, 3));
  }
}
```

