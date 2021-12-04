# Q.
Complete the function that accepts a string parameter, and reverses each word in the string. All spaces in the string should be retained.

Examples

"This is an example!" ==> "sihT si na !elpmaxe"\
"double  spaces"      ==> "elbuod  secaps"

# A)
```js
function reverseWords(str) {
  return str.split(' ').map(el => {
    let buf = "";
    for(let i = 0; i < el.length; i++) {
        buf += el[el.length - 1 - i];
    }
    return buf;
}).join(' ');
}
```
