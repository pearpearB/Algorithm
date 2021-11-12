# Q.
Given two integers a and b, which can be positive or negative, find the sum of all the integers between and including them and return it. If the two numbers are equal return a or b.

Note: a and b are not ordered!

Examples (a, b) --> output (explanation)

(1, 0) --> 1 (1 + 0 = 1)\
(1, 2) --> 3 (1 + 2 = 3)\
(0, 1) --> 1 (0 + 1 = 1)\
(1, 1) --> 1 (1 since both are same)\
(-1, 0) --> -1 (-1 + 0 = -1)\
(-1, 2) --> 2 (-1 + 0 + 1 + 2 = 2)

# A)
```js
function getSum( a,b )
{
  let result = [];
  
  if (a > b)
    result = new Array(a - b + 1).fill();
  else
    result = new Array(b - a + 1).fill();
  result[0] = a;
  for (let i = 0; i < result.length; i++) {
    if (a > b)
      result[i] = a - i
    else
      result[i] = a + i
  } 
  return result.reduce((sum, cur) => sum + cur);
}
```
