---
title: 'Golang Prep April 8th 2022'
date: 2022-04-08
permalink: /posts/2022/04/daily-post/
tags:
  - Golang Basics
---

# Golang Interview Questions
All these questions and content were sourced from InterviewBit.com

Golang or most popularly known as Go is one of the youngest programming languages that was released in the year 2012 at Google by developers Robert Griesemer, Rob Pike and Ken Thompson. It is said that Golang was born out of frustration with the demerits of the existing programming languages. 

Go is a high level, open-source programming language that was mainly developed keeping in mind the efficiency of code without compromising on the simplicity and faster compilation time to help develop software applications at a faster pace. Companies like Google, Apple, Uber are using Golang due to its proven ability of less learning time, faster code development, improved runtime efficiency, reduced bugs, concurrency, garbage collection strategies and so on. 

## 1. What is Golang?
- Go is a high level, general-purpose programming language that is very strongly and statically typed by providing support for garbage collection and concurrent programming. 
- In Go, the programs are built by using packages that help in managing the dependencies efficiently. It also uses a compile-link model for generating executable binaries from the source code. Go is a simple language with elegant and easy to understand syntax structures. It has a built-in collection of powerful standard libraries that helps developers in solving problems without the need for third party packages. Go has first-class support for Concurrency having the ability to use multi-core processor architectures to the advantage of the developer and utilize memory efficiently. This helps the applications scale in a simpler way.

## 2. Why should one learn Golang? What are the advantages of Golang over other languages?
Go language follows the principle of maximum effect with minimum efforts. Every feature and syntax of Go was developed to ease the life of programmers. Following are the advantages of Go Language:

- **Simple and Understandable**: Go is very simple to learn and understand. There are no unnecessary features included. Every single line of the Go code is very easily readable and thereby easily understandable irrespective of the size of the codebase. Go was developed by keeping simplicity, maintainability and readability in mind.
- **Standard Powerful Library**: Go supports all standard libraries and packages that help in writing code easily and efficiently.
- **Support for concurrency**: Go provides very good support for concurrency using Go Routines or channels. They take advantage of efficient memory management strategies and multi-core processor architecture for implementing concurrency.
- **Static Type Checking**: Go is a very strong and statically typed programming language. Statically typed means every variable has types assigned to it. The data type cannot be changed once created and strongly typed means that there are rules and restrictions while performing type conversion. This ensures that the code is type-safe and all type conversions are handled efficiently. This is done for reducing the chances of errors at runtime.
- **Easy to install Binaries**: Go provides support for generating binaries for the applications with all required dependencies. These binaries help to install tools or applications written in Go very easily without the need for a Go compiler or package managers or runtimes.
- **Good Testing Support**: Go has good support for writing unit test cases along with our code. There are libraries that support checking code coverage and generating code documentation.

## 3. What are Golang Packages?
Go Packages (in short pkg) are nothing but directories in the Go workspace that contains Go source files or other Go packages themselves. Every single piece of code starting from variables to functions are written in the source files are in turn stored in a linked package. Every source file should belong to a package.

The package is declared at the top of the Go source file as package <package_name>

The packages can be imported to our source file by writing: import <package_name>

An example of the Go package is fmt. This is a standard Go Package that has formatting and printing functionalities such as Println().

## 4. Is Golang case sensitive or insensitive?
Go is a case-sensitive language.

## 5. What are Golang pointers?
Go Pointers are those variables that hold the address of any variables. Due to this, they are called special variables. Pointers support two operators:

- ```*``` operator: This operator is called a dereferencing operator and is used for accessing the value in the address stored by the pointer.
- ```&``` operator: This operator is called the address operator and is used for returning the address of the variable stored in the pointer.

Pointers are used for the following purposes:

- Allowing function to directly mutate value passed to it. That is achieving pass by reference functionality.
- For increasing the performance in the edge cases in the presence of a large data structure. Using pointers help to copy large data efficiently.
- Helps in signifying the lack of values. For instance, while unmarshalling JSON data into a struct, it is useful to know if the key is present or absent then the key is present with 0 value.

## 6. What do you understand by Golang string literals?
String literals are those variables storing string constants that can be a single character or that can be obtained as a result of the concatenation of a sequence of characters. Go provides two types of string literals. They are:

- Raw string literals: Here, the values are uninterrupted character sequences between backquotes. For example: `interviewbit`
- Interpreted string literals: Here, the character sequences are enclosed in double quotes. The value may or may not have new lines. For example: "Interviewbit Website"

## 7. What is the syntax used for the loop in Golang? Explain.
