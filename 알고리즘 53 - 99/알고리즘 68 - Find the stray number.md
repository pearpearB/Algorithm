# Q.
You are given an odd-length array of integers, in which all of them are the same, except for one single number.

Complete the method which accepts such an array, and returns that single different number.

The input array will always be valid! (odd-length >= 3)

Examples

[1, 1, 2] ==> 2\
[17, 17, 3, 17, 17, 17, 17] ==> 3

# A)
```js
function stray(numbers) {
  let numObj = numbers.reduce((obj, el) => {
    if (el in obj) obj[el] += 1;
    else obj[el] = 1;
    return obj;
  }, {});
  for (let el in numObj)
    if (numObj[el] === 1)
      return Number(el);
}
```

