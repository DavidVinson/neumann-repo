# Code Challenge 8 - Node/Express/JSDom with Jokes Data

> Node, Express, JavaScript DOM

## Requirements

### Base Requirements

- Student needs to write an AXIOS GET and corresponding route on the server to return an array of joke data objects
- Student needs to write an AXIOS POST request and corresponding route on the server to add a new joke to the existing jokes data array.

### Meets Expectations

- Existing joke data displayed on load
- POST sends data as an object with current input field values
- DOM updates to display new joke data

## Feedback

Be sure to note formatting and anything missing from above (duplicates on DOM, missing `.catch`, etc )

## Nice to Haves

- `.then()` function defined
  - If missing `.catch()`, that is OK
  - If DOM duplicates instead of emptying, that is OK
- Refreshing GET request made from inside of POST `.then()`
  - If made outside `.then()` but still works, that is OK
- `POST` route adds new joke object to array
- `POST` route sends status of `200` or `201`
- `GET` route sends jokes array
- Uses arrow functions
- All requests have a `.catch()` function defined
- Appending logic is in a separate function (not in `.then()`)
- UI clears inputs upon successful POST
- Routes have matching url/endpoint
- Working input validation with a message to the user
- Has routing modules on the server
- Routes use the same url path/endpoint
  - `/jokes` is a good one but could be anything

## Rubric

For Code Challenge, keep going on rubric until there are 3 `no`s in the general section and then stop. (This way everybody has things to improve, but no student is overwhelmed by amount of feedback.)

### Table

```
---
| Functional Requirements | Complete? |
| --- | :---: |
| Existing jokes display on load | no |
| List is correctly updated on DOM after new joke is added | no |

---
### Notes:



---
| General Items | Complete? |
| --- | :---: |
| More than 2 git commits descriptive of the changes made | no |
| Post route adds joke to array and sends `201` or `200` | no |
| Another `GET` request is made after post | no |
| `.then()` is used to guarantee the `GET` happens after the `POST` | no |
| UI clears inputs upon successful POST | no |
| Server uses arrow functions | no |
| All requests have a `.catch()` function defined | no |
| Appending logic is in a separate function (not in `.then()`) | no |
| Code is consistently formatted | no |
| Appropriate amount of code comments | no |
| Working input validation with a message to the user | no |
| Routes use the same url path/endpoint | no |

---
### Notes:

```
