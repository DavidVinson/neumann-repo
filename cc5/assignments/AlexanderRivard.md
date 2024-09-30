## Code Challenge #5 Redux Dashboard (3)

| Functional Requirements                                                                                       | Complete? |
| ------------------------------------------------------------------------------------------------------------- | :-------: |
| Components use `useDispatch` correctly                                                                        |    yes    |
| Components use `useSelector` to access Redux values                                                           |    yes    |
| Speed: Reducer Increases and Decreases by 1                                                                   |    yes    |
| Speed: Buttons click dispatches actions to increase and decrease speed reducer value                          |    yes    |
| Speed: Reducer does all the math                                                                              |    yes    |
| Speed: Component renders from Redux                                                                           |    yes    |
| Passenger: View displays list of passenger names                                                              |    yes    |
| Passenger: Button click dispatches action with payload of text input field as new string to passenger reducer |    yes    |
| Passenger: Reducer properly uses spread operator                                                              |    no     |
| Dashboard: Displays current speed reducer speed number                                                        |    yes    |
| Dashboard: Displays current passenger count                                                                   |    yes    |

---

### Notes:

1. State Mutation Issue for the Passenger Reducer.
   The key issue here is that your current implementation mutates the state because of the way you handle newState:

```js
let newState = state;
newState.push(action.payload);
```

The line let newState = state; creates a reference to the original state, meaning any changes to newState (like push()) directly affect state. This breaks the immutability rule in Redux or similar state management systems.

- Fixing the Mutation:
  To avoid mutating the state, create a new array with the existing state and the new passenger. You can use the spread operator (...) or .concat() to ensure that the original state is untouched:

```js
const passengersReducer = (state = ['Alex'], action) => {
  if (action.type === 'ADD_PASSENGER') {
    let newState = [...state, action.payload]; // Creates a new array with existing passengers and the new one
    console.log('running', newState);
    return newState;
  }

  return state;
};
```

This way, newState is a brand-new array, leaving the original state unchanged, preserving immutability.

---

| General Items                                                         | Complete? |
| --------------------------------------------------------------------- | :-------: |
| Speed Reducer default value is 0                                      |    yes    |
| Passenger Reducer default value is an array with their own name in it |    yes    |
| Passenger view uses `.map()` method to display the list               |    yes    |
| Dashboard view displays passenger count using `.length` of array      |    yes    |
| More than 2 git commits descriptive of the changes made               |    yes    |
| Code is consistently formatted                                        |    yes    |
| Appropriate amount of code comments                                   |    no     |

---

### Notes:

Good work!

- do not mutate state in a reducer function.
