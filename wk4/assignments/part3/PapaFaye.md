Hey Papa. General comments about the project. (1)

- rework complete

---

| Part 3 - Cart System                                                                   | Complete? |
| -------------------------------------------------------------------------------------- | :-------: |
| Runs in browser without console errors                                                 |     -     |
| Using `let` and `const`, no `var`                                                      |    yes    |
| Created global variable for `basket` as empty array                                    |    yes    |
| `addItem` function takes in an item, adds to the array & returns a boolean `true`      |     -     |
| `listItems` loops over `basket` array and logs each item                               |     -     |
| `empty` function resets `basket ` to empty array                                       |    yes    |
| All functions called & tested in the JS file                                           |    no     |
| STRETCH: Created `const` for `maxItems`                                                |     -     |
| STRETCH: `isFull` function correctly returns boolean `true` or `false`                 |     -     |
| STRETCH: `addItem` function updated to use `isFull` and return `false` when full       |     -     |
| STRETCH: `removeItem` function removes & returns the first matching item from `basket` |     -     |
| STRETCH: `removeItem` function returns null when item is not found                     |     -     |

---

### Notes:

- addItem function:

```js
function addItem(newItem) {
  basket.push(newItem);
  return true;
}

console.log('the item was added', addItem('apples'));
```

- listItems function: the for...of loop is partly correct. if you are looping over items in an array, console.log the item, not the array. also, the function does not take an argument, yet it is called with an argument.

```js
function listItems() {
  for (let item of basket);
  //console.log(basket);
  console.log(item);
}
// basket['fruits'] ?????
// call without an argument ---- listItems()
// call with an argument ---- listItems(basket)
// you must declare the function to either take an argument or not.
console.log('each individual item on a new line', listItems(basket['fruits']));
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

Hello Papa, this could use more work. I provided a couple of examples. Rework will need to be complete by Thursday. Reach out to me if you need help.

- even though the test are passing, make sure to call each function and log the results
