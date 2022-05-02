# Q.
Given an array of integers, find the one that appears an odd number of times.

There will always be only one integer that appears an odd number of times.

Examples

[7] should return 7, because it occurs 1 time (which is odd).\
[0] should return 0, because it occurs 1 time (which is odd).\
[1,1,2] should return 2, because it occurs 1 time (which is odd).\
[0,1,0,1,0] should return 0, because it occurs 3 times (which is odd).\
[1,2,2,3,3,3,4,3,3,3,2,2,1] should return 4, because it appears 1 time (which is odd).

# A)
```js
function findOdd(A) {
  let newObj = A.reduce((obj, el) => {
    if (el in obj) obj[el] += 1;
    else obj[el] = 1;
    return obj;
  }, {})
  
  for (let el in newObj) {
    if (newObj[el] % 2 === 1)
      return Number(el);
  }
  return 0;
}
```
