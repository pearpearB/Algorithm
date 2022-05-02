# Q.

Consider an array/list of sheep where some sheep may be missing from their place. We need a function that counts the number of sheep present in the array (true means present).

For example,

[true,  true,  true,  false,\
  true,  true,  true,  true ,\
  true,  false, true,  false,\
  true,  false, false, true ,\
  true,  true,  true,  true ,\
  false, false, true,  true]\
The correct answer would be 17.

Hint: Don't forget to check for bad values like null/undefined

# A)
```js
function countSheeps(arrayOfSheep) {
  let count = 0;
  if (arrayOfSheep === null)
    return 0;
  else {
    for (let el of arrayOfSheep)
      if (el === true)
        count++;
  }
  return count;
}
```
