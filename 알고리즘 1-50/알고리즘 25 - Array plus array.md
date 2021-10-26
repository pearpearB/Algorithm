# Q.
I'm new to coding and now I want to get the sum of two arrays...actually the sum of all their elements. I'll appreciate for your help.

P.S. Each array includes only integer numbers. Output is a number too.

# A)
```js
function arrayPlusArray(arr1, arr2) {
  return arr1.reduce((sum, i)=> sum + i)+arr2.reduce((sum, i)=> sum + i)
}
```
