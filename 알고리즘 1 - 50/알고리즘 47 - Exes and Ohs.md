# Q.
Check to see if a string has the same amount of 'x's and 'o's. The method must return a boolean and be case insensitive. The string can contain any char.

Examples input/output:

XO("ooxx") => true \
XO("xooxx") => false \
XO("ooxXm") => true \
XO("zpzpzpp") => true // when no 'x' and 'o' is present should return true \
XO("zzoo") => false

# A)
```js
function XO(str) {
  let arr = str.toLowerCase().split('');
  let count = arr.reduce((obj, el) => {
      if (el in obj) 
        obj[el] += 1;
      else 
        obj[el] = 1;
      return obj}, {});
  
  return count.x === count.o;
}
```
