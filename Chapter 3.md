# Copy of Kreig's Notes

This is a running commentary. Not really parseable.

# 3.1 Variables and Mutability

- `let` can be mutated. `const` can **not.**
- `const` can only be an expression, never computed (hence `let` i guess)
- you can re`let` a variable, which means you can "shadow" the initial declaration without declaring a new variable (??? this is odd and seems anti-pattern so... ???)
- so re`let`ting a variable to a different *type* is ok—but declaring as `mut` to begin with means it's a fixed type! 😟
- in conclusion:
`let` `let` `let` is pretty much untyped
`let mut` is typed (and you don't re `let`)
`const` requires a type declaration and is sure as hell constant

# 3.2 Data Types

- and here for this first time signed and unsigned means something fundamental to myself as it affects size of maximum value based on `u` or `i` (as the signed one must accommodate a potential negative value in the same address space)
- interesting `_` can be used an a numeric separator but... hey
- ...and now I know what **Integer Overflow** is all about
- ...looks like you *can* (optionally) type a `let` (although seems like it might be used in override situations of the type inference)
- `char` is specified with single-quotes whereas strings are with double-quotes
- `tuple` is interesting — essentially it's a compound variable
- and you can either assign all values to separate vars or ref them with their index position
- arrays have fixed lengths (months of year given as use case)
- distinction is that this value will be on the stack instead of the heap... which they'll explain later ☺️
- vectors behave like JS arrays and the guidance is "use unless you know you need an array"

# 3.3 Functions

- convention is snake_case for vars and function names... boo hoo
- there they go talking about expressions again... "Rust is an expression-based language"
- ah ok. expression means returns a value
- in contrast to statement which does not
- a tautology
- "The block that we use to create new scopes, {}, is an expression"
- expressions **do not end with a semi-colon** or else it becomes a statement! (!!!) mildly maddening but i'm sure it makes sense later
- return values are not named and they are typed in the function declaration (after a skinny arrow)! interesting
- not sure why they're using `i32` everywhere when a `u8` will do... might be to not confuse the typing noobs.

# 3.5 Control Flow

- no implicit `bool` of course... always include a value compare
- can use a conditional in a `let`... that's kind of cool
- `break` keyword for exiting `loop`
- i see value compare is using an eq-eq
- `while` for creating conditional loop
- nice to see `+=` and `-=` in use
- `for` is equivalent to `forEach`
- use `.iter()` method to... iterate
- can use a range in `for` loops e.g. `for number in (1..4).rev() { }`