# Count of positives / sum of negatives
[Link to Kata](https://www.codewars.com/kata/count-of-positives-slash-sum-of-negatives)

## Instructions
Given an array of integers.

Return an array, where the first element is the count of positives numbers and the second element is sum of negative numbers.

If the input array is empty or null, return an empty array.

## Solution
**The Code:**
```
function countPositivesSumNegatives(input) {
    let positiveNums = 0;
    let negativeNums = 0;
    if (input === null || input.length === 0) {
      return [];
    } else {
      input.forEach((num) => num > 0 ? positiveNums++ : negativeNums += num);
    }
    return [positiveNums , negativeNums];
}
```
[Run it on repl.it!](https://repl.it/@cnemeth/count-of-positives-sum-of-negatives)

## Summary
For this challenge I needed to set two variables, positiveNums and negativeNums, to 0 so that we can check the numbers in the array and store them. The challenge asks to return an empty array if the input is null or empty, so in the function, I decided to start my if statement that checks that first.
```if (input === null || input.length === 0) {
      return [];
    }
```
If the input is neither empty, nor null, then I needed a way to check each element in the array and check if the numbers were greater than zero and run a conditional expression to count the positive numbers, and add the negative numbers. Since I was not worried about performance issues, I decided to reach for the handy forEach() method to achieve this.
```
else {
      input.forEach((num) => num > 0 ? positiveNums++ : negativeNums += num);
    }
```
As I iterate over each number, if the number is greater than 0, I can use the increment operator on the positive numbers, and if the number is negative, I can use the plus/equals operator to add all of the negative numbers. Finally, I need to return both positiveNums, and negativeNums into an array as my desired output.

## Resources
- [MDN: if...else](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else)
- [ES6 forEach() loops with vanilla JavaScript](https://gomakethings.com/es6-foreach-loops-with-vanilla-javascript/)
- [Operators](https://javascript.info/operators)
