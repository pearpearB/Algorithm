# Q.
Take 2 strings s1 and s2 including only letters from ato z. Return a new sorted string, the longest possible, containing distinct letters - each taken only once - coming from s1 or s2.

Examples:

a = "xyaabbbccccdefww"\
b = "xxxxyyyyabklmopq"\
longest(a, b) -> "abcdefklmopqwxy"

a = "abcdefghijklmnopqrstuvwxyz"\
longest(a, a) -> "abcdefghijklmnopqrstuvwxyz"

# A)
```js
function longest(s1, s2) {
  let s1s2Obj = (s1+s2).split('').reduce((obj, el) => {
    if (el in obj) obj[el] += 1;
    else obj[el] = 1;
    return obj;}, {});
  return Object.keys(s1s2Obj)
    .sort()
    .join('');
}
```
