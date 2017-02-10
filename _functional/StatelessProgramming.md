---
layout: functional
name: 'Stateless Programming'
iid: StatelessProgramming
status: DONE
abstract: "Operations you implement are not sensitive to the state of the computation: in practice, this means the program uses data passed by value (vs. by reference)"
---

__Stateless programming__ is a paradigm in which the operations (functions, methods, procedures, whatever you call them) you implement are not 
sensitive to the state of the computation. That means all the data used in an operation are passed as inputs to the operation, and all the 
data used by whatever operations invoked that operation are passed back as outputs. 

In practice, this means the program must have Value semantics (it is not permitted to modify shared/aliased data structures, and objects do 
not have an identity), must not use global or class variables, and all input/output must be handled specially (such as through monads or by 
threading an I/O state through any parts of the computation that perform I/O). Exception handling may also make the computation stateful.

[Swift](/Swift) provides [Structures](/Structure) and [Enumerations](Enumeration) that are passed by values and can be stateless; 
therefore, they are very efficient. Stateless programming simplifies the concurrency and multithreading.