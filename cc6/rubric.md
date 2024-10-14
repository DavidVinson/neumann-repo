# Code Challenge 6 - Redux Sagas with Zookeeper

---

| Functional Requirements                                                    | Complete? |
| -------------------------------------------------------------------------- | :-------: |
| Animals with Class Name displays on view                                   |    no     |
| `rootSaga` function includes a `takeEvery` for action of 'GET_ZOO_ANIMALS' |    no     |
| Generator function (with `*`) defined for `fetchAnimals`                   |    no     |
| `takeEvery` calls `fetchAnimals()` function                                |    no     |
| Saga uses `yield` with axios GET request                                   |    no     |
| Saga uses `yield put` to dispatch GET response data to reducer             |    no     |
| GET route query JOINs species with class table on `class_id`               |    no     |
| GET route responds with data array from JOIN query                         |    no     |

---

### Notes

---

| General Items                                           | Complete? |
| ------------------------------------------------------- | :-------: |
| More than 2 git commits descriptive of the changes made |    no     |
| Code is consistently formatted                          |    no     |
| Appropriate amount of code comments                     |    no     |

---

### Notes:

## Full Code Examples

### Fetch Saga

```
// Your saga should listen for the action type of `GET_ZOO_ANIMALS`
function* rootSaga() {
    // YOUR CODE HERE
    yield takeEvery('GET_ZOO_ANIMALS', fetchAnimals);
}

// student saga function
function* fetchAnimals(action) {
    try {
      const response = yield axios.get('/zoo');
      yield put( {type: 'SET_ZOO_ANIMALS', payload: response.data} );
    }
    catch (error) {
      console.log('error with animals get request', error);
    }
}
```

### JOIN

```
SELECT species.*, class.class_name FROM species
JOIN class ON species.class_id = class.id;
```
