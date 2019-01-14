# Transportation on Vacation
[Link to Kata](https://www.codewars.com/kata/568d0dd208ee69389d000016)

## Instructions
After a hard quarter in the office you decide to get some rest on a vacation. So you will book a flight for you and your girlfriend and try to leave all the mess behind you.

You will need a rental car in order for you to get around in your vacation. The manager of the car rental makes you some good offers.

Every day you rent the car costs $40. If you rent the car for 7 or more days, you get $50 off your total. Alternatively, if you rent the car for 3 or more days, you get $20 off your total.

Write a code that gives out the total amount for different days(d)

## Solution
[Run this on repl.it!](https://repl.it/@cnemeth/Transportation-on-Vacation)
```
function rentalCarCost(d){
  return d * 40 - (d >= 7 ? 50 : (d >= 3 ? 20 : 0));
}
```

This challenge allowed me to practice my ES6 ternary statements and order of operations. The trickiest part was having the running correct order of operations. In this case we want to multiply the rate and the amount of days and then subtract the deal that applies to the amount of days the car was driven. By running the smallest deal first in the innermost parentheses `(d >= 3 ? 20 : 0)`, we can check if the car was driven in 3 or less days. If the amount of days is equal to or greater than 7, the innermost statement will be false, thus giving you the result with the best deal at $50 off per day.

## Resources
[JavaScript Ternary](https://scotch.io/tutorials/understand-the-javascript-ternary-operator-like-abc)
[PEMDAS](https://www.chilimath.com/lessons/introductory-algebra/order-of-operations/)