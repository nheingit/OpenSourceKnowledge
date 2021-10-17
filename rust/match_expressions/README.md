# Matches

Example adapted from the RustLang Book [Example](https://doc.rust-lang.org/book/ch02-00-guessing-game-tutorial.html)

```rust
use rand::Rng;
use std::cmp::Ordering;

fn main() {
    
    let secret_number = rand::thread_rng().gen_range(1..101); // random number between 1-100
    let small_number = 3

    match small_number.cmp(&random_number) {
        Ordering::Less => println!("Too small!"),
        Ordering::Greater => println!("Too big!"),
        Ordering::Equal => println!("You win!"),
    }
}
```

here you are comparing the variables — `guess`, and `secret_number` — to each other, and then feeding that result into the `match` expression.

`match` expressions are made up of **arms**, each of which has a **pattern**. the `match` statement takes the value given to it and looks through each arm. Should the arm's pattern be met, for example: `Ordering::Less`, the expression of code following the `=>` will be executed.
