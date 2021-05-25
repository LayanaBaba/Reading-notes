## Functional Programming Concepts

**What is functional programming?**

A style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data. 

**What is a pure function and how do we know if something is a pure function?**

Pure functions are essential for a variety of purposes, including functional programming, reliable concurrency, and React+Redux apps.Pure functions are stable, consistent, and predictable. Given the same parameters, pure functions will always return the same result. We don’t need to think of situations when the same parameter has different results — because it will never happen.

**What are the benefits of a pure function?**

The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts:

* Given a parameter A → expect the function to return value B.

* Given a parameter C → expect the function to return value D


**What is immutability?**

Unchanging over time or unable to be changed.

**What is Referential transparency?**

Pure function will always have the same output, given the same input.

## Node JS Tutorial for Beginners #6 - Modules and require()

**What is a module?**

Module in Node.js is a simple or complex functionality organized in single or multiple JavaScript files which can be reused throughout the Node.js application.

**What does the word ‘require’ do?**

require function is the easiest way to include modules that exist in separate files. 

**How do we bring another module into the file the we are working in?**

To include functions defined in another file in Node.js, we need to import the module. we will use the require keyword at the top of the file.

The result of require is then stored in a variable which is used to invoke the functions using the dot notation.

To see that in action, let’s import the lib.js module by requiring it inside the main.js file and invoke the add() function with dot notation.





