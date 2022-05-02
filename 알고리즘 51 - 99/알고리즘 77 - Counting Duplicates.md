# Q.
Count the number of Duplicates

Write a function that will return the count of distinct case-insensitive alphabetic characters and numeric digits that occur more than once in the input string. The input string can be assumed to contain only alphabets (both uppercase and lowercase) and numeric digits.

Example

"abcde" -> 0 # no characters repeats more than once\
"aabbcde" -> 2 # 'a' and 'b'\
"aabBcde" -> 2 # 'a' occurs twice and 'b' twice (`b` and `B`)\
"indivisibility" -> 1 # 'i' occurs six times\
"Indivisibilities" -> 2 # 'i' occurs seven times and 's' occurs twice\
"aA11" -> 2 # 'a' and '1'\
"ABBA" -> 2 # 'A' and 'B' each occur twice\
# A)
```js
function duplicateCount(text){
  let arrObj = text.toLowerCase().split('').reduce((obj, el) => {
    if (el in obj) obj[el] += 1;
    else obj[el] = 1;
    return obj;
  }, {})
  
  let count = 0;
  for (let el in arrObj) {
    if (arrObj[el] > 1)
      count++;
  }
  
  return count;
}
```
# other)
`.indexOf()`와 `.lastIndexOf()`를 활용해 한번 이상 쓰인 글자를 알아낼 수도 있다!
```js
function duplicateCount(text){
  return text.toLowerCase().split('').filter(function(val, i, arr){
    return arr.indexOf(val) !== i && arr.lastIndexOf(val) === i;
  }).length;
}
```
