In Rust constants are a bit different than  many popular language such as JavaScript. variables declared by `const` can only have a static value, and must have it's data type annotated. It can not be reassigned, and can not have a value that is only determinable at run-time.
> Such as the return value of a function
constants are conventionally allcaps and use snake case.
> Fun fact: This particular combination of all-caps and snake case is called screaming snake case

```rust
const MAX_POINTS: u32 = 100_000;
```

Another fun bit about rust is the underscore that you see in the `100_000` value. Numeric literals allow you to use underscores for readability. Very neat.
