
###  Exercise 2.1 Assuming there are 7.481 gallons in a cubic foot, write a program that asks a user in enter a number of gallons, and then displays the equivalent in cubic feet. 

### Solution.

Given,

#### 1 gallon = 1/7.481 cubic feet or 1 gallon ≈ 0.134 cubic feet
#### Or 1 gallon = 0.134 cubic feet(approx)
#### input required in gallons
#### output should be in cubic feet


```C++ 
#include <iostream>
using namespacestd;
  
int main()
{
  float gallons;
  float cfeet;
  const float multiplier = 0.134F;
  
  cout << "Please enter volume in gallons: ";
  cin << gallons;
  
  cfeet = gallons * multiplier;
  
  cout << "Equivalent volume in cubic feet is: ";
  cout << cfeet << endl;
  
  return 0;
}
```


[For coloured code formatting click here](https://github.com/devanshusinghgithub/devanshusinghgithub.github.io/blob/master/_posts/2017-3-5-Chapter-2-Programming-Problems.md)



--------------------------------------------------------------------------------------------------------------------------------



### Q2 Write a program that generates the following table:
### 1990     135
### 1991    7290
### 1992   11300
### 1993   16200
### Use a single cout statement for all output
 
### Solution:

#### Given;
#### 1. We have to use the set width manipulator. Don't forget to include iomanip header file.
#### 2. We only need to use setw() on the right sided list and not the years.
#### 3. Unlike the example in the chapter there is no need to use long type. There is no need to inialize the integers in the question either.
#### 4. We need to cascade cout. Use endl to flush the output stream.


```C++
#include <iostream>
#include <iomanip>

using namespace std;

int main()
{
  cout << 1990 << setw(8) << 135 << endl
       << 1991 << setw(8) << 7290 << endl
       << 1992 << setw(8) << 11300 << endl
       << 1993 << setw(8) << 16200 << endl;
return 0;
}
```



--------------------------------------------------------------------------------------------------------------------------------




