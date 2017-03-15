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
