# Reading Notes 301

sources:
- https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/
- https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c

## The JavaScript Call Stack

The JavaScript engine is a single-threaded interpreter comprising of a heap and a single call stack. The call stack is primarily used for function invocation (call). Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous. In Asynchronous JavaScript, we have a callback function, an event loop, and a task queue. The callback function is acted upon by the call stack during execution after the call back function has been pushed to the stack by the event loop.

At the most basic level, a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call). When we say that the call stack, operates by the data structure principle of Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.

## In summary
### The key takeaways from the call stack are:
1. It is single-threaded. Meaning it can only do one thing at a time.
2. Code execution is synchronous.
3. A function invocation creates a stack frame that occupies a temporary memory.
4. It works as a LIFO — Last In, First Out data structure.

## Types of error messages

### Reference errors
This is as simple as when you try to use a variable that is not yet declared you get this type os errors.
`console.log(foo) // Uncaught ReferenceError: foo is not defined`

### Syntax errors
I know it’s in the name of the errors, but like it says itself, this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.
`JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1`

### Range errors
Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.
`var foo= []
foo.length = foo.length -1 // Uncaught RangeError: Invalid array length`

### Type errors
Like the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.
`var foo = {}
foo.bar // undefined
foo.bar.baz // Uncaught TypeError: Cannot read property 'baz' of undefined`
