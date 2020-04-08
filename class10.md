# Call stack
 mechanism for an interpreter 
 to keep track of its place in a script that calls multiple functions 

-  what function is currently being run and what functions are called from within that function, etc.

- When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.

- Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.

- When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.

- If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.


## LIFO (last In First Out)

 When we say that the call stack, operates by the data structure principle of Last In, First Out, it means that the lastfunction that gets pushed into the stack is the first to be pop out, when the function returns.

## Manage function invocation (call)

 The call stack maintains a record of the position of each stack frame. It knows the next function to be executed (and will remove it after execution). This is what makes code execution in JavaScript synchronous.

## What causes a stack overflow?
 
 A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.

## Types of error messages:

1. Reference errors
2. Syntax errors
3. Range errors
4. Type errors