Hey Jenny. General comments about the project. (3) (3)

---

| Part 1 -- aboutMe.js                                                     | Complete? |
| ------------------------------------------------------------------------ | :-------: |
| Use of let/const, no use of var                                          |    yes    |
| Appropriate use of variable types: string, boolean, number               |    yes    |
| First Name assigned to String                                            |    yes    |
| Last Name assigned to String                                             |    yes    |
| Full Name assigned to string concatenation                               |    yes    |
| Full Name logged                                                         |    yes    |
| Lucky Number assigned to Number                                          |    yes    |
| Name and Lucky Number sentence logged                                    |    yes    |
| Adventurous assigned to Boolean                                          |    yes    |
| Food assigned to String                                                  |    yes    |
| Pets assigned to Number                                                  |    yes    |
| Friends Pets assigned to Number                                          |    yes    |
| Add two to Pets                                                          |    yes    |
| Allowed Pets assigned to a constant                                      |    yes    |
| Correctly log based on adventurous boolean                               |    yes    |
| Runs in browser without console errors                                   |    yes    |
| "Roll the dice" conditional includes lucky number and adventurous checks |    yes    |
| Pets conditional checks less than, equal and greater than                |    yes    |
| STRETCH: Correctly log the greater value (pets or friends pets)          |    yes    |
| STRETCH: Correctly log pets or friends pets if they are equal            |    yes    |
| STRETCH: Conditionals written with correct syntax                        |    yes    |
| STRETCH: Switch statement logs the correct value                         |    yes    |
| STRETCH: Ternary written with correct syntax and logic                   |    yes    |

---

### Notes:

- this statement is all good; sigle quotes for javascript and ending with the semi-colon. however, we will get into functions in a couple of weeks, but there is no space between console.log('My first name is: firstName'); make those changes to all the console.log() statements.

```js
console.log('My first name is: ', firstName);
```

- conditional clause: below, the variable 'adventurous' is being assigned to the value 'true'. using '=' is the assignment operator. typically, in conditional statements, using the '===' is a strict equality operator. for ex, if (adventurous === true) {...}

```js
let result;
if ((adventurous = true)) {
  result = 'Adventures are great!';
} else {
  result = 'How about we stay home?';
}
console.log(result);
```

- in conditional statements using the equality operator, get into the habit of using '===' vs '=='. The '===' is the strict equality operator and is a safer way to make a comparison. the '==' is also an equality operator, but it coerces a match.

```js
let diceRoll;
if (luckyNumber == 2 && adventurous == true) {
  diceRoll = 'Roll the dice';
} else {
  diceRoll = 'Try again later.';
}

console.log(diceRoll);
```

---

| General Items                  | Complete? |
| ------------------------------ | :-------: |
| The assignment repo was forked |    yes    |
| The correct repo was turned in |    yes    |
| GitHub config correct          |    yes    |
| At least 2 commits             |    yes    |
| Code is correctly formatted    |    yes    |

---

### Notes:

Nice work, way to attempt the stretch goals!

- #16: Switch statements are another way to conditionally check a condition and assign a variable to the result of the condition. earlier, we created a variable called luckyNumber and set a value to be a number. We want our switch statement cases to be evaluated against our luckyNumber, which is of type Number. meaning, case 1: will check to see if our luckyNumber is equal to 1 (type Number). essentially, we want to match like types: numbers to numbers, strings to strings, etc.

```js
const luckyResult = '';

switch (luckyResult) {
  case 1:
    luckyResult = 'First is the worst';
    break;
  case 2:
    luckyResult = 'Second is the best';
    break;
  case 3:
    luckyResult = 'Third is the one with the polka dot dress';
    break;
  default:
    luckyResult = 'Luck is what happens when preparation meets opportunity';
    break;
}
console.log(luckyResult);
```

- #17: Great work on the ternary operator!! same idea as earlier with checking for equality, use the '===', otherwise this is spot on!

```js
result = (adventurous = true) ? 'Adventures are great!' : 'How about we stay home?';

console.log(result);
```
