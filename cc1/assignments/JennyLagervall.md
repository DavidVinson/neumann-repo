# Code Challenge 7 - JavaScript, DOM with Red and Yellow Boxes (1)

---

| Functional Requirements                                                                                  | Complete? |
| -------------------------------------------------------------------------------------------------------- | :-------: |
| Generate button appends a new `div` on the DOM                                                           |    yes    |
| New `div` contains a `p` element which contains the number of times the Generate button has been clicked |    yes    |
| New `div` contains a button labeled "Yellow"                                                             |    yes    |
| New `div` contains a button labeled "Delete"                                                             |    yes    |
| New `div` has a red background color                                                                     |    yes    |
| Background color style is defined in a CSS file                                                          |  partial  |
| Clicking Yellow button swaps background color of parent `div` from red to yellow                         |    no     |
| Clicking Delete button removes parent `div` (and the p, buttons, etc)                                    |    yes    |

---

### Notes:

---

| General Items                                           | Complete? |
| ------------------------------------------------------- | :-------: |
| Proper use of HTML classes and ids                      |    yes    |
| More than 2 git commits descriptive of the changes made |    no     |
| Code is consistently formatted                          |    yes    |
| Appropriate amount of code comments                     |    no     |

---

## Common Problems

The concepts are coming along, however, some base functionality is close, but needs adjustments

- could use some more code comments to describe what the code is expected to do
- the yellow button currently does not change the div color to yellow; use 'event.target' to find what button was selected. The same pattern used for the delete button.
