# Code Challenge 2 (1)

---

| Functional Requirements                                  | Complete? |
| -------------------------------------------------------- | :-------: |
| Existing jokes display on load                           |    yes    |
| List is correctly updated on DOM after new joke is added |    no     |

---

### Notes:

---

| General Items                                                     | Complete? |
| ----------------------------------------------------------------- | :-------: |
| More than 2 git commits descriptive of the changes made           |    yes    |
| Post route adds joke to array and sends `201` or `200`            |    yes    |
| Another `GET` request is made after post                          |    no     |
| `.then()` is used to guarantee the `GET` happens after the `POST` |    yes    |
| UI clears inputs upon successful POST                             |    no     |
| Server uses arrow functions                                       |    yes    |
| All requests have a `.catch()` function defined                   |    no     |
| Appending logic is in a separate function (not in `.then()`)      |    no     |
| Code is consistently formatted                                    |    yes    |
| Appropriate amount of code comments                               |    no     |
| Working input validation with a message to the user               |    yes    |
| Routes use the same url path/endpoint                             |    yes    |

---

### Notes:

Good start! The onReady function has too much going on. Really just need to fetch the jokes

- all logic is currently nested in the onReady function, look to remove code that is event based, ie, a user clicks a button
- the css events are really good!
- the post is getting to the server, but after a successful post, the data needs to be fetched again to refresh the DOM
