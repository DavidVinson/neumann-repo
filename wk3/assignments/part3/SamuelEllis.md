## Part 3 3-part-supply.js (1)

---

| Functional Requirements                                                        | Complete? |
| ------------------------------------------------------------------------------ | :-------: |
| JS: Use of let/const, no use of var                                            |    yes    |
| JS: STRETCH: Correct syntax (including let) in for...of loop                   |    yes    |
| 1. Variable of partsNeeded and value of 40 created                             |    yes    |
| 2. Array of supplyChanges of numbers 3, 5, -6, 0, 7, 11                        |    yes    |
| 3. Log of supplyChanges[1]                                                     |    yes    |
| 4. .pop() correctly used and logged the removed item                           |    yes    |
| 5. .push() the value 25 to supplyChanges                                       |    yes    |
| 6A. For Loop over each item in supplyChanges                                   |    yes    |
| 6B. Correctly Logs Positive Numbers                                            |    no     |
| 6C. Correctly Logs Negative Numbers                                            |    no     |
| 6D. Correctly Logs message for 0                                               |    no     |
| 7. STRETCH Uses For Of loop for refactor                                       |     -     |
| 8. STRETCH Correctly adds all supplyChanges together to equal 34               |     -     |
| 9. STRETCH Uses while loop to calculate 81 boxes filled, and 5 items remaining |     -     |

---

### Notes:

// 6. Write a `for` loop that shows each value in the 'supplyChanges' array
// Use a console.log formatted as follows, where x is the value from the array
// - if it is a positive number (greater than 0), log 'Added x parts.'
// - if the value is 0, log 'No Change.'
// - if the value is negative, format the log as 'Removed x parts.'

```js
console.log('6. Showing supplyChanges...');
for (let i = 0; i < supplyChanges.length; i++) {
  if (supplyChanges[i] > 0) {
    console.log(`Added ${supplyChanges[i]} parts.`);
  } else if (supplyChanges[i] === 0) {
    console.log('No Change.');
  } else if (supplyChanges[i] < 0) {
    console.log(`Removed ${supplyChanges[i] * -1} parts.`); //(* -1) will change negative value into positive value
  }
}
```

---

| General Items                       | Complete? |
| ----------------------------------- | :-------: |
| GitHub config correct               |    yes    |
| At least 3 commits                  |    no     |
| Code is correctly formatted         |    yes    |
| Appropriate amount of code comments |    yes    |

---

### Notes:

Nice work!

- could practice more frequent and descriptive code commits
- The README has some additional information about the style.css; mostly get into the habit of reading the entire README file.
