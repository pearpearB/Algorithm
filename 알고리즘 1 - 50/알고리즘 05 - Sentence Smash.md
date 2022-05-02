# Q.
Sentence Smash

Write a function that takes an array of words and smashes them together into a sentence and returns the sentence. You can ignore any need to sanitize words or add punctuation, but you should add spaces between each word. Be careful, there shouldn't be a space at the beginning or the end of the sentence!

Example

['hello', 'world', 'this', 'is', 'great']  =>  'hello world this is great'

# A)
```c
#include <string.h>
#include <stdlib.h>

char *smash(const char **words, size_t count) {
  
  int len = 0;
  size_t i = 0;
  
  while (i < count)
    len += strlen(words[i++]);
  
  char *result = malloc(sizeof(char) * (len + i));
  size_t j = 0;
  int y = 0;
  
  while (j < count)
  {
    int z = 0;
    while (words[j][z] != '\0')
      result[y++] = words[j][z++];
    if (j++ + 1 < count)
      result[y++] = ' ';
  }
  result[y] = '\0';
  return (result);
}
