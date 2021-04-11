### First class citizens

In functional programming languages like Elm or Haskell, functions are treated like ordinary datatypes, along with integers, booleans and so on. This means that you can store them as variables, or pass them and return them in other functions.  

In Haskell, it looks something like this:  

```haskell
--Save function in variable
pow2 x = x^2

--Pass function as parameter
list = [1, 2, 3, 4, 5]
powerList = map pow2 list

--Returning functions, calling this function with only 1 parameter will, due to functions with multiple parameters being curried, return a function that can take the other parameter
add x y = x+y

--Another way this could look is as follows:
mapWithPlusTwo = map (+2)
--This should return a function that can take a list and add two to every entry.

```

## Higher order functions
The two last examples above are examples of higher order functions, since they return functions.  
**map** is also a higher order function, because higher order functions are functions that either take functions as parameters, or return functions.

## Lambdas
Lambdas are anonymous functions. They are useful for single use functions, where there is no use naming them, for example: A function that only appears once, and is passed to the map function.  
An example of Haskell syntax for lambdas could be:
```haskell
(\x -> x+x)
```
Where the backslash indicates the start of a lambda expression.