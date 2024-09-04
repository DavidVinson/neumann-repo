Hey Jacob. General comments about the project. (3)

---

| Functional Requirements                                                            | Complete? |
| ---------------------------------------------------------------------------------- | :-------: |
| Input fields account for all of the data required                                  |    yes    |
| Submit button click appends the new employee data to the employee table on the DOM |    yes    |
| Employee entered is only added to the table once                                   |    no     |
| Employee table has headings/th for each property                                   |    yes    |
| Monthly salary total displays the correct MONTHLY total of all employees           |    yes    |
| Monthly total is styled red if over $20,000                                        |    no     |
| Delete button removes the selected employee data from the DOM                      |    yes    |

---

### Notes:

- the <form> element is a good way to provide addtional form validation instead of just a standard <div>
  - <input> elements in forms can have the 'required' attribute placed, but will only work when in a form element

```html
<form class="form-group" onSubmit="grabValues(event)">
  <input id="f-Name" required class="in" placeholder="First Name" />
  <input id="l-Name" class="in" placeholder="Last Name" />
  <input id="id" class="in" placeholder="ID" />
  <input id="title" class="in" placeholder="Title" />
  <input id="an-sal" class="in" placeholder="Annual Salary" type="number" />
  <button id="submit-btn" type="Submit">Submit</button>
</form>
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

Nice work Jacob! I like how the code has separation of duties by breaking into smaller functions. This is a great practice and will make the code easier to troubleshoot

- The concepts are understood, but some details may have been missed
  - for Total Monthly Salaries: divide all the employee salaries by 12
  - conditonal render the Total Montly Salaries 'red' when the value exceeds $20,000.00
