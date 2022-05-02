# Q.
Return the number (count) of vowels in the given string.

We will consider a, e, i, o, u as vowels for this Kata (but not y).

The input string will only consist of lower case letters and/or spaces.
# A)
```js
function getCount(str) {
  var vowelsCount = 0;
  const arr = ['a', 'e', 'i', 'o', 'u'];
  
  for (el of str){
    for (vowel of arr) {
      if (el === vowel)
        vowelsCount++;
    }
  } 
  return vowelsCount;
}
```
