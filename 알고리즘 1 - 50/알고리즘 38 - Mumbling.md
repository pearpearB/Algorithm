# Q.
This time no story, no theory. The examples below show you how to write function accum:

Examples:

accum("abcd") -> "A-Bb-Ccc-Dddd" \
accum("RqaEzty") -> "R-Qq-Aaa-Eeee-Zzzzz-Tttttt-Yyyyyyy" \
accum("cwAt") -> "C-Ww-Aaa-Tttt"

# A)
```js
function accum(s) {
	let result = "";
  
  for (let i = 0; i < s.length; i++) {
    result += s[i].toUpperCase();
    for (let j = 0; j < i; j++) {
      result += s[i].toLowerCase();
    }
    if (i + 1 < s.length) {
      result += '-'
    }
  }
  return result;
}
```
