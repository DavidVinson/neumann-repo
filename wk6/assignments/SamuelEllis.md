Hey Samuel. General comments about the project. (1)

---

| Functional Requirements                                                                              |      Complete?      |
| ---------------------------------------------------------------------------------------------------- | :-----------------: |
| DOM is ready?                                                                                        |         yes         |
| Three inputs and button on DOM                                                                       |         yes         |
| On click, the client.js file adds the car data to the array                                          |         no          |
| After a new car is added to the array, all cars in the array are re-appended on the DOM              |         no          |
| Styling in CSS file                                                                                  | yes, but not loaded |
| Using `let` and `const`, no `var`                                                                    |         yes         |
| Runs in browser without console errors                                                               |         no          |
| STRETCH: Inputs clear after button is clicked                                                        |       partial       |
| STRETCH: Car not added to array if fields are blank (and this is communicated to the user)           |          -          |
| STRETCH: Maximum number of spaces and user is prevented from adding more                             |          -          |
| STRETCH: User is informed when garage array is at capacity                                           |          -          |
| STRETCH: Input for image url, saved with car information in object, displayed with other info on DOM |          -          |

---

### Notes:

Notes on items above.

---

| General Items                       | Complete? |
| ----------------------------------- | :-------: |
| GitHub config correct               |    yes    |
| At least 4 commits                  |    no     |
| Code is correctly formatted         |    no     |
| Appropriate amount of code comments |    yes    |

---

### Notes:

The repo was empty (update: had Samuel add me to the repo)
The assignment is not complete. Look to use the videos/notes on DOM manipulation and apply to this assignment

HTML:

- The CSS file is not sourced in correctly. Look at the relative path in relation to the index file
- remove any unused elements, ie buttons that do not have any functionality attached to them

CSS:

- the css looks really good! the form and buttons are styled
- look to add style to the element that will contain the cars; ie, the <ul>

Javascript:

- accessing the DOM elements, creating the newCar object, and pushing to the garage looks good
- display/render the garage on the DOM is not complete. Look to use videos/notes to finish rendering the cars on the page
- removing a car from the DOM is incomplete

## Part 2: Remove a car from the garage

Add a "Remove Car" button next to each car in the garage.

For **Base Mode** it is ok to remove the car directly from the DOM, without updating state.
