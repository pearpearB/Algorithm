# Q.
An isogram is a word that has no repeating letters, consecutive or non-consecutive. Implement a function that determines whether a string that contains only letters is an isogram. Assume the empty string is an isogram. Ignore letter case.

"Dermatoglyphics" --> true\
"aba" --> false\
"moOse" --> false (ignore letter casing)

# A)
```js
function isIsogram(str){
  for (let i = 0; i < str.length; i++) {
    for (let j = i + 1; j < str.length; j++) {
      if (str[i] === str[j].toUpperCase() || str[i] === str[j].toLowerCase())
        return false;
    }
  }
  return true;
}
```
