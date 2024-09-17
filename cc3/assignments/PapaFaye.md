Hey Papa, (1)

---

| Functional Requirements                                 | Complete? |
| ------------------------------------------------------- | :-------: |
| GET route returns treats data                           |    yes    |
| POST route adds new treat & returns 2XX status code     |    yes    |
| PUT route updates description & returns 2XX status code |    yes    |
| DELETE route removes a treat & returns 2XX status code  |    yes    |
| Queries use prepared statements ie: $1, $2 etc          |  partial  |

---

### Notes:

---

| General Items                                             | Complete? |
| --------------------------------------------------------- | :-------: |
| Database is setup with the correct db name and table name |    no     |
| query .catch sends 500 status                             |    yes    |
| Has routing modules on the server                         |    yes    |
| More than 2 git commits descriptive of the changes made   |    no     |
| Code is consistently formatted                            |    yes    |
| Appropriate amount of code comments                       |    no     |

---

### Notes:

- PUT endpoint:

```js
// PUT
router.put('/:id', (req, res) => {
  const reqId = req.params.id;
  const queryText = `UPDATE "treats" SET "description"=$2 WHERE "id"=$1 RETURNING *`;
  console.log(req.body);
  pool
    .query(queryText, [reqId, req.body.description])
    .then(() => res.sendStatus(200))
    .catch((error) => {
      console.error(`Updating error`, error);
      res.sendStatus(500);
    });
});
```

// Note we're using the same endpoint as `GET /treats`,
// because our URL hasn't changed. We're just adding
// support for query strings to an _existing_ URL

```js
router.get('/', (req, res) => {
  let queryText, queryParams;

  // If we have a `?q=` query parameter,
  // do a LIKE (wildcard) search
  if (req.query.q) {
    queryText = `
            SELECT * FROM "treats"
            WHERE name ILIKE $1
        `;
    queryParams = [`%${req.query.q}%`];
  }
  // Otherwise, select all treats
  else {
    queryText = `SELECT * FROM "treats"`;
    queryParams = [];
  }

  pool
    .query(queryText, queryParams)
    .then((response) => {
      console.log('Successful GET: ', response);
      res.send(response.rows);
    })
    .catch((err) => {
      console.log('Error on GET from DB: ', err);
      res.sendStatus(500);
    });
});
```
