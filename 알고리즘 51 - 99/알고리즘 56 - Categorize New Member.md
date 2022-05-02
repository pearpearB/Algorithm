# Q.
To be a senior, a member must be at least 55 years old and have a handicap greater than 7. In this croquet club, handicaps range from -2 to +26; the better the player the lower the handicap.

Input

Input will consist of a list of lists containing two items each. Each list contains information for a single potential member. Information consists of an integer for the person's age and an integer for the person's handicap.
```
Note for F#: The input will be of (int list list) which is a List<List>
```
Example Input

[[18, 20],[45, 2],[61, 12],[37, 6],[21, 21],[78, 9]]
Output

Output will consist of a list of string values (in Haskell: Open or Senior) stating whether the respective member is to be placed in the senior or open category.

Example Output

["Open", "Open", "Senior", "Open", "Open", "Senior"]
  
# A)
```js
function openOrSenior(data){
  let result = [];
  for (let el of data) {
    if (el[0] >= 55 && el[1] > 7)
      result.push("Senior");
    else
      result.push("Open");
  }
  return result;
}
```
