Hey Samuel. Welcome to week 1 feedback! (3)

To set a little context, even if everything is amazing, we always give feedback on how we think you could improve - there's no such thing as perfect code, and there's always room for improvement.

---

| HTML, CSS, & JS                                          | Complete? |
| -------------------------------------------------------- | :-------: |
| HTML: Change the title to "Hello World"                  |    no     |
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

Javascript:

- nice work with the javascript file and using the semi-colon ";" at the end of the console.log statement. this is usually missed.

HTML:

- now, we just need to source the javascript file, ie, the helloWorld.js into the html file.
- put this <script src="./helloWorld.js"></script> element in the <head> section of the html file. this will source in the helloWorld.js file and you will see the consol.log("Hello World!"); in the Console tab in the chrome browser. any questions on this, feel free to ask.

- the image is unable to load. see if you can get an image from your local machine and copy into the images folder. use a relative path to the images folder, ie, like the <img> below:

```js
    <img src="../images/photo_1.jpg" alt="pixel art of Courteous bandit">
```

CSS:

- there are two footers at the end of the html file; one will do.

---

| General Items                  | Complete? |
| ------------------------------ | :-------: |
| The assignment repo was forked |    yes    |
| The correct repo was turned in |    yes    |
| GitHub config correct          |    yes    |
| More than 1 commit             |    yes    |
| Code is correctly formatted    |    no     |

---

### Notes:

This is good! I'd strongly recommend committing more often. Every time you get something new working (probably every 30 minutes or so), make a commit. You're saving your progress so that if something goes wrong, you can go back!

Great work!
