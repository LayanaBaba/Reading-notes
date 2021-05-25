## Understanding the JavaScript Call Stack

**What is a ‘call’?**

The call stack is primarily used for function invocation (call). Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.

**How many ‘calls’ can happen at once?**

* 1. When secondFunction() gets executed, an empty stack frame is created. It is the main (anonymous) entry point of the program.

* 2. secondFunction() then calls firstFunction()which is pushed into the stack.

* 3. firstFunction() returns and prints “Hello from firstFunction” to the console.

* 4. firstFunction() is pop off the stack.

* 5. The execution order then move to secondFunction().

* 6. secondFunction() returns and print “The end from secondFunction” to the console.

* 7. secondFunction() is pop off the stack, clearing the memory.

**What does LIFO mean?**

The last function that gets pushed into the stack is the first to be pop out, when the function returns.

**Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.**

![Call stack example](img/read10.png)

**What causes a Stack Overflow?**

A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.

## JavaScript error messages

**What is a ‘refrence error’?**

This is as simple as when you try to use a variable that is not yet declared you get this type os errors.

console.log(foo) // Uncaught ReferenceError: foo is not defined

This is also a common thing when using const and let, they are hoisted like var and function but there is a time between the hoisting and being declared so when you try to access them a reference error occurs, the fact that this happens to let and const is called Temporal Dead Zone (TDZ).

foo = 'Hello' // Uncaught ReferenceError: foo is not defined

let foo

**What is a ‘syntax error’?**

Some syntax errors like sending a trailing comma when calling a function are handled without error by most recent browsers, but older ones you have to be careful.

**What is a ‘range error’?**

Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.

var foo= []

foo.length = foo.length -1 // Uncaught RangeError: Invalid array length

**What is a ‘type error’?**

This types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

**What is a breakpoint?**

The breakpoint can also be achieved by putting a debugger statement in your code in the line you want to break.

**What does the word ‘debugger’ do in your code?**

I’ve added a debugger statement and when running the code above you can see the “history” before reaching that breakpoint. 


