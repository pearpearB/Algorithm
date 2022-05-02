# Q.
Given an array of integers your solution should find the smallest integer.

For example:

Given [34, 15, 88, 2] your solution will return 2
Given [34, -345, -1, 100] your solution will return -345
You can assume, for the purpose of this kata, that the supplied array will not be empty.

# A)
```c
#include <stddef.h>

int find_smallest_int(int *vec, size_t len) {
  int min = 2147483647;
  size_t i = 0;
  
  while (i < len)
  {
    if (vec[i] <= min)
      min = vec[i];
    i++;
  }
  return (min);
}
