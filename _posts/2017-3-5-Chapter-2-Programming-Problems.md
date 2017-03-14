
## The following are solutions to problems of Chapter 2 of Object Oriented Programming in C++ by Robert Lafore.
## Please click the link below for coloured formatting for better legibility, otherwise continue reading. 

[For coloured code formatting click here](https://github.com/devanshusinghgithub/devanshusinghgithub.github.io/blob/master/_posts/2017-3-5-Chapter-2-Programming-Problems.md)


--------------------------------------------------------------------------------------------------------------------------------



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




### Q5. A library function, islower(), takes a single character (a letter) as an argument and
### returns a nonzero integer if the letter is lowercase, or zero if it is uppercase. This function requires the header file  ### CTYPE.H. Write a program that allows the user to enter a letter, and then displays either zero or nonzero, depending on
### whether a lowercase or uppercase letter was entered.


### Solution.

#### Given

#### We have to use islower() function, which requires header file named CTYPE.H to take a letter as an agrument and tell us if it's lowercase or uppercase.
#### Again this is one of those programs that require pseudocode for explanation.

### Important Note : I did this question after completing the first three chapters, which means that I do know the use of if----else statment, but this question is for chapter two, and therefore I'm not using if----else, which would make it a better program. The reason for this is that I want to show structered progression in my ability. 


```C++

#include <iostream>
#include <ctype.h>                              //For islower()

using namespace std;

int main()

{
    char letter;
    int answer;                                 //Because the funtion islower() returns an interger value
    
    cout << "Please Enter a letter: ";          //Ask for a letter from user for input
    cin >> letter;                              //Assign the variable 'letter' to input
    
    answer = islower(letter);                   //Use the islower() function
    
    cout << "The letter is: " << answer << endl; //If non-zero integer is the output then the letter us lowercase.
                                                 //If zero is returned then it's lowercase.
    return 0;
    
}
```


--------------------------------------------------------------------------------------------------------------------------------



### Q6. On a certain day the British pound was equivalent to $1.487 U.S., the French franc was
### $0.172, the German deutschemark was $0.584, and the Japanese yen was $0.00955.
### Write a program that allows the user to enter an amount in dollars, and then displays this
### value converted to these four other monetary units.


#### Solution:


```C++
#include <iostream>
using namespace std;

int main()
{
    double  gbp, fra, ger, yen;
    double  usd;
    
    gbp = 0.672;
    fra = 5.813;7. 
    ger = 1.712;
    yen = 104.712;
    
    cout << "Please enter amount in USD: ";
    cin >> usd;
    
    cout << "Equivalent amount in Great Britain Pound is: " << usd * gbp << endl;
    cout << "Equivalent amount in Franc is: " << usd * fra << endl;
    cout << "Equivalent amount in German Mark is: " << usd * ger << endl;
    cout << "Equivalent amount in Japanese Yen is: " << usd * yen << endl;

    return 0;
}
```


--------------------------------------------------------------------------------------------------------------------------------


### Q7. If you have two fractions, a/b and c/d, their sum can be obtained from the formula
### a/b + c/d = a*d+b*c/b*d
### For example, 1/4 plus 2/3 is 11/12
### Write a program that encourages the user to enter two fractions, and then displays their
### sum in fractional form. (You don’t need to reduce it to lowest terms.) The interaction
### with the user might look like this:
### Enter first fraction: 1/2
### Enter second fraction: 2/5
### Sum = 9/10
### You can take advantage of the fact that the extraction operator (>>) can be chained to
### read in more than one quantity at once:
### cin >> a >> dummychar >> b;


#### Solution

```C++
#include<iostream>
using namespace std;

int main()
{
 int a,b,c,d;
 char slash;
 
 cout << "Enter first fraction: ";
 cin >> a >> slash >> b;
 cout << "Enter second fraction: ";
 cin >> c >> slash >> d;
 
 
 cout << "The sum of the two fractions is " << (a * d) + (b * c) << "/" << b * d << endl;
 
 return 0;
}
```


--------------------------------------------------------------------------------------------------------------------------------


### Q8. In the heyday of the British empire, Great Britain used a monetary system based on
### pounds, shillings, and pence. There were 20 shillings to a pound, and 12 pence to a
### shilling. The notation for this old system used the pound sign, £, and two decimal points,
### so that, for example, £5.2.8 meant 5 pounds, 2 shillings, and 8 pence. (Pence is the plural
### of penny.) The new monetary system, introduced in the 1950s, consists of only pounds
### and pence, with 100 pence to a pound (like U.S. dollars and cents). We’ll call this new
### system decimal pounds. Thus £5.2.8 in the old notation is £5.13 in decimal pounds (actually £5.1333333). Write a program to convert the old pounds-shillings-pence format to
### decimal pounds. An example of the user’s interaction with the program would be
### Enter pounds: 7
### Enter shillings: 17
### Enter pence: 9
### Decimal pounds = £7.89
### In most compilers you can use the decimal number 156 (hex character constant ‘\x9c’)
### to represent the pound sign (£). In some compilers, you can put the pound sign into your
### program directly by pasting it from the Windows Character Map accessory.


#### Solution:


##### Given : This is a simple program but it may look a bit daunting. You may initially think that you have to convert only shillings and pence to pence and then just convert them into modern system but actually you need to conver pound, shillings and pence all to pence and divide by 240 because 240 pence = 1 pound in the old system. So, the hint given in the question about the user interation makes this question an easy question. 

```C++
#include<iostream>
using namespace std;


int main()
{
    float pounds, shillings, pence, shilltopence1, shilltopence2, poundtoshill;
    double newsystem;
    
    cout << "Enter pounds: ";
    cin >> pounds;
    cout << "Enter shillings: ";
    cin >> shillings;
    cout << "Enter pence: ";
    cin >> pence;
    
    poundtoshill = pounds * 20;
    shilltopence1 = shillings * 12;
    shilltopence2 = poundtoshill * 12;
    
    newsystem = (shilltopence1 + shilltopence2 + pence) / 240;
    
    cout << "Pounds in new system equals: " << newsystem << endl;
    
    return 0;
}
```

--------------------------------------------------------------------------------------------------------------------------------
