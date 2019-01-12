---
layout: post
title: The Anatomy of a C++ Program
category: C++
tags: [C++]
---

# The Anatomy of a C++ Program
C++ programs are organized into classes comprising member functions and member variables.

**Remark**

if an artifact declared in FileA needs to be used in FileB, you need to include the former in the latter. You usually do that by inserting the following include statement in FileA:
 ```
#include "...relative path to FileB\FileB"
#include <headername>
```
 
In order to show anatomy, we list some programs.

 ```C++
 // a simple C++ program
// Preprocessor directive that includdes header iostream
#include <iostream>

// Start of your program: function block main()
int main()
{
  std::cout << "Hello World" << std::endl;
  
  return 0; // return a value to the os
}


#include <iostream>

using namespace std; // import all objects in std
using std::cout; // only import cout
using std::cin;

int main()
{
  cout << "Hello World" << endl;
  
  return 0;
  /* This is a comment which tells you this 
  comment can prolong to multipl line*/
}



// function
#include <iostream>
#include <string>

using namespace std;

int DemoOutput() // Function declaration and definition
{
  string inputName;
  getline(cin, inputNamee); // getline function is to get entire line
  cout << "Hello! " << inputName << endl; 
  
  return 0;
}

int main()
{
  DemoOutput(); // invoke the function
  
  return 0;
}
```
