# Keep Hydrated!
[Link to Kata](https://www.codewars.com/kata/keep-hydrated-1)

## Instructions
Nathan loves cycling.

Because Nathan knows it is important to stay hydrated, he drinks 0.5 litres of water per hour of cycling.

You get given the time in hours and you need to return the number of litres Nathan will drink, rounded to the smallest value.

For example:

time = 3 ----> litres = 1

time = 6.7---> litres = 3

time = 11.8--> litres = 5

## Solution
[Run this on repl.it!](https://repl.it/@cnemeth/keep-hydrated)
```
function litres(time) {
  return Math.floor(time * 0.5);
}
```

In order to complete this challenge, I knew I would need to multiply the given time value by 0.5. Once I had the total for the litres, I would need to find a way to round that number down to the nearest whole integer. After google searching "JavaScript round down integer," I discovered you can use `Math.floor()` to round down, while `Math.round()` will round up or down to the nearest integer.

## Resources
- [Rounding and Truncating Numbers in JavaScript](https://pawelgrzybek.com/rounding-and-truncating-numbers-in-javascript/)