
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


[For coloured code formatting click here]()

--------------------------------------------------------------------------------------------------------------------------------


 
