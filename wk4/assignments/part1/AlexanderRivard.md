Hey Alex. General comments about the project. (5)

---

| Part 1 - Function Practice                      | Complete? |
| ----------------------------------------------- | :-------: |
| Runs in browser without console errors          |    yes    |
| Returns the string 'hello'                      |    yes    |
| Returns the string 'Hello, Your Name!'          |    yes    |
| Returns the sum of two numbers                  |    yes    |
| Multiplies three numbers and returns the result |    yes    |
| Should check if number is positive              |    yes    |
| Returns the last item in an Array               |    yes    |
| Finds an item in an Array                       |    yes    |
| STRETCH: Checks the first letter of a string    |    yes    |
| STRETCH: Sum all numbers of an array            |    yes    |
| STRETCH: All postive numbers                    |    yes    |

### Notes:

- Q6: another way to handle question 6. checking for null/undefined or the the length of an array

```js
function getLast(array) {
  if (!array || array.length === 0) {
    //checks for nothing is sent OR if the array is empty
    return undefined;
  }
  return array[array.length - 1];
}
```

-Q7 good work, get into the habit to declare the iterator with 'let' or 'const': for (let i of array) {...}

Excellent work!!
