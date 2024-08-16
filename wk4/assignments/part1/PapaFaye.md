Hey Papa. General comments about the project. (1)

- rework complete

---

| Part 1 - Function Practice                      |   Complete?    |
| ----------------------------------------------- | :------------: |
| Runs in browser without console errors          |      yes       |
| Returns the string 'hello'                      |      yes       |
| Returns the string 'Hello, Your Name!'          |      yes       |
| Returns the sum of two numbers                  |      yes       |
| Multiplies three numbers and returns the result |      yes       |
| Should check if number is positive              |      yes       |
| Returns the last item in an Array               |      yes       |
| Finds an item in an Array                       | no, see note 1 |
| STRETCH: Checks the first letter of a string    |      yes       |
| STRETCH: Sum all numbers of an array            | no, see note 2 |
| STRETCH: All postive numbers                    | no, see note 3 |

### Notes:

1. AssertionError: find() does not return anything: expected undefined to exist

2. AssertionError [ERR_ASSERTION]: 253 == 15

3. TypeError: allPositive.push is not a function

- Q7: we want to loop to continue with checking other values until the condition is true, or nothing is found (false)
  the way it is written below will allow the loop to continue and ONLY if there is a match will it return true ending the loop. If no match is found, return false.

- note this one and we can discuss.

```js
function find(value, array) {
  for (let i = 0; i < array.length; i++) {
    if (array[i] === value) {
      return true;
    }
  }
  return false;
}
console.log('The value is found', find(array, 'pen')); //the function has to be called with an actual value, ie, 'pen'.
```

- Stretch: Q8. you were close on this one. no need to find the index of a single letter, ie, letter[i] is unecessary. just use the letter which is 'F'.

```js
function isFirstLetter(letter, string) {
  for (let i = 0; i < string.length; i++) {
    // letter to check is 'F'
    // the string that was provided was 'Fargo'
    // the string[0] will be 'F'
    // if ('F' === 'F')
    if (letter === string[0]) {
      return true;
    }
  }
  return false;
}
console.log('Is the letter the first letter in the string?', isFirstLetter('F', 'Fargo'));
```

### Feedback

Getting better!

- I like how you test all of the functions.
- we can discuss the other stretch goals as well
