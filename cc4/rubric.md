# Code Challenge 10 - React Month List

# Rubric

## Base Requirements

Student needs to write several React components and use axios for a GET request to populate the app. They need to then handle a click event and alert the name of the month clicked.

## Meets Expectations

- `App` component
  - makes axios request in `onComponentDidMount()`
  - Axios GET request retrieves data from provided server route
  - Month list array stored in `App` component's local state
  - Stores clicked-on month name in local state
- `MonthList` component used
  - component shows all `MonthItems` on the DOM
- `MonthItem` displays each month's name string
  - On click alerts month name to user using built-in `alert()`

## Exceeds Expectations

- `Header` component rendered in `App`
  - receives props of clicked on month name
  - displays given month name from props

## Feedback Fodder

### Trying to set State and Use Immediately

Student tries to `setState` on `MonthItem` and then use `this.state` immediately:

```
handleMonthClick = (event) => {
    setSelectedMonth(month);

    //state will not match the above value
    console.log('toggleMonth', selectedMonth);
}
```

Changing state takes some time and the new state is only available in the following `render` update. Plus this component doesn't really need its own state. You can just pass the name along directly:

```
handleClick = (event) => {
    setSelectedMonth(month)
}
```

### Displaying Month in Header (STRETCH as of v4.3)

Student got the click to log the name but didn't get it back to app or to header

```
Fantastic start on the challenge! You are very close to finishing it! You have the correct month showing in the log.

The next step is having a function on `App` that you pass to `MonthList` and then to each `MonthItem` via props. Then the click on `MonthItem` calls a function IN `MonthItem`, which in turn calls `this.props.passedFunctionFromApp()` and sends along the month's name string.

The `App` function stores the string in state and passes the string to `Header` via props.

See if you can work through it this week and ask me any questions you have.

```

## Rubric

For Code Challenge, keep going on rubric until there are 3 `no`s in the general section and then stop. (This way everybody has things to improve, but no student is overwhelmed by amount of feedback.)

### Table

```
# Code Challenge 10 - React Month List

---
| Functional Requirements | Complete? |
| --- | :---: |
| Axios GET request for months in App with `useEffect()` | no |
| Months array stored in `App` local state with `useState()` | no |
| Months data passed to `MonthList` Component using props | no |
| `MonthList` loops over months and renders `MonthItem`s | no |
| Month data is passed to `MonthItem` using props | no |
| `MonthItem` renders each individual month name on the DOM | no |

---

### Notes:


---
| General Items | Complete? |
| --- | :---: |
| `MonthItem` alerts month name on click | no |
| All axios requests have a .catch() function with an alert | no |
| Loop uses `key` with Month id on each MonthItem rendered | no |
| View uses `.map()` to render `MonthItem` components | no |
| More than 2 git commits descriptive of the changes made | no |
| Code is consistently formatted | no |
| Appropriate amount of code comments | no |

---
### Notes:
```
