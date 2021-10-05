# Q.
Introduction

The first century spans from the year 1 up to and including the year 100, The second - from the year 101 up to and including the year 200, etc.

Task :

Given a year, return the century it is in.

Input , Output Examples :

1705 --> 18
1900 --> 19
1601 --> 17
2000 --> 20

# A)
```c
int centuryFromYear(int year) 
{
  return (year % 100 > 0 ? year/100 + 1 : year/100);
}
