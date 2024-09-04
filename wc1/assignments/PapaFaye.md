Hey Papa. General comments about the project. (3)

---

| Functional Requirements                                                            | Complete? |
| ---------------------------------------------------------------------------------- | :-------: |
| Input fields account for all of the data required                                  |    yes    |
| Submit button click appends the new employee data to the employee table on the DOM |    yes    |
| Employee entered is only added to the table once                                   |    yes    |
| Employee table has headings/th for each property                                   |    yes    |
| Monthly salary total displays the correct MONTHLY total of all employees           |    yes    |
| Monthly total is styled red if over $20,000                                        |    no     |
| Delete button removes the selected employee data from the DOM                      |    yes    |

---

### Notes:

- the <form> element will have the 'onsubmit' action, ie, <form onsubmit="onSubmit(event)">

```js
<form>
  <input id='firstName' placeholder='First Name' required />
  <input type='text' id='lastName' placeholder='Last Name' required />
  <input type='number' id='id' placeholder='ID' required />
  <input type='text' id='title' placeholder='Title' required />
  <input type='number' id='salary' placeholder='Annual Salary' required />
  <button id='submit' onsubmit='onSubmit(event)'>
    Submit
  </button>
</form>
```

- need conditional render for total monthly salary that is greater than $20,000.00, ie,

```js
if (totalMonthly > 20000) {
  //display the total monthly in red text on the DOM
} else {
  //remove the red text
}
```

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

Good work Papa!

- really good job updating the README file, this is often missed
- use code comments to help describe what the code is expected to do
- we can discuss alternative ways of displaying data to the DOM
