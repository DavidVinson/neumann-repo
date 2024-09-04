Hey Jenny. General comments about the project. (3)

---

| Functional Requirements                                                            | Complete? |
| ---------------------------------------------------------------------------------- | :-------: |
| Input fields account for all of the data required                                  |    yes    |
| Submit button click appends the new employee data to the employee table on the DOM |    yes    |
| Employee entered is only added to the table once                                   |    no     |
| Employee table has headings/th for each property                                   |    yes    |
| Monthly salary total displays the correct MONTHLY total of all employees           |    yes    |
| Monthly total is styled red if over $20,000                                        |    yes    |
| Delete button removes the selected employee data from the DOM                      |    yes    |

---

### Notes:

- excellent work on incorporating the number format! super handly in displaying monetary values

```js
new Intl.NumberFormat('en-US');
```

- be more specific when using 'id', ie, the id could be id="monthly-salary-total"
  - <h3 id="hThreeTwo">$6250</h3>

---

| General Items                                                | Complete? |
| ------------------------------------------------------------ | :-------: |
| More than 8 git commits                                      |    yes    |
| Commits are descriptive of the changes made or feature added |    yes    |
| Correct use of id and classes                                |    yes    |
| Correct use of HTML elements                                 |    yes    |
| Appropriate amount of code comments                          |    no     |
| Code is consistently formatted                               |    yes    |
| Input fields cleared when employee added                     |    yes    |

---

### Notes:

Nice work Jenny! All the functionality does what it is expected to do.

- good use of the 'defer' attribute for the javascript file!
- could use more code comments to help describe what a function or block of code is expected to do
- handling forms; the <form> element will have an 'onsubmit="addSomething(event)".
