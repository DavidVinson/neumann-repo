# Code Challenge 2 (3)

---

| Functional Requirements                                  | Complete? |
| -------------------------------------------------------- | :-------: |
| Existing jokes display on load                           |    no     |
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
| Working input validation with a message to the user               |    yes    |
| Routes use the same url path/endpoint                             |    yes    |

---

### Notes:

Nice work Jenny! It's really close

- a function that fetches all the jokes can be called in the onReady function, there is a function, just needs to be called
- appending to the DOM in a Post function is not necessary as the after a successful post, a call to fetech/display can handle the DOM manipulation
- the below works due to the `document.getElementById('whose-joke').value = '';`. the variables are not accessed

```js
let whoseJoke = (document.getElementById('whose-joke').value = '');
let jokeQuestion = (document.getElementById('joke-question').value = '');
let punchLine = (document.getElementById('punch-line').value = '');
```
