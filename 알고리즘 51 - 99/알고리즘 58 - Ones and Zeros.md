# Q.
Given an array of ones and zeroes, convert the equivalent binary value to an integer.

Eg: [0, 0, 0, 1] is treated as 0001 which is the binary representation of 1.

Examples:

Testing: [0, 0, 0, 1] ==> 1\
Testing: [0, 0, 1, 0] ==> 2\
Testing: [0, 1, 0, 1] ==> 5\
Testing: [1, 0, 0, 1] ==> 9\
Testing: [0, 0, 1, 0] ==> 2\
Testing: [0, 1, 1, 0] ==> 6\
Testing: [1, 1, 1, 1] ==> 15\
Testing: [1, 0, 1, 1] ==> 11

# A)
```js
const binaryArrayToNumber = arr => {
  let newArr = arr.reverse();
  
  let sum = 0;
  for (let i = 0; i < newArr.length; i++) {
    if (i === 0 && newArr[i] === 1)
      sum += 1;
    else if (newArr[i] === 1)
      sum += Math.pow(2, i);
    else
      sum += 0;
  }
  return sum;
};
```
