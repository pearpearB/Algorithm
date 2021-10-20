# Q.
Write a function to convert a name into initials. This kata strictly takes two words with one space in between them.

The output should be two capital letters with a dot separating them.

It should look like this:

Sam Harris => S.H

patrick feeney => P.F

# A)
```js
function abbrevName(name){
  let nameSplit = name.split(' ');
  let initial = [];
  
  for (el of nameSplit) {
    initial += el[0];
  }
  initial = initial.split('').join('.').toUpperCase();
  
  return initial;
}
```
