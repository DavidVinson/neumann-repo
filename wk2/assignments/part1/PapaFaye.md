Hey Papa. General comments about the project. (3) (3)

---

| Part 1 -- aboutMe.js                                                     | Complete? |
| ------------------------------------------------------------------------ | :-------: |
| Use of let/const, no use of var                                          |    yes    |
| Appropriate use of variable types: string, boolean, number               |    yes    |
| First Name assigned to String                                            |    yes    |
| Last Name assigned to String                                             |    yes    |
| Full Name assigned to string concatenation                               |    no     |
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
| STRETCH: Switch statement logs the correct value                         |    no     |
| STRETCH: Ternary written with correct syntax and logic                   |    no     |

---

### Notes:

- #3 fullName: looking to concatenate the firstName and lastName variables
  let fullName = firstName + " " + lastName;

- #12 the variable result is assigned a value based on conditions.

```js
// 12 - Create a variable called `result`. Create a conditional:
//      if adventurous is true, set `result` to be "Adventures are great!",
//      if it's not true,  set `result` to be "How about we stay home?"
//      Console log the value of `result`
let result;
if (adventurous === true) {
  console.log('Adventures are great!');
  result = 'Adventures are great!';
} else {
  console.log(' How about we stay home? ');
  result = 'How about we stay home?';
}
console.log('Result', result);
```

- #14 after this block of code, console.log(petStatus);

```js
let petStatus;
if (pets < allowedPets) {
  petStatus = 'I can have more pets';
  console.log('I can have more pets');
} else if (pets === allowedPets) {
  petStatus = 'I have enough pets';
  console.log(' I have enough pets ');
} else if (pets > allowedPets) {
  petStatus = 'Oh no, I have too many pets!';
  console.log('Oh no, I have too many pets!');
}
//petStatus has been updated with the appropriate message.
console.log(petStatus);
```

- #16 switch statement: use the variable 'luckyResult' that was declared. The case will assign a value to luckyResult, then console.log('luckyResult', luckyResult);

```js
let luckyResult;
switch (luckyNumber) {
  case 1:
    // alert('First is the worst');
    luckyResult = 'First is the worst';
    break;

  case 2:
    // alert('Second is the best');
    luckyResult = 'Second is the best';
    break;

  case 3:
    // alert('Third is the one with the polka dot dress');
    luckyResult = 'Third is the one with the polka dot dress';
    break;

  default:
    // alert('Luck is what happens when preparation meets opportunity');
    luckyResult = 'Luck is what happens when preparation meets opportunity';
}
console.log('LuckyResult', luckyResult);
```

- #17 the structure for a ternary operation:
  condition ? Truthy part : Falsey part;

```js
result = adventurous ? 'Adventures are great!' : 'How about we stay home?';
```

---

| General Items                  | Complete? |
| ------------------------------ | :-------: |
| The assignment repo was forked |    yes    |
| The correct repo was turned in |    yes    |
| GitHub config correct          |    yes    |
| At least 2 commits             |    yes    |
| Code is correctly formatted    |    no     |

---

### Notes:

Nice work! Way to attempt the stretch goals. Look into the ternary operator again.
