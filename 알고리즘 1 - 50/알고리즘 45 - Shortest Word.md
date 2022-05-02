# Q.
Simple, given a string of words, return the length of the shortest word(s).

String will never be empty and you do not need to account for different data types.

# A)
```js
function findShort(s){
  return s.split(' ').reduce((min, cur) => {
    if (min > cur.length)
      min = cur.length;
    return min;
  }, 2147483647);
}
```
