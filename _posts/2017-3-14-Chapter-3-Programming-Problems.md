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


