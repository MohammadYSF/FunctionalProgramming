# F# : Introduction

**F#** is a **functional programming language** released in 2005 by **Microsoft**.Its main goal is to able .NET programmers to write code in a functional way. Although , it **supports OOP** paradigm . F# is **cross-platform** meaning that it can run on windows , mac and linux using the .NET SDK . One good thing about this language is that It can use any library written in C# or Visual Basic And vice versa.


## F# :  Comparison with λ-Calculus
Below code is a **λ-Calculus** expression which caluculates the square of something.

```λx. (* * x))```

we assume that **\*** is a  function  with single argument that multiplies the given argument with 1 . so ```* * x ``` means ```*(*(x))``` .First we calculate ```*(x)```
the returning of this is again a function like **f** . then we have ```*((*)(x)) = *(f(x))```
For example . if we want to apply this function with the argumeant  *2* , we say : 

```((λx. (* * x)) 2)```

**[!]** Remember that is  λ-Calculus pure abstract and  every thing in it  is a function . So , when we write **2** , we assume that **2** is a function that represents us the value 2 that we use in our world. and it's clear that we assume  the return entity of the above code is also a function that represents number **4** to us. There is no real 2 or 4 in λ-Calculus !
Now We want to do the same thing in **F#**

```let square x = x*x```

In the above code , we defined a function *square* which accepts one argument namely ```x``` and returns ```x*x``` .That's it!
Now , if we want to apply this function and print the result on the Console.we say : 

```printfn "%i" (square 2)```

```square 2 ``` is the way we apply a function with a its argument (name of the function , space and then supply the arguments)
```printfn``` is also a function built into the F# which in this case  takes 2 arguments and you can guess that what it does !
**[!]** Note that every thing in F# is immutable . meaning that you can not change ``square`` any time later . Once it is declared , then it gives you compile error if you try to change 
also , there is another way of doing the same thing : 

```let square2 = fun x -> x*x```

we say that ```square2``` is a function with no argument at first . but inside it , there is an anonymous function specified by ```fun``` key word that takes an argument and returns something . 
application is the same as ```sqaure2```
you can see some more examples of F# code and its syntax in the  **f#codes** folder.

# Haskell : Introduction

> Haskell is a general-purpose, statically-typed, purely functional programming language with type inference and lazy evaluation.

Haskell was released in 1990 . Like F# needs to be compiled first . 
## Haskell :  Comparison with λ-Calculus
Below code is a **λ-Calculus** expression which caluculates the square of something.

```λx. (* * x))```

we assume that **\*** is a  function  with single argument that multiplies the given argument with 1 
If we want to apply this function with the argumeant  *2* , we say : 

```((λx. (* * x)) 2)```

To do this in Haskell , we say : 
```
import System.IO
square x = x*x
main = putStrLn ("2^2 is = " ++ show (square 2) )

```
In the 1st line , we import ```System.IO ``` library , which is neccesary to read or write data from Console.
2nd line  is our function .  we defined a function *square* which accepts one argument namely ```x``` and returns ```x*x``` 
And in the 3rd line we print the the result to the Console. 

