
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




### Q3. Write a program that generates the following output:
### 10
### 20
### 19
### Use an integer constant for the 10, an arithmetic assignment operator to generate the 20,
### and a decrement operator to generate the 19.


### Solution:


#### Given,

#### It wants use to use an interger constant so just use int num
#### For arithmetic assignment operator we can use on of the following += -= *= etc. Basically we will use *= because we need to generate 20 from interger constant. 
#### Finally, use the -- operator to decrement int num to 19.


```C++

#include <iostream>

using namespace std;

int main()
{
  int num = 10;
  
  cout << num << endl;
  
  num *= 2;
  
  cout << num << endl;
  cout << --num << endl;
  
  return 0;
}
```



--------------------------------------------------------------------------------------------------------------------------------




### Q4. Write a program that displays your favorite poem. Use an appropriate escape sequence
### for the line breaks. If you don’t have a favorite poem, you can borrow this one by Ogden
### Nash:
### Candy is dandy,
### But liquor is quicker.


### Solution:

#### Given,

#### 1. No I do not have a favorite poem so I'll be using the one given to me. 
#### 2. An appropriate escape sequence for this would be \n(called new line or new feed). So, I'll use that for the above string literals.

```C++

#include <iostream>
using namespace std;

int main()
{
  cout << "Candy is dandy,\n" << endl
       << "But liquor is quicker." << endl;
  
  return 0;   
}
```


--------------------------------------------------------------------------------------------------------------------------------




### Q5. A library function, islower(), takes a single character (a letter) as an argument and
### returns a nonzero integer if the letter is lowercase, or zero if it is uppercase. This function requires the header file 
### CTYPE.H. Write a program that allows the user to enter a letter, and then displays either zero or nonzero, depending on 
### whether a lowercase or
### uppercase letter was entered. (See the SQRT program for clues.)


### Solution:

#### No need to analyze this program's prerequisites, because it's a very easy problem.

```C++
#include <iostream>
using namespace std;

int main()
{
  cout << "Candy is dandy,\n" << endl
       << "But liquor is quicker." << endl;
  
  return 0;   
}
```



--------------------------------------------------------------------------------------------------------------------------------




