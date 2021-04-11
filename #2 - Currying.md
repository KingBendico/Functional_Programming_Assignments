# 2 Duality of programming



### The principle of currying

Currying means breaking down functions that take multiple arguments, into a sequence of functions, each taking one argument.

```haskell
--This function is curried, because it is actually a sequence of functions, where each "step" only takes one argument
f :: a -> (b -> c)

--This function is not curried, because it is a single function that requires multiple arguments
f :: (a, b) -> c
```

### How to implement and use currying in Elm and Haskell

Currying in Elm and Haskell allow partial function application, where a function called with only some of its arguments can return another function that takes the remaining arguments.

```haskell
--This function takes multiple arguments. Calling it with only part of them returns a partially applied function.
--Since this is a function like any other, we can save it as a variable:
f :: Int -> Int -> Int
f x y = x + y

partial = f 2

--This function now accepts one argument(y), and will return 2+y
```

Functions in Elm and Haskell are both curried by default.

### Typical currying use cases

```haskell

```

