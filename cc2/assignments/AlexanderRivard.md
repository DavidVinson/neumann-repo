# Code Challenge 2 (3)

---

| Functional Requirements                                  | Complete? |
| -------------------------------------------------------- | :-------: |
| Existing jokes display on load                           |    yes    |
| List is correctly updated on DOM after new joke is added |    yes    |

---

### Notes:

---

| General Items                                                     | Complete? |
| ----------------------------------------------------------------- | :-------: |
| More than 2 git commits descriptive of the changes made           |    yes    |
| Post route adds joke to array and sends `201` or `200`            |    yes    |
| Another `GET` request is made after post                          |    yes    |
| `.then()` is used to guarantee the `GET` happens after the `POST` |    yes    |
| UI clears inputs upon successful POST                             |    yes    |
| Server uses arrow functions                                       |    yes    |
| All requests have a `.catch()` function defined                   |    yes    |
| Appending logic is in a separate function (not in `.then()`)      |    no     |
| Code is consistently formatted                                    |    yes    |
| Appropriate amount of code comments                               |    yes    |
| Working input validation with a message to the user               |    no     |
| Routes use the same url path/endpoint                             |    yes    |

---

### Notes:

Nice work Alex!

- move the form input clear logic to the .then() statement of the POST. ensures that the form is cleared only upon a successful post
