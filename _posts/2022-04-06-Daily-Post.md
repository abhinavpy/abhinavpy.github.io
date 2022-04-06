---
title: 'Daily Blog Post 6 April 2022'
date: 2022-04-06
permalink: /posts/2022/04/daily-post/
tags:
  - GRE Reading Comprehension
  - interview problems 
  - algorithms
  - data structures
  - Golang Basics
---
### GRE Verbal:
- Completed Advanced Reading Comprehension 4. Scored 14/20. Could have scored slightly better. Took a lot of time - 1hr19min which has to be reduced.
- Completed Advanced Sentence Equivalence 5. Hence finishing the section of Advanced Sentence Equivalence. Scored 12/20. Not a very good score. Will have to start revising all SE Questions to revise word meanings.

### GRE Quant:
- Completed Advanced Sequences Practice.
- Completed Basic Geometry and Triangles Advanced Practice.

## Golang Practice from exercism.org
Url link: https://exercism.org/tracks/go/exercises/lasagna
### About Comments
In go, comments play an important role in documenting code. They are used by the godoc command, which extracts these comments to create documentation about Go packages.
A documentation comment should be a complete sentence that starts with the name of the thing being described and ends with a period.

Comments should precede packages as well as export identifiers, for example exported functions, methods, package variables, constants and structs, which you will learn more about in the next exercises.
A package level variable can look like this:
```
var TemperatureCelsius float64
```
### Package Comments
Package comments should be written directly before a package clause (**package x**) and begin with **Package x ...** like this:
```
//Package Kelvin provides tools to convert
// temperatures to and from kelvin
package kelvin
```

### Function Comments
A function comment should be written directly before the function declaration. It should be a full sentence that starts with a function name. For example, an exported comment for the function 
**Calculate** should take the form **Calculate ...** It should also explain what arguments the function takes, what it does with them, and what its return values mean, ending in a period.
```
// CelsiusFreezingTemp returns an integer value equal to the temperature at which water freezes in degree celsius
func CelsiusFreezingTemp() int {
  return 0
}
```

### Go comments exercise - Weather Forecast

Instructions:

Being hired by a big weather forecast company, your job is to maintain their codebase. Scrolling through their code, you find it hard to follow what the code is actually doing.
Good thing you know just the right thing to do.

Step 1: Document Package Weather

Write a package comment for **package weather** that describes its contents. The package comment should introduce the package and provide information relevant to the package as a whole.

Step 2: Document the Current Condition Variable

Write a comment for the package variable **CurrentCondition**

This should tell any user of the package what information the variable stores, and what they can do with it.

Step 3: Document the currentLocation variable

Just like the previous step, write a comment for currentLocation.

Step 4: Document the Forecast() function

Write a function comment for Forecast(). Your comments must describe what the function does, but not how it does it.

```
func TestComments(t *testing.T) {
	filename := "weather_forecast.go"

	fs := token.NewFileSet()
	f, err := parser.ParseFile(fs, filename, nil, parser.ParseComments)
	if err != nil {
		t.Fatal(err)
	}

	wantedComments := 4
	got := len(f.Comments)
	if got != wantedComments {
		t.Errorf("Incorrect number of comments: got %d, want %d", got, wantedComments)
	}

	testPackageComment(t, f)

	ast.Inspect(f, func(node ast.Node) bool {
		switch n := node.(type) {
		case *ast.GenDecl:
			if n.Lparen.IsValid() {
				for _, v := range n.Specs {
					testBlockIdentifierComment(t, v.(*ast.ValueSpec))
				}
			} else {
				testIdentifierComment(t, n)
			}
		case *ast.FuncDecl:
			testFunctionComment(t, n)
		}
		return true
	})
}
```

### Numbers in Go
About Numbers

Go contains basic numeric types that can represent sets of either integer or floating point values.

This concept will concentrate on two number types:
 

