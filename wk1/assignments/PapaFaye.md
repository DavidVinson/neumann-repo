Hey Papa. Welcome to week 1 feedback! (3)

To set a little context, even if everything is amazing, we always give feedback on how we think you could improve - there's no such thing as perfect code, and there's always room for improvement.

---

| HTML, CSS, & JS                                          | Complete? |
| -------------------------------------------------------- | :-------: |
| HTML: Change the title to "Hello World"                  |    yes    |
| HTML: Create an `<h1>` containing your name              |    yes    |
| HTML: Include an image                                   |    yes    |
| HTML: Create an unordered list with 3 list items         |    yes    |
| HTML: Create a footer                                    |    yes    |
| HTML: Put a `<p>` with your favorite quote in the footer |    yes    |
| CSS: Give your page a fun background color               |    yes    |
| CSS: Make the header and footer a different color        |    yes    |
| CSS: Center the h1 with your name                        |    yes    |
| CSS: Make your p tag a different color and italic        |    yes    |
| CSS: Put a border around your image                      |    yes    |
| CSS: Change the font-family of your list                 |    yes    |
| JS: JS contains console log                              |    yes    |
| Runs in browser without console errors                   |    no     |

---

### Notes:

A few things to work on, but overall looks good!

- get into a good habit of formatting the files (html, css, js) to ensure good readability. Formatting makes a big difference in trying to troubleshoot missing element tags, etc. VS code has a built in formatter (Shift + Option + F). try it out and see what you think. There are also 3rd part extensions such as Prettier that are available.

HTML:

- referencing a javascript file in the head section of the html file: use the <script src="./helloWorld.js"></script> element and the src attribute.
- having the <script>console.log("hello world again");</script> in the body of the html document will work as well, but you will see EDA reference a javascript file in the head section more often.

- the <link /> to the helloWorld.js file can be removed.

```js
link rel="stylesheet" href="/Users/a/EDA/Tier1/week1/eda-pw-week-1-assignment/assignment/helloWorld.js" />
```

- image: use a relative path to the images folder and the picture will load.
  <img class="My picture" src="../images/my-picture-460 × 460.jpeg" alt="A handsome guy" />

CSS:

- an alternative to styling the <li> elements, one could style the <ul> that would cascade to each <li>. How the code is right now is just fine, but just anther option.

Javascript:

- get into the habit of using ";" semi-colon at the end of javascript statements. ex,

```js
console.log('hello world');
```

---

| General Items                  | Complete? |
| ------------------------------ | :-------: |
| The assignment repo was forked |    yes    |
| The correct repo was turned in |    yes    |
| GitHub config correct          |    yes    |
| More than 1 commit             |    yes    |
| Code is correctly formatted    |    yes    |

---

### Notes:

This is really good! I'd strongly recommend committing more often. Every time you get something new working (probably every 30 minutes or so), make a commit. You're saving your progress so that if something goes wrong, you can go back!

Great work!
