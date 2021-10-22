# Q.
Given a string of digits, you should replace any digit below 5 with '0' and any digit 5 and above with '1'. Return the resulting string.

# A)
```js
function fakeBin(x){
  let result = '';
  
  for (let el of x) {
    if (el < '5')
      result += '0';
    else
      result += '1';
  }
  return result;
}
```
