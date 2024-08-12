Hey Samuel. General comments about the project. (3)

---

| Part 3 - Cart System                                                                   | Complete? |
| -------------------------------------------------------------------------------------- | :-------: |
| Runs in browser without console errors                                                 |    yes    |
| Using `let` and `const`, no `var`                                                      |    yes    |
| Created global variable for `basket` as empty array                                    |    yes    |
| `addItem` function takes in an item, adds to the array & returns a boolean `true`      |    yes    |
| `listItems` loops over `basket` array and logs each item                               |    yes    |
| `empty` function resets `basket ` to empty array                                       |    yes    |
| All functions called & tested in the JS file                                           |    yes    |
| STRETCH: Created `const` for `maxItems`                                                |     -     |
| STRETCH: `isFull` function correctly returns boolean `true` or `false`                 |     -     |
| STRETCH: `addItem` function updated to use `isFull` and return `false` when full       |     -     |
| STRETCH: `removeItem` function removes & returns the first matching item from `basket` |     -     |
| STRETCH: `removeItem` function returns null when item is not found                     |     -     |

---

### Notes:

- Nice use of built-in array method!!

```js
function listItems() {
  basket.forEach((item) => console.log(item));
}
```

- Very clean way to empty an array

```js
function empty() {
  basket.length = 0;
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

The functions were clean and concise!

- would like to see you try out the stretch goals
