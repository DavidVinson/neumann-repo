## Part 1, 1-array-practice.js (1)

| Functional Requirements                                        | Complete? |
| -------------------------------------------------------------- | :-------: |
| 1. Favorite Foods Array created and logged                     |    yes    |
| 2. Used `.length` property to find array length                |    no     |
| 3.a Logged second item (index 1) in animal array               |    yes    |
| 3.b Logged last item (index 3) in animal array                 |    yes    |
| 3.c STRETCH Logged last item (length - 1) in animal array      |    no     |
| 4.a Used `.push()` to add item to end of array                 |    no     |
| 4.b Used `.unshift()` to add item to beginning of array        |    yes    |
| 4.c Used `.pop()` to remove the item from end of array         |    yes    |
| 4.d Used `.shift()` to remove the item from beginning of array |    yes    |
| 4.e STRETCH Replaced the second item in the gem array          |     -     |
| 4.f STRETCH Sorted and reversed the gem array                  |     -     |
| 4.g STRETCH Joined the gem array into a string                 |     -     |
| 4.h STRETCH Combined the color array with the gem array        |     -     |

---

### Notes:

// 2. TODO: Create a variable `numberOfFoods` and use the .length property
// to assign it the number value of how many items are inside `favoriteFoods`.
// Don't forget to console.log `numberOfFoods` to make sure your code worked!

- use the 'favFoods' array to get the length.

```js
let numberOfFoods = numberOfFoods.length; //<-took me abit i thought i would use favfoods
console.log('number Of Foods:', numberOfFoods);
```

// 3.b. TODO: Create a variable `lastAnimal` and assign it the value of
// the "last" item in `animalArray`, using its array index.
// You'll need to console.log `animalArray` and `lastAnimal` to make
// sure that your code does what you want. (Never trust your code until
// you have proof that it works!)

- watch for variable case, such as 'lastFood' has a lower case 'l'. The conole log is trying to log out 'LastFood' which is not the same.

```js
let lastFood = numberOfFoods[3]; //<- the "forth food"
console.log('Last Food is', LastFood);
```

// 4.a. TODO: Create a variable `dessert` and assign it a string value of
// a dessert that you love.
// Similar to above, add the `dessert` to the end of your `favoriteFoods`
// array. (How can you be 100% certain this worked? 🤔)

- let dessert = 'ice cream'; // make a variable called 'dessert'
  favoriteFoods.push(dessert); //this adds the variable to the end of the 'favoriteFoods' array.

```js
let dessert = ('ice', 'cream', 'sprinkles'); //<-making this easier for myself
console.log('Dessert are: ', dessert); //<- not 100% if this is correct i think it fine to me
```

---

| General Items                       | Complete? |
| ----------------------------------- | :-------: |
| GitHub config correct               |    yes    |
| At least 3 commits                  |    no     |
| Code is correctly formatted         |    yes    |
| Appropriate amount of code comments |    yes    |

---

### Notes:

good work!

- use the chrome dev console to look for errors. you will see all the console logs there.
- The code looks good, but pay more attention to the details of each question.
- keep practicing arrays and array methods; such as array.push()
