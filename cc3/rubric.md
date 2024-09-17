Hey STUDENT,

---

| Functional Requirements                                 | Complete? |
| ------------------------------------------------------- | :-------: |
| GET route returns treats data                           |    no     |
| POST route adds new treat & returns 2XX status code     |    no     |
| PUT route updates description & returns 2XX status code |    no     |
| DELETE route removes a treat & returns 2XX status code  |    no     |
| Queries use prepared statements ie: $1, $2 etc          |    no     |

---

### Notes:

---

| General Items                                             | Complete? |
| --------------------------------------------------------- | :-------: |
| Database is setup with the correct db name and table name |    no     |
| query .catch sends 500 status                             |    no     |
| Has routing modules on the server                         |    no     |
| More than 2 git commits descriptive of the changes made   |    no     |
| Code is consistently formatted                            |    no     |
| Appropriate amount of code comments                       |    no     |

---

### Notes:

// Note we're using the same endpoint as `GET /treats`,
// because our URL hasn't changed. We're just adding
// support for query strings to an _existing_ URL
router.get('/', (req, res) => {
let queryText, queryParams;

    // If we have a `?q=` query parameter,
    // do a LIKE (wildcard) search
    if (req.query.q) {
        queryText = `
            SELECT * FROM "treats"
            WHERE name ILIKE $1
        `;
        queryParams = [`%${req.query.q}%`]
    }
    // Otherwise, select all treats
    else {
        queryText = `SELECT * FROM "treats"`;
        queryParams = [];
    }

    pool.query(queryText, queryParams)
        .then(response => {
            console.log('Successful GET: ', response);
            res.send(response.rows)
        })
        .catch(err => {
            console.log('Error on GET from DB: ', err);
            res.sendStatus(500);
        })

});
