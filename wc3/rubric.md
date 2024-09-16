# Weekend 9 Challenge - SQL ToDo App

## Base Required Features

All base features must be implemented for score of _3 - Meets Expectations_

<details>
  <summary>Expand for Details</summary>

- Database:

  - [ ] Includes `database.sql` file to create database
  - [ ] Database is named `weekend-to-do-app`
  - [ ] Appropriate names used for table & columns
  - [ ] Appropriate database types used for columns

- Initial Display:

  - [ ] UI to create Task
  - [ ] All existing Tasks shown
    - [ ] Each Task has an option to Complete
    - [ ] Completed Tasks are styled to be visually different
    - [ ] Each Task has an option to Delete

- Client code:

  - [ ] Axios GET request to get all tasks
  - [ ] Axios POST request to add a tasks
  - [ ] Axios PUT request to complete a task, jQuery data for id
  - [ ] Axios DELETE request to remove a task, jquery data for id

- Server code:
  - [ ] Express Setup
  - [ ] PG Setup (`pool.js` module optional but should be recommended if not used)
  - [ ] Routes setup (router module optional but should be recommended if not used)
    - [ ] GET route to select all Tasks, SQL SELECT (recommend ORDER BY if not used)
    - [ ] POST route to add a Task, SQL Insert must use query parameters for values
    - [ ] PUT route to complete a Task, id for update should come from request parameters, value from request body
    - [ ] DELETE route to remove a Task, id for delete should come from request parameters

## General Items

Feedback should be provided for these items, but they do not impact scoring.

- Git
  - [ ] Multiple git commits showing incremental progress
  - [ ] Commits are descriptive of the changes made or feature added
  - [ ] Has .gitignore with node_modules
  - [ ] Readme file updated (assuming this is previously discussed)
- Code Style
  - [ ] Appropriate amount of code comments
  - [ ] Code is consistently formatted
- Client
  - [ ] Appropriate use of HTML tags
  - [ ] Basic CSS styling with margins/padding

</details>

---

## Stretch Goals

All must be complete for score of _5 - Exceeds Expectations_

- [ ] Git Branching for stretch features, merged with `--no-ff`
- [ ] Styling with Bootstrap
- [ ] Confirm before delete
- [ ] Order completed tasks to the bottom of the page

---

## Markdown Template

```

Hey ___. General comment about the project.

---
| Functional Requirements | Complete? |
| --- | :---: |
| Includes `database.sql` file to create database | no |
| Displays all existing tasks on load | no |
| Form to create a task & add it to database | no |
| Ability to complete a task | no |
| Completed tasks are visually styled differently | no |
| Ability to delete a task & remove it from database | no |
| STRETCH: Using Git Branches for stretch features | no |
| STRETCH: Styling with Bootstrap or 3rd party library | no |
| STRETCH: Confirmation Alert before Delete | no |
| STRETCH: Order completed tasks to the bottom of the page | no |

---
### Notes:

Notes on items above.

---
| General Items | Complete? |
| --- | :---: |
| More than 10 git commits | no |
| Commits are descriptive of the changes made or feature added | no |
| Readme file updated | no |
| Appropriate amount of code comments | no |
| Code is consistently formatted | no |
| SQL commands use placeholders (`$1, $2, $3`), to prevent injection attacks | no |

---
### Notes:

The above items are things that employers will look for when browsing your GitHub page. I would recommend going back and adding more code comments and updating the README to include a description of the project in your own words.
```

---

## Feedback Snippets

### Page reloads on Form submission

You may have noticed that the "Submit Task" button causes the whole page to _flash_, and sometimes the new task doesn't show up. This is actually the page reloading! Sometimes this happens so fast that your AJAX request doesn't have a chance to complete, and the new item is not created.

This happens when you use `<form>` elements in your HTML. The default behavior of HTML forms is to redirect the user to wherever the `action` property specifies, eg:

```html
<form action="nextPage.html"></form>
```

In your case, there's not an `action` property, so it "redirects" to the same page. Regardless, we don't want it to redirect at all -- we want our JS code to handle the form submission, and send data to our server via AJAX. This take an extra line of code in your form event handler:

```js
function addTask(event) {
  event.preventDefault();

  //...
}
```

Voila!

### SQL Data Types

Let's look at your DB setup:

```sql
CREATE TABLE "todo" (
	"id" SERIAL PRIMARY KEY,
	"task" VARCHAR(70) NOT NULL,
	"notes" VARCHAR(100) NOT NULL,
	"dueDate" VARCHAR(70),
	"complete" VARCHAR
);
```

I notice that all your fields are setup as `VARCHAR`, the SQL equivalent of a string. SQL has built-in data types, just like javascript does -- take advantage of them! Here's how I'd setup the same DB, using postgres data types:

```sql
CREATE TABLE "todo" (
	"id" SERIAL PRIMARY KEY,
	"task" VARCHAR(70) NOT NULL,
	"notes" VARCHAR(100) NOT NULL,
	-- The TIMESTAMP data type is great for storing dates.
	-- The node pg library will convert these to native JS `Date` types.
	-- See https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date
	"dueDate" TIMESTAMP,
	-- "complete" can either be true of false -- sounds like a boolean to me!
	-- Again, pg will convert these to a native js Boolean type,
	-- making these values easier to work with client-side
	"complete" BOOLEAN
);
```

This will prevent invalid data from getting into your database, and allow you to use `boolean` and `Date` objects in your server/client JS code.
