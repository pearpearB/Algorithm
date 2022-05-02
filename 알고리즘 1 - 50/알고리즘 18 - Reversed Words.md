# Q.
Complete the solution so that it reverses all of the words within the string passed in.

Example:

"The greatest victory is that which requires no battle" --> "battle no requires which that is victory greatest The"

# A)
```js
function reverseWords(str){
  let arrStr = str.split(' ');
  let result = [];
  
  for (let i = 0; i < arrStr.length; i++)
    result[i] = arrStr[arrStr.length - 1 - i]
  
  return result.join(' ')
}
```
