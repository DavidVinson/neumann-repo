### Part 2 - HTML/CSS (3)

---

| Part 2 - HTML & CSS                                                                   | Complete? |
| ------------------------------------------------------------------------------------- | :-------: |
| CSS file created and sourced in correctly                                             |    yes    |
| Added a `<header>` containing the original `<h1>` and a new `<h2>`                    |    yes    |
| Added a `<main>` containing the `<p>` tag                                             |    yes    |
| Added CSS to give `<header>` dark background, light text, & center text               |    yes    |
| Added CSS for a `background-image` that repeats the `record.png` image                |    yes    |
| Added `margin: 0` for the `<body>` and `padding: 1em` & light background for `<main>` |    yes    |
| STRETCH: Used CSS style classes (except for `<body>`)                                 |     -     |

---

### Notes:

Notes on items above.

---

| General Items                       | Complete? |
| ----------------------------------- | :-------: |
| GitHub config correct               |    yes    |
| At least 4 commits                  |    no     |
| Code is correctly formatted         |    yes    |
| Appropriate amount of code comments |    yes    |

---

### Notes

All good! It's good to keep up with css, it's the first thing people see in an app!

- could use more frequesnt code commits and descriptive commit messages

### CSS

- each element can have its own style. not all tucked in the 'body' element

```
body {
  background-image: url('record.png');
  background-repeat: repeat;
  margin: 0;
}

header {
  background-color: darkslategrey;
  text-align: center;
}
main {
  background-color: lightslategray;
  padding: 1em;
}
```
