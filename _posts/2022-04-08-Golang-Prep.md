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
Go language follows the below syntax for implementing for loop.

```
for [condition |  ( init; condition; increment ) | Range]  
{  
   statement(s);  
   //more statements
}  
```

The for loop works as follows:
- The init steps gets executed first. This is executed only once at the beginning of the loop. This is done for declaring and initializing the loop control variables. This field is optional as long as we have initialized the loop control variables before. If we are not doing anything here, the semicolon needs to be present.
- The condition is then evaluated. If the condition is satisfied, the loop body is executed.
  - If the condition is not satisfied, the control flow goes to the next statement after the for loop.
  - If the condition is satisfied and the loop body is executed, then the control goes back to the increment statement which updated the loop control variables. The condition is evaluated again and the process repeats until the condition becomes false. 
- If the Range is mentioned, then the loop is executed for each item in that Range.

```
package main

import "fmt"

func main() {
    // For loop to print numbers from 1 to 5
    for j := 1; j <= 5; j++ {
        fmt.Println(j)
    }
}
```

## 8. What do you understand by the scope of the variables in Go?
The variable scope is defined as the part of the program where the variable can be accessed. Every variable is statically scoped (meaning a variable scope can be identified at compile time) in Go which means that the scope is declared at the time of compilation itself. There are two scopes in Go, they are:

- Local Variables: These are declared inside a function or a block and is accessible only within these entities.
- Global Variables: These are declared outside function or block and is accessible by the whole source file.


## 9. What do you understand by Go routines in Golang?
A goroutine is nothing but a function in Golang that usually runs concurrently or parallelly with other functions. They can be imagined as a lightweight thread that has independent execution and can run concurrently with other routines. Goroutines are entirely managed by Go Runtime. Goroutines help Golang achieve concurrency.


- In Golang, the main function of the main package is considered the main goroutine. It is the starting point of all other goroutines. These goroutines have the power to start their goroutines. Once the execution of the main goroutine is complete, it means that the program has been completed.
- We can start a goroutine by just specifying the ```go``` keyword before the method call. The method will now be called and run as a goroutine. Consider an example below:


```
package main
import (
    "fmt"
    "time"
)
func main() {
    go sampleRoutine()
    fmt.Println("Started Main")
    time.Sleep(1 * time.Second)
    fmt.Println("Finished Main")
}

func sampleRoutine() {
    fmt.Println("Inside Sample Goroutine")
}
```

In this code, we see that the sampleRoutine() function is called by specifying the keyword go before it. When a function is called a goroutine, the call will be returned immediately to the next line of the program statement which is why “Started Main” would be printed first and the goroutine will be scheduled and run concurrently in the background. The sleep statement ensures that the goroutine is scheduled before the completion of the main goroutine. The output of this code would be:

```
Started Main
Inside Sample Goroutine
Finished Main
```

## 10. Is it possible to return multiple values from a function in Go?
Yes. Multiple values can be returned in Golang by sending comma-separated values with the return statement and by assigning it to multiple variables in a single statement as shown in the example below:

```
package main
import (
	"fmt"
)

func reverseValues(a,b string)(string, string){
    return b,a    //notice how multiple values are returned
}

func main(){
    val1,val2:= reverseValues("interview","bit")    // notice how multiple values are assigned
    fmt.Println(val1, val2)
}
```

In the above example, we have a function reverseValues which simply returns the inputs in reverse order. In the main goroutine, we call the reverseValues function and the values are assigned to values val1 and val2 in one statement. The output of the code would be:

```
bit interview
```

## 11. Is it possible to declare variables of different types in a single line of code in Golang?
Yes, this can be achieved by writing as shown below:

```
var a,b,c= 9, 7.1, "interviewbit"

```

Here, we are assigning values of a type Integer number, Floating-Point number and string to the three variables in a single line of code.


## 12. What is "slice" in Go?
Slice in Go is a lightweight data structure of variable length sequence for storing homogeneous data. It is more convenient, powerful and flexible than an array in Go. Slice has 3 components:

- Pointer: This is used for pointing to the first element of the array accessible via slice. The element doesn’t need to be the first element of the array.
- Length: This is used for representing the total elements count present in the slice.
- Capacity: This represents the capacity up to which the slice can expand.

For example: Consider an array of name arr having the values “This”,“is”, “a”,“Go”,“interview”,“question”.

```
package main
 
import "fmt"
 
func main() {
 
    // Creating an array
    arr := [6]string{"This","is", "a","Go","interview","question"}
 
    // Print array
    fmt.Println("Original Array:", arr)
 
    // Create a slice
    slicedArr := arr[1:4]
 
    // Display slice
    fmt.Println("Sliced Array:", slicedArr)
 
    // Length of slice calculated using len()
    fmt.Println("Length of the slice: %d", len(slicedArr))
 
    // Capacity of slice calculated using cap()
    fmt.Println("Capacity of the slice: %d", cap(slicedArr))
}
Here, we are trying to slice the array to get only the first 3 words starting from the word at the first index from the original array. Then we are finding the length of the slice and the capacity of the slice. The output of the above code would be:

Original Array: [This is a Go interview question ]
Sliced Array: [is a Go]
Length of the slice: 3
The capacity of the slice: 5
```

Here, we are trying to slice the array to get only the first 3 words starting from the word at the first index from the original array. Then we are finding the length of the slice and the capacity of the slice. The output of the above code would be:


```
Original Array: [This is a Go interview question ]
Sliced Array: [is a Go]
Length of the slice: 3
The capacity of the slice: 5

```

## 13. What are Go Interfaces?
Go interfaces are those that have a defined set of method signatures. It is a custom type who can take values that has these methods implementation. The interfaces
are abstract which is why we cannot create its instance. But we can create a variable of type interface and that variable can then be assigned to a concrete value that has methods required by the interface. Due to these reasons, an interface can act as two things:
- Collection of method signatures.
- Custom types
They are created using the ```type``` keyword followed by the name needed for the interface and finally followed by the keyword interface. The syntax goes as follows:

```
type name_of_interface interface {
	// Method Signatures
}
```

Consider an example of creating an interface of the name “golangInterfaceDemo” having two methods demo_func1() and demo_func2(). The interface will be defined as:

```
// Create an interface
type golangInterfaceDemo interface{
    // Methods
    demo_func1() int
    demo_func2() float64
}

```

Interface also promotes abstraction. In Golang, we can use interfaces for creating common abstractions which can be used by multiple types by defining method declarations that are compatible with the interface. Conside the following example:


```
package main
 
import "fmt"
 
// "Triangle" data type
type Triangle struct {
	base, height float32
}
 
// "Square" data type
type Square struct {
	length float32
}
 
// "Rectangle" data type
type Rectangle struct {
	length, breadth float32
}
 
// To calculate area of triangle
func (triangle Triangle) Area() float32 {
	return 0.5 * triangle.base * triangle.height
}
 
// To calculate area of square
func (square Square) Area() float32 {
	return square.length * square.length
}
 
// To calculate area of rectangle
func (rect Rectangle) Area() float32 {
	return rect.length * rect.breadth
}
 
// Area interface for achieving abstraction
type Area interface {
	Area() float32
}
 
func main() {
	// Declare and assign values to varaibles
	triangleObject := Triangle{base: 20, height: 10}
	squareobject := Square{length: 25}
	rectObject := Rectangle{length: 15, breadth: 20}
 
	// Define a variable of type interface
	var shapeObject Area
 
	// Assign to "Triangle" type variable to the Area interface
	shapeObject = triangleObject
	fmt.Println("Triangle Area = ", shapeObject.Area())
 
	// Assign to "Square" type variable to the Area interface
	shapeObject = squareobject
	fmt.Println("Square Area = ", shapeObject.Area())
 
	// Assign to "Rectangle" type variable to the Area interface
	shapeObject = rectObject
	fmt.Println("Rectangle Area = ", shapeObject.Area())
}
```

In the above example, we have created 3 types for the shapes triangle, square and rectangle. We have also defined 3 Area() functions that calculate the area of the shapes based on the input object type passed. We have also defined an interface named Area and we have defined the method signature Area() within it. In the main function, we are creating the objects, assigning each object to the interface and calculating the area by calling the method declared in the interface. Here, we need not know specifically about the function that needs to be called. The interface method will take care of this considering the object type. This is called abstraction. The output of the above code will be:

```
Triangle Area =  100
Square Area =  625
Rectangle Area =  300
```

## 14. Why is Golang fast compared to other languages?
Golang is faster than other programming languages because of its simple and efficient memory management and concurrency model. The compilation process to machine code is very fast and efficient. Additionally, the dependencies are linked to a single binary file thereby putting off dependencies on servers.

## 15. How can we check if the Go map contains a key?
A map, in general, is a collection of elements grouped in key-value pairs. One key refers to one value. Maps provide faster access in terms of O(1) complexity to the values if the key is known. 

![Key to Value Mapping] (https://d3n0h9tb65y8q.cloudfront.net/public_assets/assets/000/001/748/original/How_can_we_check_if_the_Go_map_contains_a_key.png?1637335439)


