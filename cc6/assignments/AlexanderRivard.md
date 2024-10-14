# Code Challenge 6 - Redux Sagas with Zookeeper (3)

---

| Functional Requirements                                                    | Complete? |
| -------------------------------------------------------------------------- | :-------: |
| Animals with Class Name displays on view                                   |    yes    |
| `rootSaga` function includes a `takeEvery` for action of 'GET_ZOO_ANIMALS' |    yes    |
| Generator function (with `*`) defined for `fetchAnimals`                   |    yes    |
| `takeEvery` calls `fetchAnimals()` function                                |    yes    |
| Saga uses `yield` with axios GET request                                   |    yes    |
| Saga uses `yield put` to dispatch GET response data to reducer             |    yes    |
| GET route query JOINs species with class table on `class_id`               |    yes    |
| GET route responds with data array from JOIN query                         |    yes    |

---

### Notes

---

| General Items                                           | Complete? |
| ------------------------------------------------------- | :-------: |
| More than 2 git commits descriptive of the changes made |    yes    |
| Code is consistently formatted                          |    yes    |
| Appropriate amount of code comments                     |    no     |

---

### Notes:

## Full Code Examples

### Fetch Saga

```js
// Your saga should listen for the action type of `GET_ZOO_ANIMALS`
function* rootSaga() {
  // YOUR CODE HERE
  yield takeEvery('GET_ZOO_ANIMALS', fetchAnimals);
}

// student saga function
function* fetchAnimals(action) {
  try {
    const response = yield axios.get('/zoo');
    yield put({ type: 'SET_ZOO_ANIMALS', payload: response.data });
  } catch (error) {
    console.log('error with animals get request', error);
  }
}
```

### JOIN

```sql
SELECT species.*, class.class_name FROM species
JOIN class ON species.class_id = class.id;
```
