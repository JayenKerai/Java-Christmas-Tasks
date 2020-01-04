# Java-Christmas-Tasks
> Tasks completed for Manish Gadhvi (Sparta Global) over the 2019-2020 Christmas holiday period

## 2020-01-06

## Testing method
Executed all tests and documented outputs under "Testing".
For each issue, read through code to find what needs to be corrected.
Retest after every change and document any differences to outputs.
Document individual changes made (what and where), along with what issue it solves under "Changes".

## Testing

1 `divisibleBy(4,2)` should return true
- Output before changes: false
- Output after change 1: true
- Problems discovered: 
  1. Does not return true

2 `divisibleBy(3,2)` should return false
- Output before changes: false
- Problems discovered: ~

3 `fizzBuzzGenerator(1,15)` should return ["1", "2", "Fizz", "4", "Buzz", "Fizz", "7", "8", "Fizz", "buzz", "11", "Fizz", "13", "14", "FizzBuzz"]
- Output before changes: [1, FizzBuzz, 3, 4, FizzBuzz, 6, FizzBuzz, FizzBuzz, 9, 10, FizzBuzz, FizzBuzz, 13, FizzBuzz]
- Output after change 1: [1, 2, FizzBuzz, 4, FizzBuzz, FizzBuzz, 7, 8, FizzBuzz, FizzBuzz, 11, FizzBuzz, 13, 14]
- Output after change 2: [1, 2, FizzBuzz, 4, FizzBuzz, FizzBuzz, 7, 8, FizzBuzz, FizzBuzz, 11, FizzBuzz, 13, 14, FizzBuzz]
- Output after change 3: [1, 2, Fizz, 4, Buz, Fizz, 7, 8, Fizz, Buz, 11, Fizz, 13, 14, FizzBuzz]
- Output after change 5: [1, 2, Fizz, 4, Buzz, Fizz, 7, 8, Fizz, Buzz, 11, Fizz, 13, 14, FizzBuzz]
- Problems discovered:
  1. Only 14 returned values (should be 15)
  2. Incorrect triggering of FizzBuzz word
  3. Buzz word not being triggered
  4. Test case contains incorrect spelling/grammar: "buzz" at 12 should be "Buzz" 
  5. Incorrect Spelling: "Buz" should be "Buzz"

## Changes
1
- Changed: At FizzBuzzGenerator > divisibleBy()
  `return numerator % Denominator == 2;` to `return numerator % Denominator == 0;`
- Solves: 1.1, 3.2

2
- Changed: At FizzBuzzGenerator > FizzBuzz()
  `for (int i = startNumber; i <endNumber ; i++) {` to `for (int i = startNumber; i <= endNumber ; i++) {`
- Solves: 3.1

3
- Changed: At FizzBuzzGenerator > FizzBuzz()
  `if(divisibleBy(i, 3) || divisibleBy(i, 5)) fizzBuzzList.add("FizzBuzz");` to `if(divisibleBy(i, 3) && divisibleBy(i, 5)) fizzBuzzList.add("FizzBuzz");`
- Solves: 3.3

4
- Changed: At FizzBuzzGenerator > FizzBuzz()
  `else if (divisibleBy(i, 5)) fizzBuzzList.add("Buz");` to `else if (divisibleBy(i, 5)) fizzBuzzList.add("Buzz");`
- Solves: 3.5
