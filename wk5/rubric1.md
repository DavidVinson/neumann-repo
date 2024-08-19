### Part 1 - `1-object-practice.js`

---

| Part 1 - Object Practice                                            | Complete? |
| ------------------------------------------------------------------- | :-------: |
| Functions do not create errors or exceptions in the browser console |     -     |
| Using `let` and `const`, no `var`                                   |     -     |
| Properties added correctly to `me` object                           | partial\* |
| `fullName` set correctly using object properties                    |     -     |
| Correctly logged foods from nested array property                   |     -     |
| Updated `shoeCount` & logged new value from `me` object             |     -     |
| Added new `favoriteColor` property & logged `me` object             |     -     |

---

### Notes:

Notes on items above.

---

| General Items                       | Complete? |
| ----------------------------------- | :-------: |
| GitHub config correct               |     -     |
| At least 4 commits                  |     -     |
| Code is correctly formatted         |     -     |
| Appropriate amount of code comments |     -     |

---

### Notes:

Notes on items above.

## Feedback Snippets

### Properties for Object Literal

When you're adding properties to the `me` object in step 1, it would be fine to add them all inside the object literal. Adding them after is not wrong, but it is more typically done all in one step:

```
const me = {
  firstName: 'John',
  lastName: 'Doe',
  hasSiblings: true,
  shoeCount: 1,
  favThreeFoods: ['apples', 'bananas', 'corn'];
}
```

### Template Literal Strings

Note that you can use _Template Literal Strings_ to assemble and format text with variables. These are created using backtics ` which is typically the key above tab with the ~.

```
let fullName = `${me.firstName} ${me.lastName}`
console.log(`Hello, my name is ${fullName}`);
```

### Search Function Solution (stretch goal)

Let's take a look at this stretch goal. This will be very similar to the `findByArtist` function, except that our input argument is an object. Our goal is to be able to use this `search()` function like:

```js
// Prepare the search criteria argument
let searchCriteria = { artist: 'Ray Charles', year: 1957 };

// Run the search
let results = search(searchCriteria);
console.log(results);
/*
Logs an array of albums, like:
[
  { title: 'Ray Charles', artist: 'Ray Charles', year: 1957 },
  { title: 'The Great Ray Charles', artist: 'Ray Charles', year: 1957 },
]
*/
```

We can also pass the `searchCriteria` object directly to the function all in one step:

```js
let results = search({
  artist: 'Ray Charles',
  year: 1957,
});
console.log(results);
```

Let's see now if we can figure out how to implement this `search()` function:

```js
function search(criteria) {
  // Prepare an array to hold our matching albums
  let matchingAlbums = [];

  // Loop through the collecion array
  for (let album of collection) {
    // Check if the artist and year match
    if (criteria.artist === album.artist && criteria.year === album.year) {
      // If it's a match,
      // add this album to our array
      matchingAlbums.push(album);
    }
  }

  return matchingAlbums;
}
```

### Comments

You _could_ start to add more comments to your code though. A lot is said here through the console.logs and naming of functions and variables. However it is common professionally to add comments before functions to explain their inputs, output, and purpose.
