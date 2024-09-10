Hey Jacob. General comments about the project. (1)

---

| Functional Requirements                                                                          | Complete? |
| ------------------------------------------------------------------------------------------------ | :-------: |
| Input fields for numbers, and a way to select operator                                           |  partial  |
| Submit button or = button runs POST                                                              |    no     |
| All calculations done on the server                                                              |    no     |
| History displays all previous calculations                                                       |    no     |
| GET on page load retrieves all history data on the server                                        |    no     |
| Proper use of GET and POST requests                                                              |    no     |
| Server always sends a response                                                                   |    no     |
| STRETCH: Calculator UI implemented to match example                                              |    no     |
| STRETCH: Input validation prevents the POST call on = submit when any necessary input is missing |    no     |
| STRETCH: Button is added to clear history both on the page and on the server                     |    no     |
| STRETCH: Client makes a DELETE request to clears the history                                     |    no     |
| STRETCH: Server has DELETE route to clear the history array                                      |    no     |
| STRETCH: Items in history can be clicked on to re-run the calculation                            |    no     |
| STRETCH: Calculation result is displayed where answer is shown                                   |    no     |
| STRETCH: Display is updated to show calculation that was run                                     |    no     |
| STRETCH: Calculation is added to history again                                                   |    no     |
| STRETCH: Deploy to Fly                                                                           |    no     |

---

### Notes:

Notes on items above.

---

| General Items                                                | Complete? |
| ------------------------------------------------------------ | :-------: |
| Clear or "C" button clears form inputs                       |    no     |
| More than 10 git commits                                     |  partial  |
| Commits are descriptive of the changes made or feature added |    no     |
| Correct use of id and classes                                |    no     |
| Basic CSS styling                                            |    no     |
| Appropriate amount of code comments                          |    no     |
| Code is consistently formatted                               |    no     |
| Code is consistently indented                                |    no     |

---

### Notes:

Based on some of the latest git commit messages, some refactoring is needed. No problem, let's make those changes and let me know when to review again.

### HTML/CSS

- use a function on the <form> element to capture form submit, ie, `<form onsubmit="submitCalculation(event)">`
- the '=' button will handle submitting the form, ie, `<button type="submit">=</button>`
- the other buttons in the form can have an onclick attribute

### Client

- some overlap of functional responsibilities
- fetchResults() seems to be a duplicate function of getCal()
- refactor the postCal function
  - the .then() is where, upon a successful POST, can call the getCal()

```js
function postCal(numOne, numTwo, operator) {
  axios({
    method: 'POST',
    url: '/calculations',
    data: {
      numOne: numOne,
      numTwo: numTwo,
      operator: operator,
    },
  })
    .then(function (response) {
      const results = document.getElementById('recentResult');
      results.innerText = `Result: ${response.data.result}`;
      console.log('New Calculation:', response.data);
    })
    .catch((error) => {
      console.error(error, 'Error performing calculation');
    });
}
```

### Server

- although .json() is used with built in 'fetch' for HTTP, we have Express middleware to handle json and we can 'send' data and it will be deserialized as json: 'res.send(calculations);'

```js
// GET /calculations
app.get('/calculations', (req, res) => {
  res.json(calculations);
});
```

- ensure that mathematical operations are performed on numbers by casting strings to numbers: Number()

```js
let result = 0;
if (operator === '+') {
  result = Number(numOne) + Number(numTwo); //this will add the numbers vs concatenate strings
}
```

- we can move the 'res.status(201)' to the end of the function.

```js
// POST /calculations
app.post('/calculations', (req, res) => {
  const { numOne, numTwo, operator } = req.body;
  let result = 0;
  if (operator === '+') {
    result = numOne + numTwo;
    res.status(201);
  } else if (operator === '-') {
    result = numOne - numTwo;
    res.status(201);
  } else if (operator === '*') {
    result = numOne * numTwo;
    res.status(201);
  } else if (operator === '/') {
    result = numOne / numTwo;
    res.status(201);
  }

  const newCalculation = { numOne, numTwo, operator, result };
  calculations.push(newCalculation);

  //res.status(201).send(newCalcuation);
  res.json(newCalculation);
});
```
