# Q.
The goal of this exercise is to convert a string to a new string where each character in the new string is "(" if that character appears only once in the original string, or ")" if that character appears more than once in the original string. Ignore capitalization when determining if a character is a duplicate.

Examples
```js
"din"      =>  "((("
"recede"   =>  "()()()"
"Success"  =>  ")())())"
"(( @"     =>  "))((" 
```
# A)
```js
function duplicateEncode(word){
  let result = "";
  let newWord = word.toLowerCase();
  for (let i = 0; i < newWord.length; i++) {
    if ((newWord.slice(0, i)+newWord.slice(i + 1, newWord.length)).includes(newWord[i]) === true)
      result += ')'
    else
      result += '('
  }
  return result;
}
```

# other)
```js
function duplicateEncode(word){
  return word
    .toLowerCase()
    .split('')
    .map( function (a, i, w) {
      return w.indexOf(a) == w.lastIndexOf(a) ? '(' : ')'
    })
    .join('');
}
```
