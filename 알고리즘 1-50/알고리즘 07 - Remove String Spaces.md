# Q.
Simple, remove the spaces from the string, then return the resultant string.

For C, you must return a new dynamically allocated string.

# A)
```c
#include <stdlib.h>

char *no_space(const char *str_in) {
  int len = 0;
  while (str_in[len] != '\0')
    len++;
  char *result = malloc(sizeof(char) * len + 1);
  int i = 0;
  int j = 0;
  while (str_in[i] != '\0')
  {
    if (str_in[i] == ' ')
      i++;
    else
     result[j++] = str_in[i++];
  }
  while (j <= len)
    result[j++] = '\0';
  return (result);
}
