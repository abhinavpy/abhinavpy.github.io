---
title: 'Daily Blog Post 5 April 2022'
date: 2022-04-05
permalink: /posts/2022/04/daily-post/
tags:
  - GRE Reading Comprehension
  - interview problems 
  - algorithms
  - data structures
  - Golang Basics
---
### Reading Comprehension - GREEdge
- Finished Advanced Reading Comprehension Exercise 3. Scored 12/20. Need to perform better. Again, questions were confusing. Made one or two errors that could have been avoidable.

### GRE Quant
- Watch https://www.youtube.com/watch?v=K7B0ckmrviM&ab_channel=Crackverbal to gain confidence to solve Venn Diagram questions in GRE Quant.
- Rule of thumb to differentiate when to use Venn Diagrams and Tables.

### Golang Tutorials
About Basics
Go is a statically typed, compiled programming language. Go is syntactically similar to C. The language is often referred to as Golang because of its previous domain name
golang.org, but the proper name is Go.
The Basics concept will introduce three major language features: packages, functions and variables.
Packages: Go applications are organized in packages. A package is a collection of source files located in the same directory. All source files in a directory must share the same package name.
It is conventional for the package name to be the last directory in the import path. For example the files in the "math/rand" package begin with the statement package rand.
When a package is imported, only entities (functions, types, variables, and constants) whose names start with a capital letter can be used/accessed. The recommended style of naming in 
Go is that identifiers will be named using camelCase, except for those meant to be accessible across packages which should be PascalCase.
```
package lasagna
```

Variables:
Go is statically types, which means all variables must have a defined type at compile time. 
Variables can be defined by explicitly specifying a type:
```
var explicit int
```
You can also use an initializer, and the compiler will assign the variable type to match the type of the initializer:
```
implicit := 10
```
Once declared variables can be assigned value using the = operator. 
Once declared a variable's type can never be changed.
count := 1 //Initial value
count = 2 //update new value
count = false //This throws a compiler error due to assigning a 'non' int-type

Constants:
Constants hold a piece of data just like variables, but their value cannot change during the execution of the program.
Constants are defined using the const keyboard and can be numbers, characters, strings or booleans:
const Age = 12

Functions:
Go functions accept zero or more parameters. Parameters must be explicitly typed, there is no type inference.
Values are returned from the function using the return keyword.
A function is invoked by specifying the function name and passing arguments for each of the function's parameters.
Note that Go supports two types of comments. Single line comments are preceded by // and multiple line comments are inserted between /* and */
```
package greeting
// Hello is a public function
func hello(name string) string {
  return hi(name)
}

// hi is a private function
func hi(name string) string {
  return "hi" + name;
}
```

Gopher's Gorgeous Lasagna
Instructions:
1. Define the expected oven time in minutes: Define OvenTime constant with how many minutes the Lasagna should be in the oven. According to the cooking book, the expected oven time in minutes is 40.
```
OvenTime
```
2. Calculate the remaining oven time in minutes: Define the RemainingOvenTime() function that takes the actual minutes the Lasagna has been in the oven as a parameter and returns how many minutes the lasagna still has to remain in the oven, based on the expected oven time in minutes from the previous task.
```
func RemainingOvenTime(actual int) int {
  //TODO
}
RemainingOvenTime(30)
```
3. Calculate the preparation time in minutes: Define the PreparationTime function that takes the number of layers you added to the lasagna as a parameter and returns how many minutes you spent preparing the lasagna, assuming each layer takes you 2 minutes to prepare.
```
func PreparationTime(numberOfLayers int) int {
  // TODO
}
PreparationTime(2)
```
4. Calculate the elapsed working time in minutes: Define the ElapsedTime function that takes two parameters: the first parameter is the number of layers you added to the Lasagna, the second parameter is the number of minutes the lasagna has been in the oven. The function should return how many minutes in total you have worked on cooking the lasagna, which is the sum of the preparation time in minutes, and the time in minutes the lasagna has spent in the oven at the moment.
```
func ElapsedTime(numberOfLayers, actualMinutesInOven int) int {
  // TODO
}
ElapsedTime(3, 20)
```
