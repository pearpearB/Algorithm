# Q.
Create a function that takes an integer as an argument and returns "Even" for even numbers or "Odd" for odd numbers.

# A)
```c
const char * even_or_odd(int number) {
  if((number % 2) == 0)
    return "Even";
  else
    return "Odd";
}
