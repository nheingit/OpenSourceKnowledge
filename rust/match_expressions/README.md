# Matches

```rust
//Taken from the RustLang Book [Example](https://doc.rust-lang.org/book/ch02-00-guessing-game-tutorial.html)
use rand::Rng;
use std::cmp::Ordering;
use std::io;

fn main() {
    // --snip--

    println!("You guessed: {}", guess);

    match guess.cmp(&secret_number) {
        Ordering::Less => println!("Too small!"),
        Ordering::Greater => println!("Too big!"),
        Ordering::Equal => println!("You win!"),
    }
}
```

here you are comparing the (instiatied beforehand) variables — `guess`, and `secret_number` — to each other, and then feeding that result into the `match` expression.

`match` expressions are made up of **arms**, each of which has a **pattern**. the `match` statement takes the value given to it and looks through each arm. Should the arm's pattern be met, for example: `Ordering::Less`, the expression of code following the `=>` will be executed.
