# Q.
Build a function that returns an array of integers from n to 1 where n>0.

Example : n=5 --> [5,4,3,2,1]

# A)
```js
const reverseSeq = n => {
  let buf = [];
  
  for (let i = 0; i < n; i++)
    buf.push(n - i);
  return buf;
};
```
