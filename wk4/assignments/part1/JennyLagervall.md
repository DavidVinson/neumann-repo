Hey Jenny. General comments about the project. (3)

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
| STRETCH: Sum all numbers of an array            |      yes       |

### Notes

1. AssertionError [ERR_ASSERTION]: false == true

- Q6: another way to handle empty array check
  1. check to see if the array was sent to the function, this is checking for 'null' or 'undefined'
  2. check is see if the array length is equal to 0.
     if those two conditions are true, return undefined
     otherwise get the last item in the array

```js
function getLast(array) {
  if (!array || array.length === 0) {
    //checks for nothing is sent OR if the array is empty
    return; //will return 'undefined'
  }
  return array[array.length - 1];
}
```

-Q7: we want to loop to continue with checking other values until the condition is true, or nothing is found (false)
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
```

### Feedback

Nice work!

- remember to format the files, ie, Shift + Option + F
