# Guessing Game

Initial contents of src\main.rs

```Rust
fn main() {
    println!("Hello, world!");
}
```

To be replaced with:

```Rust
// Bring the io library from the standard library into scope
use std::io;

fn main() {
    println!("Guess the number!");

    println!("Please input your guess.");

    // LHS: create a mutable variable; In Rust, variables are immutable by default
    // = means bind; bind the new empty String to the variable guess
    // :: to be used for assiciated functions e.g. new is associated with the String type
    let mut guess = String::new();

    // Read input from the user, append it to the guess string without overwriting its contents
    /* & represents reference, for the variable to be accessed by multiple parts in the program
        without needing the data to be copied multiple times in memory */
    io::stdin()
        .read_line(&mut guess)
        .expect("Failed to read line");

    println!("You guessed: {}", guess);
}
```

To be continued from *Handling Potential Failure with the Result Type*