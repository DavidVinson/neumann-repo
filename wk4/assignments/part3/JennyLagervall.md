Hey Jenny. General comments about the project. (1)

- rework compelte

---

| Part 3 - Cart System                                                                   | Complete? |
| -------------------------------------------------------------------------------------- | :-------: |
| Runs in browser without console errors                                                 |    yes    |
| Using `let` and `const`, no `var`                                                      |    yes    |
| Created global variable for `basket` as empty array                                    |    yes    |
| `addItem` function takes in an item, adds to the array & returns a boolean `true`      |    yes    |
| `listItems` loops over `basket` array and logs each item                               |    yes    |
| `empty` function resets `basket ` to empty array                                       |    yes    |
| All functions called & tested in the JS file                                           |    no     |
| STRETCH: Created `const` for `maxItems`                                                |    yes    |
| STRETCH: `isFull` function correctly returns boolean `true` or `false`                 |    no     |
| STRETCH: `addItem` function updated to use `isFull` and return `false` when full       |     -     |
| STRETCH: `removeItem` function removes & returns the first matching item from `basket` |     -     |
| STRETCH: `removeItem` function returns null when item is not found                     |     -     |

---

### Notes:

- the empty basket test may be failing, but the code works. the test is for this function is not taking an argument, so it will fail when this code runs: empty(array) {...}

---

| General Items                       | Complete? |
| ----------------------------------- | :-------: |
| GitHub config correct               |    yes    |
| At least 3 commits                  |    no     |
| Code is correctly formatted         |    yes    |
| Appropriate amount of code comments |    yes    |

---

### Notes:

Good work.

- even though the test are passing, make sure to call each function and log the results (listItems)
