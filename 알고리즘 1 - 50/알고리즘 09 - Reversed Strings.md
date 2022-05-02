# Q.
Complete the solution so that it reverses the string passed into it.

'world'  =>  'dlrow'

# A)
```js
function solution(str){
  let revStr = "";
  for (let i = 0; i < str.length; i++) {
    revStr += str[str.length - 1 - i]
  }
  return revStr;
}
```
