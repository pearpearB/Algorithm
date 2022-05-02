# Q.
In this little assignment you are given a string of space separated numbers, and have to return the highest and lowest number.

Examples

highAndLow("1 2 3 4 5");  // return "5 1" \
highAndLow("1 2 -3 4 5"); // return "5 -3" \
highAndLow("1 9 3 4 -5"); // return "9 -5"

# A)
```js
function highAndLow(numbers){
  let arrnum = numbers.split(' ').map(el => Number(el));
  
  let min = Math.min(...arrnum);
  let max = Math.max(...arrnum);
  
  return `${max} ${min}`;
}
```
