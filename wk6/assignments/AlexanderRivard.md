Hey Alex. General comments about the project. (3)

---

| Functional Requirements                                                                              | Complete? |
| ---------------------------------------------------------------------------------------------------- | :-------: |
| DOM is ready?                                                                                        |    yes    |
| Three inputs and button on DOM                                                                       |    yes    |
| On click, the client.js file adds the car data to the array                                          |    yes    |
| After a new car is added to the array, all cars in the array are re-appended on the DOM              |    yes    |
| Styling in CSS file                                                                                  |    yes    |
| Using `let` and `const`, no `var`                                                                    |    yes    |
| Runs in browser without console errors                                                               |    yes    |
| STRETCH: Inputs clear after button is clicked                                                        |    yes    |
| STRETCH: Car not added to array if fields are blank (and this is communicated to the user)           |    yes    |
| STRETCH: Maximum number of spaces and user is prevented from adding more                             |    yes    |
| STRETCH: User is informed when garage array is at capacity                                           |    yes    |
| STRETCH: Input for image url, saved with car information in object, displayed with other info on DOM |     -     |

---

### Notes:

Notes on items above.

---

| General Items                       | Complete? |
| ----------------------------------- | :-------: |
| GitHub config correct               |    yes    |
| At least 4 commits                  |    yes    |
| Code is correctly formatted         |    yes    |
| Appropriate amount of code comments |    yes    |

---

### Notes:

Really good!

HTML:

- good job on form validation; using the _*required*_ attribute on the form inputs is also a good practice
- use the 'defer' attribute for the <script src="file.js" defer></script>. this attribute waits to load the javascript file until
  the index.html file is loaded.

JS:

- putting the renderGarage function when the file loads is good practice; display something right away
  - // if there are no cars; return -> this will display the <li>da garage</li> in the html <ul>
    if (garage.length === 0) {
    return;
    }
- nice work clearing the form after it is submitted!
