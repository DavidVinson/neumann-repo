### Part 3 - `3-music-collection.js` (3)

---

| Part 3 - Music Collection                                                                          | Complete? |
| -------------------------------------------------------------------------------------------------- | :-------: |
| Using `let` and `const` - no `var`                                                                 |    yes    |
| Functions do not create errors or exceptions in the browser console                                |    yes    |
| `collection` array initialized as an empty array                                                   |    yes    |
| `addToCollection` pushes record object into the array & returns the object                         |    yes    |
| Tested `addToCollection` by adding 6 albums & logged results                                       |    yes    |
| `showCollection` takes in an array, loops over it logging each item                                |    yes    |
| Tested `showCollection` function                                                                   |    yes    |
| `findByArtist` takes in an artist and returns an array of matching albums                          |    yes    |
| Tested `findByArtist` function for both a match and no match                                       |    yes    |
| STRETCH: `search` takes in a criteria object and returns an array of matching albums               |     -     |
| STRETCH: Added an array of `tracks` to the albums and updated functions to work with this property |     -     |
| STRETCH: All Stretch functions tested fully                                                        |     -     |

---

### Notes:

Notes on items above.

---

| General Items                       | Complete? |
| ----------------------------------- | :-------: |
| GitHub config correct               |    yes    |
| At least 4 commits                  |    yes    |
| Code is correctly formatted         |    no     |
| Appropriate amount of code comments |    yes    |

---

### Notes:

Very nice work!

- good job testing the functions
- get into the habit of formatting the files (Shift + Option + F)

### Search Function Solution (stretch goal)

- posted a solution to the search function

```js
function search(collection, searchObj) {
  let collect = [];
  console.log('running');
  // return the collection if there is bad search data; will not even attempt the loop
  if (!searchObj || Object.keys(searchObj).length === 0 || !searchObj.artist || !searchObj.yearPublished) {
    return collection;
  }
  // if the data is good, loop to find the match
  // instead of nested if statements (which will work) a cleaner way is put on one line
  for (let i of collection) {
    if (i.artist === searchObj.artist && i.yearPublished === searchObj.yearPublished) {
      collect.push(i);
    }
  }
  return collect;
}
```
