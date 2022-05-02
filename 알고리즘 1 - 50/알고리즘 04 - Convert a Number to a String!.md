# Q.
Description:

We need a function that can transform a number into a string.

What ways of achieving this do you know?

In C, return a dynamically allocated string that will be freed by the test suite.

Examples:

123 --> "123" \
999 --> "999"

# A)
```c
#include <stdlib.h>

const char* number_to_string(int number) {
  int nbr = number;
  int len = 0;
  
  if (nbr < 0)
  {
    nbr *= -1;
    len += 1;
  }
  while (nbr > 0)
  {
    nbr /= 10;
    len++;
  }
  
  char *strnum = malloc(sizeof(char) * len + 1);
  strnum[len] = '\0';
  
  if (number == 0)
    strnum[0] = '0';
  else if (number < 0)
  {
    strnum[0] = '-';
    number *= -1;
  }
  while (number > 0)
  {
    strnum[--len] = number % 10 + '0';
    number /= 10;
  }
  return (strnum);
}
