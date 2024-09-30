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
| Passenger: Reducer properly uses spread operator                                                              |    yes    |
| Dashboard: Displays current speed reducer speed number                                                        |    yes    |
| Dashboard: Displays current passenger count                                                                   |    yes    |

---

### Notes:

1. Passengers.jsx

- Remove unused useEffect if it's not doing anything. The useEffect hook is currently empty:
- Use camel case naming for the state setter (setNewPassenger).

2. Dashboard.jsx

- by convention, use lowercase for variables, upper case use for function components and global constants.
  const Speed = useSelector((store) => store.speed);
  const Passengers = useSelector((store) => store.passengers);

---

| General Items                                                         | Complete? |
| --------------------------------------------------------------------- | :-------: |
| Speed Reducer default value is 0                                      |    yes    |
| Passenger Reducer default value is an array with their own name in it |    yes    |
| Passenger view uses `.map()` method to display the list               |    yes    |
| Dashboard view displays passenger count using `.length` of array      |    yes    |
| More than 2 git commits descriptive of the changes made               |    no     |
| Code is consistently formatted                                        |    yes    |
| Appropriate amount of code comments                                   |    no     |

---

### Notes:

Nice work!

- the redux store was spot on!!
