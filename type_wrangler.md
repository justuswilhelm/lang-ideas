# Type Wrangler Concept

## Requirements

- Haskell-like function bodies
- Type Inference, but should feel as dynamic as possible, but still static
- No type classes
- Interpreted first
- Side effects
- Powerful string expression matching
- IO primitives
- Structs with composition
- Should feel as dynamic as possible
- Useful string methods
- Garbage collection
- Everything is use once type
- J like array usefulness (over/under operator)
- No loop, only map, foldl, filter
- Minimal primitive data types:
    - Type Safe Union
    - int64
    - float64
    - string
    - homogenous array
    - struct

Sample code

Notice how the first argument is implicitly passed around

```
main =
    print_greeting " World"

print_greeting greeting =
    greeting,
    prepend "Hello, ",
    append "!",
    println
```
