# Q.
Your goal in this kata is to implement a difference function, which subtracts one list from another and returns the result.

It should remove all values from list a, which are present in list b keeping their order.

arrayDiff([1,2],[1]) == [2]\
If a value is present in b, all of its occurrences must be removed from the other:

arrayDiff([1,2,2,2,3],[2]) == [1,3]

# A)
```js
function arrayDiff(a, b) {
  if (b.length < 1)
    return a;
  
  let i = 0;
  let j = 0;
  let result = [];
for (let i of a) {
  let flag = 1;
  for (let j of b) {
    if (i === j)
      flag = 0;
  }
  if (flag === 1)
    result.push(i);
}
  return result;
}
```

# other)
```js
function array_diff(a, b) {
  return a.filter(e => !b.includes(e));
}
```
