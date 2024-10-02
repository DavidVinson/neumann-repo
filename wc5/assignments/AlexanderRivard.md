Hey Alex, (3)

---

| Functional Requirements                                                | Complete? |
| ---------------------------------------------------------------------- | :-------: |
| Multi page form with client side routing and navigation (next button)  |    yes    |
| Data stored in Redux when navigating from page to page                 |    yes    |
| User is notified when trying to leave a blank score                    |    yes    |
| Review Component displays scores and comments from current redux state |    yes    |
| Submit button sends data to the server via Axios                       |    yes    |
| Confirmation Page displays after data is POSTed to the server          |    yes    |
| Button on Confirmation Page starts a new survey                        |    yes    |
| Views are broken down into components                                  |    yes    |

---

### Notes:

1. store.js

- having the initial state equal an object with the key/value pairs identified is a great start!
- move async data handling, ie axios calls, out of reducers
- careful not to mutate state directly; make use of the spread operator

```js
if (action.type === 'SET_FEELS') {
  let newState = state; //this makes a direct reference to state
  if (Number(action.payload) >= 5) {
    action.payload = '5';
  } else if (Number(action.payload) <= 0) {
    action.payload = '0';
  }
  newState.feels = action.payload;
  return newState;
}

if (action.type === 'SET_FEELS') {
  let newState = { ...state }; //use spread operator to make a shallow copay of state
  if (Number(action.payload) >= 5) {
    action.payload = '5';
  } else if (Number(action.payload) <= 0) {
    action.payload = '0';
  }
  newState.feels = action.payload;
  return newState;
}
```

2. Feeling.jsx

- use local state to capture user inputs; then the submit function can dispatch({type: "SET_FEELS", payload: feeling}) to reducer

```js
const [feeling, setFeeling] = useState(0);
//a function to dispatch the local state to redux reducer
dispatch({ type: 'SET_FEELS', payload: feeling });
```

3. Review.jsx

- make the axios.post call to the server with the feedback object from redux

---

| General Items                                                | Complete? |
| ------------------------------------------------------------ | :-------: |
| More than 15 git commits                                     |    yes    |
| Commits are descriptive of the changes made or feature added |    yes    |
| Readme file updated                                          |    yes    |
| Appropriate amount of code comments                          |    yes    |
| Code is consistently formatted                               |    yes    |
| Server code organized with router & module files             |    yes    |
| Dispatch action to clear redux state on new survey           |    yes    |

---

### Notes:

Overall, the requirements were met, but there are some things to clean up.

- the code functions, which is good, but better practices should be used.
- using local state to capture user inputs is the React way. Reaching out to the DOM works, but best practice is capturing inputs via local state.
- in reducers, using the spread operator to make a shallow copy of state, then can modify the copy ensures state is not mutated directly.
