From the author's defination of closure in eloquent javascript,we understood that a function that “closes over” some local 
variables is called a closure.



In simple terms, a closure is the combination of a function enclosed with references to its surrounding state (environment).

Closure is just like an inner function that has access to the outer function's variables—scope

chain. The closure has three scope chains: 

1.It has access to its own variables defined between the curly brackets

2.It has access to the outer function's variables(also to the outer function’s parameters)

3.It has access to the global variables.




Closures allow JavaScript programmers to write better code as when functions execute, they use the same scope-chain that was

in effect when they were created. Meaning that even after the outer function has returned, the inner function still has access

to the outer function’s variables. This gives the right to call the inner function later in the program. Closures are commonly

used to give objects data privacy. Data privacy is an essential property that helps the programmer work to an interface, not an implementation.




This feature also creates a problem as closures still have access to the updated values of the outer function’s variables, they

can lead to bugs when the outer function’s variable changes with a for or while loop. To be clear,until unless the outer function

has not finished executing, it gonna return the value for the same i.e  a new value each time the loop runs. So, the other 

functions taking the value of the outer function's variable might clash with the inside functions who are using that variable's

value. 


Here is an example code to create understanding the concept:


function add(value1)
{
    return function doAdd(value2)
            {
                return value1 + value2;
              };
}

var increment = add(1);
var getValue = increment(2);

// getValue equals 3

(code taken from reference1)



To know more about scope, scope chains, closures examples, take a look at these reference.

Reference1: (https://www.sitepoint.com/javascript-closures-demystified/ )

Reference2: https://howtonode.org/why-use-closure

Reference3: https://www.youtube.com/watch?v=zRZNb4GDOPI

