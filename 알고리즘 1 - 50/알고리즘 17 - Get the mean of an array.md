# Q.
t's the academic year's end, fateful moment of your school report. The averages must be calculated. All the students come to you and entreat you to calculate their average for them. Easy ! You just need to write a script.

Return the average of the given array rounded down to its nearest integer.

The array will never be empty.

# A)
```js
function getAverage(marks){
  let result = 0;
  
  for (let el of marks)
    result += el;
  
  return Math.floor(result/marks.length)
}
```

