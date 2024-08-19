### Part 3 - `3-music-collection.js` (5)

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
| STRETCH: `search` takes in a criteria object and returns an array of matching albums               |    yes    |
| STRETCH: Added an array of `tracks` to the albums and updated functions to work with this property |    yes    |
| STRETCH: All Stretch functions tested fully                                                        |    yes    |

---

### Notes:

Notes on items above.

---

| General Items                       | Complete? |
| ----------------------------------- | :-------: |
| GitHub config correct               |    yes    |
| At least 4 commits                  |    yes    |
| Code is correctly formatted         |    yes    |
| Appropriate amount of code comments |    yes    |

---

### Notes:

Really nice work!

- short circuit: the below code can be shortened to if (!showTracklist) {...}
  will check for falsey statements: undefined, null, false, 0, "" (empty string), NaN (Not a Number)

```
  if(showTracklist === undefined || showTracklist === false){...}
```

- way leverage functions calling other functions!!

- string literal: \t in a string template will create a tab. useful to see sub groups such as the tracklist

```
console.log(`\t${i + 1}. ${album.tracks[i].name} : ${album.tracks[i].duration}`);
```

### Search Function Solution (stretch goal)

- search function using the '!' operator to check falsey statements

```js
function search(collection, searchCriteria, trackName) {
  let matches = [];
  if (trackName) {
    for (let i = 0; i < collection.length; i++) {
      for (let j = 0; j < collection[i].tracks.length; j++) {
        if (collection[i].tracks[j].name === trackName) {
          matches.push(collection[i]);
        }
      }
    }
    return matches;
  } else if (
    !searchCriteria ||
    !searchCriteria.artist ||
    !searchCriteria.yearPublished ||
    Object.keys(searchCriteria).length === 0
  ) {
    //checks if object has properties
    return collection;
  }

  for (let i = 0; i < collection.length; i++) {
    if (
      collection[i].artist === searchCriteria.artist &&
      collection[i].yearPublished === searchCriteria.yearPublished
    ) {
      matches.push(collection[i]);
    }
  }
  return matches;
}
```
