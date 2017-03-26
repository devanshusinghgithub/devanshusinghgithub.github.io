# Solutions to programming problems from Chapter 3 of Object Oriented Programming in C++ by Robert Lafore

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

# I am really starting to enjoy programming now...LOL


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


# Solutions To Problem From Chapter 4 Of Object Oriented Programming in C++

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
### Q8. Use the time structure from Question 6, and write a program that obtains two time values from the user in 12:59:59 format, stores them in struct time variables, converts each one to seconds (type int), adds these quantities, converts the result back to hoursminutes-seconds, stores the result in a time structure, and finally displays the result in 12:59:59 format.

#### Solution:


