
# C++ Basics
## Please click the link below for coloured formatting for better legibility, otherwise continue reading. 

[For coloured code formatting click here](https://github.com/devanshusinghgithub/devanshusinghgithub.github.io/blob/master/_posts/2017-3-5-Chapter-2-Programming-Problems.md)






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

-------------------------------------------------------------------------------------------------------------------------------

### Q9. Write the inverse of Exercise 10, so that the user enters an amount in Great Britain’s new decimal-pounds notation (pounds and pence), and the program converts it to the old pounds-shillings-pence notation. An example of interaction with the program might be 

### Enter decimal pounds: 3.51
### Equivalent in old notation = £3.10.2.

### Make use of the fact that if you assign a floating-point value (say 12.34) to an integer variable, the decimal fraction (0.34) is lost; the integer value is simply 12. Use a cast to avoid a compiler warning. You can use statements like

### float decpounds; // input from user (new-style pounds)
### int pounds; // old-style (integer) pounds
### float decfrac; // decimal fraction (smaller than 1.0)
### pounds = static_cast < int >(decpounds); // remove decimal fraction
### decfrac = decpounds - pounds; // regain decimal fraction

### You can then multiply decfrac by 20 to find shillings. A similar operation obtains pence.



#### Solution:

##### Given : The best question in this chapter without a doubt. Lovely!


#### Do note that there is a space before int and after int in the question. This is because of issues with github markdown language. The syntax does not contain actually spaces.


```C++
#include<iostream>
using namespace std;


int main()
{
    float decpounds, decfrac, shilling, pence;
    int pounds;
    
    cout << "Enter Pounds as per new British System: ";
    cin >> decpounds;
    
    pounds = static_cast<int>(decpounds);     //Pounds obtained and decimal gotten rid of
    decfrac = decpounds - pounds;             //To get the fraction part of user input for future converstion to shillings and pence
    
    decfrac *= 20;                            //This is just part one of obtaining shillings
    shilling = int(decfrac);                  //Shillings obtained. A whole number!
    
    pence = decfrac - shilling;               //To recover fraction lost while getting shillings
    pence *= 12;
    pence = int(pence);                       //Finally a whole number obtained for pence
    
    cout << "Pounds as per old system is: " << pounds << "." << shilling << "." << pence << endl;
    return 0;
}
```

-------------------------------------------------------------------------------------------------------------------------------

# Loops and Decisions in C++

--------------------------------------------------------------------------------------------------------------------------------

### Q1. Assume that you want to generate a table of multiples of any given number. Write a program that allows the user to enter the number and then generates the table, formatting it into 10 columns and 20 lines. Interaction with the program should look like this (only the first three lines are shown):

### Enter a number: 7
###   7  14  21  28  35  42  49  56  63  70
###  77  84  91  98 105 112 119 126 133 140
### 147 154 161 168 175 182 189 196 203 210


#### Solution:

```C++
#include<iostream>
#include<iomanip>                                   //For setw manipulator
using namespace std;


int main()
{
    unsigned long x;                                          // Defines an integer x
    
    cout << "Please enter a number: ";              // User enters a number
    cin >> x;                                       // Entered value is assigned to x
    
    for (int i=1; i<=200; i++)                      // For 20 lines
        {
        cout << setw(5) << i*x << " ";         // Width enough to accomodate large numbers
        if(i/10 == 0)                              // The question says columns must be 10
            cout << endl;              
        }
    return 0;
}
```

--------------------------------------------------------------------------------------------------------------------------------



### Q2. Write a temperature-conversion program that gives the user the option of converting Fahrenheit to Celsius or Celsius to Fahrenheit. Then carry out the conversion. Use floating-point numbers. Interaction with the program might look like this:

### Type 1 to convert Fahrenheit to Celsius,
### 2 to convert Celsius to Fahrenheit: 1
### Enter temperature in Fahrenheit: 70
### In Celsius that’s 21.111111


#### Solution: 

##### Now, problem clearly states that before you even take the input on which you will perform computation, you must give user the option to choose between one or the other. So here we have two options, one is to use two if statements and the other is to use an if.....else statement. For if.....else statement we will in reality be saying that as long as the user type any integer that is not 1, we will convert from Celsius to Fehrenheit. But with two if statements the user will have to type exactly what we want him/her to. 

```C++

#include<iostream>
using namespace std;

int main()

{
    int x;
    float fahrenheit, celsius;
    double ftoc, ctof;
    
    cout << "Please enter 1 for to convert from Fahrenheit to Celsius or 2 for the other way around: ";     // Ask user for input
    cin >> x;                                                                                               // Entered integer is stored in variable x.
                                                                                                            // The entered value to choose from if or else.
    
    if (x == 1)
       {
           cout << "Enter value in Fahrenheit: ";
           cin >> fahrenheit;
           ftoc = (fahrenheit - 32) * 5/9;
           cout << "Equivalent value in Celsius is: " << ftoc << endl;
       }
    if (x == 2)
        {   cout << "Enter value in Celsius: ";
            cin >> celsius;
            ctof = (celsius * 9/5) + 32;
            cout << "Equivalent value in Fahrenheit is: " << ctof << endl;
        }
    return 0;
    
}

```
--------------------------------------------------------------------------------------------------------------------------------

### Q3. Create the equivalent of a four-function calculator. The program should ask the user to enter a number, an operator, and another number. (Use floating point.) It should then carry out the specified arithmetical operation: adding, subtracting, multiplying, or dividing the two numbers. Use a switch statement to select the operation. Finally, display the result.

### When it finishes the calculation, the program should ask whether the user wants to do another calculation. The response can be ‘y’ or ‘n’. Some sample interaction with the program might look like this:

### Enter first number, operator, second number: 10 / 3
### Answer = 3.333333
### Do another (y/n)? y
### Enter first number, operator, second number: 12 + 100
### Answer = 112
### Do another (y/n)? n



#### Solution:

##### This question is very similar to one of the examples where we used while( n != 0) statement. In this case we replace n with a char and 0 with n for no. Simple question. There are actually two more ways in which this problem can be handled. But the following is my approach. 




```C++
#include<iostream>
using namespace std;

int main()
{
    float num1, num2, answer;
    char arithop, ch;
    
    while (ch != 'n')
    {
    cout << "Please enter a number, operator and another number: ";
    cin >> num1 >> arithop >> num2;
    
    if 
   
        (arithop == '+')
        answer = num1 + num2;
        
     
    
    else if
       
        (arithop == '-')
        answer = num1 - num2;
        
    
    else if
    
        (arithop == '/')
        answer = num1/num2;
        
    
    else if 
    
        (arithop == '*')
        answer = num1 * num2;
        
    cout << answer << endl;
    
    cout << "Do you want to do another calculation? : y/n";
    cin >> ch;
    }
    
return 0;
```    
}

--------------------------------------------------------------------------------------------------------------------------------


### Q4. Use for loops to construct a program that displays a pyramid of Xs on the screen. The pyramid should look like this

###      X
###     XXX
###    XXXXX
###   XXXXXXX
###  XXXXXXXXX

### except that it should be 20 lines high, instead of the 5 lines shown here. One way to do this is to nest two inner loops, one to print spaces and one to print Xs, inside an outer loop that steps down the screen from line to line.

#### Solution:

##### The question itself gives us a hint on how to solve this. As we learned, if the no of iterations are known or are fixed, we use for loop. So the hint here is we can create a pyramid by nesting two inner loops. So, we will be nexting two for loops in on outter loop. 

##### One more thing to understand here is that the pyramid's base will be 20 total 'x'. This is key to forming the right for loop for spaces. We need to create a strong relation between spaces and 20 to make sure it works right. Remember to put endl not in the inner loops but in the outer loop or it's scope changes. 

##### Lastly after the x has been printed there is no more spaces need obviously. So, don't get bogged down by that.
##### In each row upto 20, spaces keep decreasing by one until there is no space at the base of the pyramid. 

```C++

#include<iostream>
using namespace std;

int main()
{
    int iterations, space, row, x;
    row = 20;
    
    for (iterations = 0; iterations < 20; ++iterations)
    
    {
        for (space = 0; space < row - iterations; ++space)
            {
                cout << " ";
            }
    
        for (x = 0; x < 2 * iterations + 1; x++)
            {
                cout << "x";
            }
        cout << endl;                                           
    }

return 0;

}

```

--------------------------------------------------------------------------------------------------------------------------------


### Q5. Modify the FACTOR program in this chapter so that it repeatedly asks for a number and calculates its factorial, until the user enters 0, at which point it terminates. You can enclose the relevant statements in FACTOR in a while loop or a do loop to achieve this effect.


#### Solution:



```C++

#include<iostream>
using namespace std;

int main()

{
    unsigned int number;
    unsigned long factorial;
    number = 1;
    factorial = 1;
    
    while (number != 0)
    {
        cout << "Please enter a number: ";
        cin >> number;
        
        for (int j = number; j > 0; j--)
        {
            factorial *= j;
        }
        
        cout << "Factorial of chosen number is: " << factorial << endl;
        
    }

return 0;

}

```

--------------------------------------------------------------------------------------------------------------------------------


### Q6. Write a program that calculates how much money you’ll end up with if you invest an amount of money at a fixed interest rate, compounded yearly. Have the user furnish the initial amount, the number of years, and the yearly interest rate in percent. Some interaction with the program might look like this:

### Enter initial amount: 3000
### Enter number of years: 10
### Enter interest rate (percent per year): 5.5
### At the end of 10 years, you will have 5124.43 dollars.

### At the end of the first year you have 3000 + (3000 * 0.055), which is 3165. At the end of the second year you have 3165 + (3165 * 0.055), which is 3339.08. Do this as many times as there are years. A for loop makes the calculation easy.

#### Solution:

##### The question says a for loop will make calculations easy and I agree. We can set a variable to intial input amount and we can have variables as conditions for 'for' loop. This program requires clearly defined variables so be professional. 
##### Use the following variable names to make the program better 
##### 1. 'finalamount' for intial amount and final amount. 
##### 2. 'year' for number of years
##### 3. 'interest' for interest rate.


```C++
#include<iostream>
using namespace std;

int main()
{
    int year;                                                                       //For input from user. 
    float finalamount , interest;
    
    cout << "Enter the initial invested amound: ";                                  //This variable has been sent to finalamount 
                                                                                    //because of the formula used. 
    cin >> finalamount;
    cout << "Enter number of years to maturity: ";
    cin >> year;
    cout << "Enter the Rate of Interest(percent per year): ";
    cin >> interest;
    
        
    for (int j = 1; j <= year ; j++)
        {
            finalamount = finalamount + (finalamount * interest/100);
        }

    cout<<"Balance after maturity: "<< finalamount << endl;
    
return 0;
}
```

--------------------------------------------------------------------------------------------------------------------------------


### Q7. Suppose you give a dinner party for six guests, but your table seats only four. In how many ways can four of the six guests arrange themselves at the table? Any of the six guests can sit in the first chair. Any of the remaining five can sit in the second chair. Any of the remaining four can sit in the third chair, and any of the remaining three can sit in the fourth chair. (The last two will have to stand.) So the number of possible arrangements of six guests in four chairs is 6*5*4*3, which is 360. Write a program that calculates the number of possible arrangements for any number of guests and any number of chairs. (Assume there will never be fewer guests than chairs.) Don’t let this get too complicated. A simple for loop should do it.


#### Solution

##### Very easy question. Again like the British Pound question in chapter 2, it looks complicated but it isn't. 

```C++
#include<iostream>
using namespace std;

int main()
{
    int guests, chairs, arrangements;
    arrangements = 1;
    
    cout << "Please enter number of chairs: ";
    cin >> chairs;
    
    cout << "Please enter number of guests: ";
    cin >> guests;
    
    for (int j = 0; j < chairs; j++)
        {
        arrangements *= guests - j;   
        }
    
    cout << arrangements << endl;

    return 0;
}
```

--------------------------------------------------------------------------------------------------------------------------------


### Q8. Write another version of the program from Question 6 so that, instead of finding the final amount of your investment, you tell the program the final amount and it figures out how many years it will take, at a fixed rate of interest compounded yearly, to reach this amount. What sort of loop is appropriate for this problem? (Don’t worry about fractional years; use an integer value for the year.)


#### Solution: 

##### Always use a notebook or paper in the beginning of learning programming to understand how control goes from one statement to another. This is again an easy problem. Infact it's so simple that we can just copy the code of Question 6, change the formula to decrease from final amount to initial amount and where it stop because of another condition that final amount should not become less than intial amount, we can cout the counter from loop conditions as output. This all was figured out using pen and paper and creating pseudocode with leading lines to show flow of control. 


##### ALSO REMEMBER THIS!!!
##### The for loop is appropriate when you know in advance how many times the loop will be executed. The while and do loops are used when you don’t know in advance when the loop will terminate (the while loop when you may not want to execute the loop body even once, and the do loop when you’re sure you want to execute the loop body at least once). Also note that this isn't a hard and fast rule but it does guide you a bit. 



```C++
#include<iostream>
using namespace std;

int main()
{
    int initialamount, j;                                                                       //For input from user. 
    float finalamount , interest;
    j = 0;
    
    cout << "Enter the final amount: ";                                  //This variable has been sent to finalamount 
                                                                                    //because of the formula used. 
    cin >> finalamount;
    cout << "Enter the initial amount: ";
    cin >> initialamount;
    cout << "Enter the Rate of Interest(percent per year): ";
    cin >> interest;
    
    while (finalamount >= initialamount)
        {
            finalamount = finalamount - (finalamount * interest/100);
            j++;
        }
    cout<<"No of years to reach Final Amount: "<< j << endl;
    
return 0;
}
```


--------------------------------------------------------------------------------------------------------------------------------


# Intermediate Algorithm Scripting in C++

--------------------------------------------------------------------------------------------------------------------------------

### A phone number, such as (212) 767-8900, can be thought of as having three parts: the area code (212), the exchange (767),
### and the number (8900). Write a program that uses a structure to store these three parts of a phone number separately.
### Call the structure phone. Create two structure variables of type phone.
### Initialize one, and have the user input a number for the other one. Then display both numbers.
### The interchange might look like this:
### Enter your area code, exchange, and number: 415 555 1212
### My number is (212) 767-8900
### Your number is (415) 555-1212



#### Solution:

##### This problem is way to similar to the example where we stored model number, 
##### part number and part cost in a structure. 
##### In this case we will cout "(212) 767-8900" for my number and then cout the members 
##### of the structure that are modified by the user using input. 
##### So, replace moder number with area code, part number with exchange, and part cost with the number. 



```C++

#include <iostream>
using namespace std;

////////////////////////////////////////////////////STRUCTURE///////////////////////////////////////////////////////


struct phone
{
int areacode;                                                         //Three members of structure called phone.       
int exchange; 
int number; 
};

/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////


int main()
{

phone phoneuser;                                                      //Define a variable phoneuser of type phone

cout << "Please enter your area code, exchange, and number";

cin >> phoneuser.areacode >> phoneuser.exchange >> phoneuser.number;  //We know this is the only way to access structure members
                                                                      //Because structure members are of user-defined data type
cout << "My number is: " << "(212) 767-8900";                           
cout << "Your number is: " << "(" << phoneuser.areacode << ")" << phoneuser.exchange << "-" << phoneuser.number << endl;
 
return 0;
}
```

--------------------------------------------------------------------------------------------------------------------------------

### A point on the two-dimensional plane can be represented by two numbers: an x coordinate and a y coordinate. For example, (4,5) represents a point 4 units to the right of the vertical axis, and 5 units up from the horizontal axis. The sum of two points can be defined as a new point whose x coordinate is the sum of the x coordinates of the two points, and whose y coordinate is the sum of the y coordinates. Write a program that uses a structure called point to model a point. Define three points, and have the user input values to two of them. Then set the third point equal to the sum of the other two, and display the value of the new point. Interaction with the program might look like this:

### Enter coordinates for p1: 3 4
### Enter coordinates for p2: 5 7
### Coordinates of p1+p2 are: 8, 11

#### Solution:

##### Again, this problem is similar to exercise 1 and that widget parts example. No further explanation needed. Use the variables as shown above. Your variable name are sometimes too long.  

```C++

#include <iostream>
using namespace std;

////////////////////////////////////////////////////STRUCTURE///////////////////////////////////////////////////////


struct point
{
int x; 
int y; 
};


/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

int main()
{

point p1, p2, p3;

cout << "Please enter coordinates for point 1: ";
cin >> p1.x >> p1.y;

cout << "Please enter coordinates for point 2: ";
cin >> p2.x >> p2.y;

p3.x = p1.x + p2.x;                                             //Just like addition of coordinates in mathematics
p3.y = p1.y + p2.y;
cout << "Coordinates for sum of point 1 and point 2 is: " << "(" << p3.x << ", " << p3.y << ")" <<endl;

return 0;
}
```

--------------------------------------------------------------------------------------------------------------------------------

### Q3. Create a structure called Volume that uses three variables of type Distance (from the ENGLSTRC example) to model the volume of a room. Initialize a variable of type Volume to specific dimensions, then calculate the volume it represents, and print out the result. To calculate the volume, convert each dimension from a Distance variable to a variable of type float representing feet and fractions of a foot, and then multiply the resulting three numbers.

#### Solution:

##### A very simple problem. The question itself tells us which example to take 'inspiration' from. Basically we are going to nest a structure inside another structure just like we did in the example architecture sofware example where we nested two structures. 

```C++
#include <iostream>
using namespace std;

////////////////////////////////////////////////////STRUCTURE1//////////////////////////////////////////////////////


struct Distance
{
int feet;
float inches;
};

////////////////////////////////////////////////////STRUCTURE2//////////////////////////////////////////////////////

struct Volume
{
Distance length;
Distance width;
Distance height;
};

/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

int main()
{
float l, w, h;

Volume room = { { 16, 3.5 }, { 12, 6.25 }, { 8, 1.75 } };

l = room.length.feet + room.length.inches/12.0;
w = room.width.feet + room.width.inches /12.0;
h = room.height.feet + room.height.inches/12.0;

cout << "Volume of the room is: " << l*w*h << " cubic feet" << endl;
return 0;
}
```

--------------------------------------------------------------------------------------------------------------------------------

### Q4. Create a structure of type date that contains three members: the month, the day of the month, and the year, all of type int. (Or use day-month-year order if you prefer.) Have the user enter a date in the format 12/31/2001, store it in a variable of type struct date, then retrieve the values from the variable and print them out in the same format.


####  Solution:

##### Again a simple program with only input and output. No loop needed. 


```C++
#include<iostream>
using namespace std;

////////////////////////////////////////////////////STRUCTURE///////////////////////////////////////////////////////


struct Date
{
int month;
int day;
int year;
};

/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

int main()
{
struct date1;

cout << "Please enter the day of the month: ";
cin >> date1.day;
cout << "Please enter the month: ";
cin >> date1.month;
cout << "Please enter the year: ";
cin >> date1.year;

cout << "The chosen date is: " << date1.month << "/" << date1.day << "/" << date1.year << endl;

return 0;
}
```

--------------------------------------------------------------------------------------------------------------------------------

### Q5. We said earlier that C++ I/O statements don’t automatically understand the data types of enumerations. Instead, the (>>) and (<<) operators think of such variables simply as integers. You can overcome this limitation by using switch statements to translate between the user’s way of expressing an enumerated variable and the actual values of the enumerated variable. For example, imagine an enumerated type with values that indicate an employee type within an organization: enum etype { laborer, secretary, manager, accountant, executive, researcher };
### Write a program that first allows the user to specify a type by entering its first letter (‘l’, ‘s’, ‘m’, and so on), then stores the type chosen as a value of a variable of type enum etype, and finally displays the complete word for this type.
### Enter employee type (first letter only) laborer, secretary, manager, accountant, executive, researcher): a
### Employee type is accountant.
### You’ll probably need two switch statements: one for input and one for output.


#### Solution :

```C++
#include<iostream>
using namespace std;

enum employee {laborer, secretary, manager, accountant, executive, researcher};
 
int main()
    {
    char letter;
    employee etype;
 
    cout << "Please enter employee type(only type in first letter eg. l for laborer. Options : laborer, secretary, manager, accountant, executive, researcher ) " << endl;
          
    cin >> letter;
 
    switch(letter)
        {
        case 'l': etype = laborer; break;
        case 's': etype = secretary; break;
        case 'm': etype = manager; break;
        case 'a': etype = accountant; break;
        case 'e': etype = executive; break;
        case 'r': etype = researcher;
        }
        
    
        
    cout << "Employee type is: " << etype << endl;
    
    return 0;
    }
```


--------------------------------------------------------------------------------------------------------------------------------


### Q6. Create a structure called time. Its three members, all type int, should be called hours, minutes, and seconds. Write a program that prompts the user to enter a time value in hours, minutes, and seconds. This can be in 12:59:59 format, or each number can be entered at a separate prompt (“Enter hours:”, and so forth). The program should then store the time in a variable of type struct time, and finally print out the total number of seconds represented by this time value:long totalsecs = t1.hours*3600 + t1.minutes*60 + t1.seconds.


#### Solution:

```C++
#include<iostream>
using namespace std;

int totalseconds;

////////////////////////////////////////////////////STRUCTURE///////////////////////////////////////////////////////


struct time 
{
int hours;
int minutes;
int seconds;
};

/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

int main()
{
    time time1;
    
    cout << "Enter Hours: ";
    cin >> time1.hours;
    
    cout << "Enter Minutes: ";
    cin >> time1.minutes;
 
    cout << "Enter Seconds: ";
    cin >> time1.seconds;
 
    totalseconds = time1.hours*3600 + time1.minutes*60 + time1.seconds;
 
    cout<<"The total number of seconds is: "<< totalseconds << endl ;
return 0;
}
```


--------------------------------------------------------------------------------------------------------------------------------


### Q7.  Create a structure called sterling that stores money amounts in the old-style British system discussed in Exercises 8 and 11 in Chapter 3, “Loops and Decisions.” The members could be called pounds, shillings, and pence, all of type int. The program should ask the user to enter a money amount in new-style decimal pounds (type double), convert it to the old-style system, store it in a variable of type struct sterling, and then display this amount in pounds-shillings-pence format.


#### Solution: 


```C++
#include<iostream>
using namespace std;

////////////////////////////////////////////////////STRUCTURE///////////////////////////////////////////////////////

struct sterling 
{
int pounds;
int shillings;
int pence;
};

/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

int main()
{
    sterling s1;
    double decpounds;
    float decfrac;
    
    cout << "Please enter value new style decimal pounds: ";
    cin >> decpounds;
    
    s1.pounds = static_cast<int>(decpounds);
    decfrac = 240 * (decpounds - s1.pounds);

    s1.shillings = (static_cast<int>(decfrac)) % 12;
    
    decfrac = static_cast<int>((decfrac-s1.shillings) / 12);
     
    cout<<"The equivalent amount as per old notation is: "<< s1.pounds << "."<< decfrac <<"." <<s1.shillings << endl; 

return 0;
}
```

--------------------------------------------------------------------------------------------------------------------------------

### Q8. Use the time structure from Question 6, and write a program that obtains two time values from the user in 12:59:59 format, stores them in struct time variables, converts each one to seconds (type int), adds these quantities, converts the result back to hoursminutes-seconds, stores the result in a time structure, and finally displays the result in 12:59:59 format.

#### Solution:


```C++
#include<iostream>
using namespace std;

int totalseconds, totalseconds1, totalseconds2;

////////////////////////////////////////////////////STRUCTURE///////////////////////////////////////////////////////


struct time 
{
int hours;
int minutes;
int seconds;
};

/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

int main()
{
    time time1, time2, time3;
    
    cout << "Enter Hours: ";
    cin >> time1.hours;
    
    cout << "Enter Minutes: ";
    cin >> time1.minutes;
 
    cout << "Enter Seconds: ";
    cin >> time1.seconds;
 
    totalseconds1 = (time1.hours * 3600) + (time1.minutes * 60) + time1.seconds;
    
    cout << "Enter Hours for Second Time: ";
    cin >> time2.hours;
    
    cout << "Enter Minutes for Second Time: ";
    cin >> time2.minutes;
    
    cout << "Enter Seconds for Second Time: ";
    cin >> time2.seconds;
    
    totalseconds2 = (time2.hours * 3600) + (time2.minutes * 60) + time2.seconds;
    
    totalseconds = totalseconds1 + totalseconds2;
    
    time3.hours = (totalseconds / 3600) % 24;
    time3.minutes = (totalseconds / 60) % 60;
    time3.seconds = (totalseconds / 60);
    
    cout<<"The new time is: "<< time3.hours << ":" << time3.minutes << ":" << time3.seconds << endl ;

return 0;
}
```


--------------------------------------------------------------------------------------------------------------------------------


# Functions in C++



### Q1. Refer to the CIRCAREA program in Chapter 2, “C++ Programming Basics.” Write a function called circarea() that finds the area of a circle in a similar way. It should take an argument of type float and return an argument of the same type. Write a main() function that gets a radius value from the user, calls circarea(), and displays the result.


#### Solution:

```C++
#include<iostream>
using namespace std;
float circlearea (float radius);    //A funciton called circlearea that will
                                    // return a float value and takes another 
                                    //float radius as argument
                                    //Function declaration

int main()

{
    float userradius;
    cout << "Please enter radius: ";
    cin >> userradius;
    cout << "The area of the circle of entered radius is: " << circlearea(userradius) << endl;
    return 0;
}

/////////////////////////////////////////////Function Definition////////////////////////////////////////////////

float circlearea(float radius)
{
    const float PI = 3.14F;
    return radius * radius * PI;
}

////////////////////////////////////////////////////////////////////////////////////////////////////////////////
```


--------------------------------------------------------------------------------------------------------------------------------


### Q2.  Raising a number n to a power p is the same as multiplying n by itself p times. Write a function called power() that takes a double value for n and an int value for p, and returns the result as a double value. Use a default argument of 2 for p, so that if this argument is omitted, the number n will be squared. Write a main() function that gets values from the user to test this function.


#### Solution: 

```C++
#include<iostream>
using namespace std;

/////////////////////////////////////////Funtion Declaration////////////////////////////////////////////

double power (double, int = 2);

///////////////////////////////////////////////////////////////////////////////////////////////////////

int main()
{
	int p;
	double n;
	double solution;
	
	cout << "Please enter the number : ";
	cin >> n;
	
	cout << "Please enter the exponent : ";
	cin >> p;
	
	solution = power(n,p);
	
	cout << "Result is " << solution;
	
	return 0;
}

////////////////////////////////////Function Definition//////////////////////////////////////////

double power(double nn, int pp)
{
	double a = 1;
	for(int i = 1; i <= pp; i++)
		a = a * nn;
	return a;
}

/////////////////////////////////////////////////////////////////////////////////////////////////
```

--------------------------------------------------------------------------------------------------------------------------------


### Q3. Write a function called zeroSmaller() that is passed two int arguments by reference and then sets the smaller of the two numbers to 0. Write a main() program to exercise this function.


#### Solution:

```C++
#include <iostream>
using namespace std;

/////////////////////////////////Funtion Declaration//////////////////////////////////////

void zeroSmaller(int&, int&);

//////////////////////////////////////////////////////////////////////////////////////////

int main()
{

int a, b;

cout << "Please enter first number: ";
cin >> a;

cout << "Please enter second number: ";
cin >>b;

zeroSmaller(a, b);

cout << "First number is: " << a << endl;
cout << "Second number is: " << b << endl;

return 0;
}

/////////////////////////////////Function Definition//////////////////////////////////////

void zeroSmaller(int& x, int& y)
{
    if( x < y )
        x = 0;

    else
        y = 0;
}

//////////////////////////////////////////////////////////////////////////////////////////
```

--------------------------------------------------------------------------------------------------------------------------------

### Q4. Write a function that takes two Distance values as arguments and returns the larger one. Include a main() program that accepts two Distance values from the user, comparesthem, and displays the larger. (See the RETSTRC program for hints.)


#### Solution:

```C++
#include<iostream>
using namespace std;

//////////////////////////////////////Function Declaration/////////////////////////////////////

int distance (int d1, int d2);

///////////////////////////////////////////////////////////////////////////////////////////////

int main()
{
	int distance1, distance2;
	
	cout << "Please enter first distance: ";
	cin >> distance1;
	
	cout << "Please enter second distance: ";
	cin >> distance2;

	cout << " The larger distance is: "<< distance (distance1, distance2);
	
}


////////////////////////////////////Function Definition////////////////////////////////////////

int distance (int d1, int d2)

{ 
    if(d1<d2) 
        return d2; 
    
    else
        return d1;
}


///////////////////////////////////////////////////////////////////////////////////////////////
```

-------------------------------------------------------------------------------------------------------------------------------


### Q5. Write a function called hms_to_secs() that takes three int values—for hours, minutes, and seconds—as arguments, and returns the equivalent time in seconds (type long). Create a program that exercises this function by repeatedly obtaining a time value in hours, minutes, and seconds from the user (format 12:59:59), calling the function, and displaying the value of seconds it returns.


#### Solution: Finally an exciting problem after a long lull. The function should have three arguments. It's similar to one we did in the previous chapter but this time we are using a function instead of a structure. 

```C++
#include<iostream>
using namespace std;

////////////////////////////////////Function Declaration/////////////////////////////////////

int hms_to_sec(int hours, int minutes, int seconds);

/////////////////////////////////////////////////////////////////////////////////////////////

int main()
{
int userhours, userminutes, userseconds, finalseconds;


cout << "Please enter hours: ";
cin >> userhours;

cout << "Please enter minutes: ";
cin >> userminutes;

cout << "Please enter seconds: ";
cin >> userseconds;

finalseconds = hms_to_sec(userhours , userminutes, userseconds);

6. 
cout << "Equavilent in seconds is: " << finalseconds;

return 0;
}

///////////////////////////////////////Funtion Definition///////////////////////////////////////////

int hms_to_sec(int hours, int minutes, int seconds)
{
    int result;

    result = (hours * 60 * 60) + (minutes * 60) + seconds;

    return result;
}

////////////////////////////////////////////////////////////////////////////////////////////////////
```


-------------------------------------------------------------------------------------------------------------------------------

### Q6: Start with the program from Question 8 in Chapter 4, “Structures,” which adds two struct time values. Keep the same functionality, but modify the program so that it uses two functions. The first, time_to_secs(), takes as its only argument a structure of type time, and returns the equivalent in seconds (type long). The second function, secs_to_time(), takes as its only argument a time in seconds (type long), and returns a structure of type time.


#### Solution: The difficulty of programs is on the rise again. In this we will pass a structure as argument. We will create two functions i.e. time_to_secs() and secs_to_time().


```C++
#include<iostream>
using namespace std;

/////////////////////////////////////Structure of type time////////////////////////////////////

struct time
{
    int hours;
    int minutes;
    int seconds;
};

////////////////////////////////////////////////////////////////////////////////////////////////

/////////Function must return type long and should take argument of type time(structure)///////
//////////////////////////////Function Declaration/////////////////////////////////////////////

long time_to_secs(time usertime);

////////////////////////////////////////////////////////////////////////////////////////////////

/////A second function should return type time and should take in agrument, type long seconds///
////////////////////////////////////////Funtion Declaration/////////////////////////////////////

time secs_to_time(long userseconds);

/////////////////////////////////////////////////////////////////////////////////////////////////

int main()
{
	
	time t1, t2, t3;
	

	cout << "Please enter hours value of first time: ";
	cin >> t1.hours;
	
	cout << "Please enter minutes value of first time: ";
	cin >> t1.minutes; 
	
	cout << "Please enter hours value of second time: ";
	cin >> t2.hours;
	
	cout << "Please enter minutes value of second time: ";
	cin >> t2.minutes;
	
	cout << "Please enter seconds value of second time: ";
	cin >> t2.seconds;
	
	t3 = secs_to_time (time_to_secs(t1) + time_to_secs(t2));
	
	cout<<"The sum is: "<< t3.hours << ":" << t3.minutes << ":" <<t3.seconds << endl;
	
	return 0;
}

/////////////////////////////////Funtion definition for time_to_secs///////////////////////////////////


long time_to_secs(time usertime)
{   
    int result1;
    result1 = t1.hours * 3600 + t1.minutes * 60 + t1.seconds;
    return result1;
}
    
///////////////////////////////////////////////////////////////////////////////////////////////////////

////////////////////////////Funtion declaration for secs_to_time///////////////////////////////////////

    time secs_to_time(long userseconds)
    
{
	time result2;
	
	t3.seconds = userseconds % 60; 
	t3.minutes= ((userseconds - usertime . seconds) % 3600) / 60;
	t3.hours = userseconds / 3600;
	
	if(t3.seconds>59)
	    {
	        t3.seconds -= 59; t3.minutes++;
	    } 
	        
	        
	if(t3.minutes > 59)
	    {
	        t3.minutes -= 59; t3.hours++;
	    }  
	    
	return t3;
}
```

-------------------------------------------------------------------------------------------------------------------------------

### Q7. Start with the power() function of Question 2, which works only with type double. Create a series of overloaded functions with the same name that, in addition to double, also work with types char, int, long, and float. Write a main() program that exercises these overloaded functions with all argument types.

#### Solution:

```C++
#include<iostream>
using namespace std;

////////////////////////////////Funtion declarations///////////////////////////////////////

double power(double, int p);

char   power(char, int p);

int    power(int, int p);

long   power(long, int p);

float  power(float, int p);

///////////////////////////////////////////////////////////////////////////////////////////

int main()
{
    	int p;
	
	double double_n;
	char char_n;
	int int_n;
	long long_n;
	float float_n;
	
	double solution;
	
	cout << "Please type a number: ";
	cin >> double_n;
	cin >> char_n;
	cin >> int_n;
	cin >> long_n;
	cin >> float_n;
	
	
	cout << "Please type an exponent: ";
	cin >> p;
	
	solution = power(double_n,p);
    	solution = power(char_n,p);
    	solution = power(int_n,p);
   	 solution = power(long_n,p);
    	solution = power(float_n,p);
    
   	 return 0;
}	

/////////////////////////////////Funtion Definitions////////////////////////////////////////////

double power(double double_n, int p)
{
	double a = 1;
	for(int i = 1; i <= p; i++)
		a = a * double_n;
	return a;
}
```

-------------------------------------------------------------------------------------------------------------------------------

### Q8. Write a function called swap() that interchanges two int values passed to it by the calling program. (Note that this function swaps the values of the variables in the calling program, not those in the function.) You’ll need to decide how to pass the arguments. Create a main() program to exercise the function.


#### Solution: The problem is similar to Question 3 and the examples given for argument by reference. We need to utilise argument by reference to solve this problem. In the examples the temp variable was used to store value for swap purposes and apart from that this problem is almost exactly similar to Question 3. 


```C++
#include<iostream>
using namespace std;

//////////////////////////////////Function Declaration/////////////////////////////////////


void swap(int& a, int& b);


///////////////////////////////////////////////////////////////////////////////////////////


int main()
{

    int a, b;
	
    cout << "Please enter first number: ";
    cin >> a;

    cout << "Please enter second number: ";
    cin >>b;
    
    swap(a, b);
	
	cout << "The first number is: " << a << endl;
	
	cout << "The second number is: " << b << endl;

    return 0;	
}	
	
/////////////////////////////////Function Definition//////////////////////////////////////


void swap(int& a, int& b)
{
    int temp = a;
        a = b;
        b = temp;
}



///////////////////////////////////////////////////////////////////////////////////////////
```

-------------------------------------------------------------------------------------------------------------------------------


### 9. Repeat Exercise 8, but instead of two int variables, have the swap() function interchange two struct time values (see Question 6).

#### Solution: This problem again deals with "passing by reference". We have come to that part of the chapter. In this question we will be passing a structure as argument to a function called swap and we will be passing it by reference. 


```C++
#include<iostream>
using namespace std;


/////////////////////////////////Structure////////////////////////////////////////////


struct time
{
    int hours;
    int minutes;
    int seconds;
};


////////////////////////////////////////////////////////////////////////////////////////

///////////////////////////////////Function Declaration/////////////////////////////////


void swap(time& time1, time& time2);


/////////////////////////////////////////////////////////////////////////////////////////


int main()
{
	time time1, time2;
	

	cout << "Please enter hours value of first time: ";
	cin >> time1.hours;
	
	cout << "Please enter minutes value of first time: ";
	cin >> time1.minutes;
	
	cout << "Please enter seconds value of first time: ";
	cin >> time1.seconds;
	
	cout << "Please enter hours value of second time: ";
	cin >> time2.hours;
	
	cout << "Please enter minutes value of second time: ";
	cin >> time2.minutes;
	
	cout << "Please enter hours value of second time: ";
	cin >> time2.seconds;
	
	swap(time1, time2);
	
	cout << "After swap the first time is : " << time1.hours << ":" << time1.minutes << ":" << time1.seconds << endl;
	cout << "And the second time is : " << time2.hours << ":" << time2.minutes << ":" << time2.seconds;
	
	return 0;
}

/////////////////////////////Function Definition////////////////////////////////////////


void swap(int& a, int& b)
{
    int temp = a;
        a = b;
        b = temp;
}


/////////////////////////////////////////////////////////////////////////////////////////
```


-------------------------------------------------------------------------------------------------------------------------------

# Objects and Classes - Upper Intermediate Scripting


### Q1. Create a class that imitates part of the functionality of the basic data type int. Call the class Int (note different capitalization). The only data in this class is an int variable. Include member functions to initialize an Int to 0, to initialize it to an int value, to display it (it looks just like an int), and to add two Int values. Write a program that exercises this class by creating one uninitialized and two initialized Int values, adding the two initialized values and placing the response in the uninitialized value, and then displaying this result.


#### Solution:

```C++
#include<iostream>
using namespace std;


///////////////////////////////////Class/////////////////////////////////////////////

class Int

{

private:

    int var1;

public:

    Int()

    { var1 = 0; }

    Int(int var2)

        { var1 = var2; }

  

    int add(Int Int1,Int Int2)

        { var1 = Int1.var1 + Int2.var1; 
        return 0;
        }

    int display()2
        { cout << var1; 
        return 0;
        }

};


//////////////////////////////////////////////////////////////////////////////

int main()
{
    int a = 1;
    int b = 2;
    int c = 3;
    
    c.add(a,b);
    
    cout << "The result is: " << c.display() << endl;
    
    return 0;
}
```

-------------------------------------------------------------------------------------------------------------------------------


### Q2. Imagine a tollbooth at a bridge. Cars passing by the booth are expected to pay a 50 cent toll. Mostly they do, but sometimes a car goes by without paying. The tollbooth keeps track of the number of cars that have gone by, and of the total amount of money collected. 
### Model this tollbooth with a class called tollBooth. The two data items are a type unsigned int to hold the total number of cars, and a type double to hold the total amount of money collected. A constructor initializes both of these to 0. A member function called payingCar() increments the car total and adds 0.50 to the cash total. Another function, called nopayCar(), increments the car total but adds nothing to the cash total. Finally, a member function called display() displays the two totals. Make appropriate member functions const.
### Include a program to test this class. This program should allow the user to push one key to count a paying car, and another to count a nonpaying car. Pushing the Esc key should cause the program to print out the total cars and total cash and then exit.

#### Solution: 

```C++
#include <iostream>
using namespace std;

/////////////////////////////////////Class///////////////////////////////////////////

class tollBooth
{ 
    private:
       int null,pcar,wpcar;
       float tax;
    public:
       tollboth()
       {
              tax = 0;
              pcar = 0;
              wpcar = 0;
              null = 0;
       }
       void paycar(int a)
       {

       pcar = pcar + a;
       for(null; null <= pcar; null++)
       {
              tax = tax + 0.50;
       }
       }
       void withoutpay(int b)
       {
       wpcar = wpcar + b;
       }
       void showdata()
       {
       cout << "Total no of payed cars are : " << pcar << endl;
       cout<< "Total tax is : "<<tax<<endl; 
       cout<< "Total no of not payed cars are : "<< wpcar << endl;
    
       }
};

///////////////////////////////////////////////////////////////////////////////////////////

int main()
{
       tollboth tb;
       char press,input;
       int a,b;
 do{
    
       cout << "Press 1 for car pay tax" << endl;
       cout << "Press 2 for car not pay tax" << endl;
       cout << "Press 3 for total tax and Exit" << endl;
       cin >> press;

       switch(press)
       {
       case '1':
              {
                     cout << "Enter No of the cars pay tax"<<endl;
                     cin >> a;
                     tb.paycar(a);
                     break;
              }
       case '2':
              {
                     cout << "Enter No of cars not pay tax" << endl;
                     cin >> b;
                     tb.withoutpay(b);
                     break;
              }    
       } 
       cout <<"Press y to continue and n for terminate" << endl;
       cin >> input;
       }
       while(input == 'y');
       tb.showdata();
    system("pause");
    return 0;
}
```

-------------------------------------------------------------------------------------------------------------------------------

### Q3.Create an employee class, basing it on Question 4 of Chapter 4. The member data should comprise an int for storing the employee number and a float for storing the employee’s compensation. Member functions should allow the user to enter this data and display it. Write a main() that allows the user to enter data for three employees and display it.

#### Solution:

```C++
#include <iostream>

using namespace std;

//////////////////////////////////Class//////////////////////////////////////

class employee{
    private:
        int eNum;
        float eComp;
    
    public:
        void empData(){
        cout << "Please enter the employee number: ";
        cin >> eNum;
        cout << "Please enter the salary corresponding to that employee number: " ;
        cin >> eComp;
        }
  
    void display(){
        cout << "Employee Number: " << eNum << endl;
        cout << "Enployee Salary: " << eComp << endl;
        }
};

///////////////////////////////////////////////////////////////////////////////

int main(){
 
 employee a, b, c;
 
    cout << "Please enter the data for first employee: " << endl;
    a.empData();
    
    cout << "Please enter the data for second employee: " << endl;
    b.empData();

    cout << "Please enter the data For third employee: " << endl;
    c.empData();
    
    
    cout << "The following entries have been made: " << endl;
    a.display();
    b.display();
    c.display();
    
    return 0;
}
```

-------------------------------------------------------------------------------------------------------------------------------

### Q4 Start with the date structure in Question 5 in Chapter 4 and transform it into a date class. Its member data should consist of three ints: month, day, and year. It should also have two member functions: getdate(), which allows the user to enter a date in 12/31/02 format, and showdate(), which displays the date.

#### Solution:

```C++
#include<iostream>
using namespace std;

class date
{
private:

	int day, month, year;
	
public:
	void getdate()
	{
	cout<<"Enter date in [DD/MM/YY] format: ";
	cin >>day>>c>>month>>c>>year;
	}
	void showdate() const { cout<<"Date is: "<<day<<c<<month<<c<<year;}};

int main()
{
	date x;
	
	x.getdate();
	x.showdate();
	
	return 0;
}
```

-------------------------------------------------------------------------------------------------------------------------------
