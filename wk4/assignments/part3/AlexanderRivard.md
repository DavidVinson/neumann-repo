Hey Alex. General comments about the project. (3)

---

| Part 3 - Cart System                                                                   | Complete? |
| -------------------------------------------------------------------------------------- | :-------: |
| Runs in browser without console errors                                                 |    yes    |
| Created global variable for `basket` as empty array                                    |    yes    |
| `addItem` function takes in an item, adds to the array                                 |    yes    |
| `addItem` function returns true                                                        |    yes    |
| `listItems` loops over `basket` array and logs each item                               |    yes    |
| `empty` function empties the `basket` array                                            |    yes    |
| STRETCH: Added a global const named `maxItems` and set it to 5                         |    yes    |
| STRETCH: `isFull` function correctly returns boolean `false`                           |    yes    |
| STRETCH: `isFull` function correctly returns boolean `true`                            |    yes    |
| STRETCH: `addItem` function updated to use `isFull` and return `false` when full       |    yes    |
| STRETCH: `removeItem` function removes & returns the first matching item from `basket` |    yes    |
| STRETCH: `removeItem` function returns null when item is not found                     |    yes    |

---

### Notes:

- removeItem function: casting strings to lower case is a good idea.

```js
function removeItem(item) {
  let lowerCaseItems = [];
  for (let x of basket) {
    lowerCaseItems.push(x.toLowerCase());
  }
  let i = lowerCaseItems.indexOf(item.toLowerCase());
  let ret = lowerCaseItems.splice(i, i);
  if (ret.length < 1) {
    return null;
  }
  return ret[0];
}
```

---

| General Items                       | Complete? |
| ----------------------------------- | :-------: |
| GitHub config correct               |    yes    |
| At least 3 commits                  |    yes    |
| Code is correctly formatted         |    yes    |
| Appropriate amount of code comments |    yes    |

---

### Notes:

Good work!
