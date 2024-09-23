# Code Challenge 4 - React Month List (1)

---

| Functional Requirements                                    | Complete? |
| ---------------------------------------------------------- | :-------: |
| Axios GET request for months in App with `useEffect()`     |    no     |
| Months array stored in `App` local state with `useState()` |    no     |
| Months data passed to `MonthList` Component using props    |    no     |
| `MonthList` loops over months and renders `MonthItem`s     |    no     |
| Month data is passed to `MonthItem` using props            |    no     |
| `MonthItem` renders each individual month name on the DOM  |    no     |

---

### Notes:

---

| General Items                                             | Complete? |
| --------------------------------------------------------- | :-------: |
| `MonthItem` alerts month name on click                    |    no     |
| All axios requests have a .catch() function with an alert |    no     |
| Loop uses `key` with Month id on each MonthItem rendered  |    yes    |
| View uses `.map()` to render `MonthItem` components       |    yes    |
| More than 2 git commits descriptive of the changes made   |    yes    |
| Code is consistently formatted                            |    yes    |
| Appropriate amount of code comments                       |    no     |

---

### Notes:

Provided some pointers to get going on the rework.

- use axios to handle http requests
- load the data into local state, then it can be passed to child components as props
