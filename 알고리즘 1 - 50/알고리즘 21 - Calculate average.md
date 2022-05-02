# Q.
Write a function which calculates the average of the numbers in a given list.

Note: Empty arrays should return 0.

# A)
```js
function find_average(array) {
  if (array.length === 0)
    return 0;
  return array.reduce((sum, cur) => sum + cur)/array.length
}
```
