This is a template for a repository to do [Advent of Code](http://adventofcode.com) in Rust.

# How to set-up

First you need to put your Advent of Code session token. See [this
link](https://github.com/wimglenn/advent-of-code-wim/issues/1) for instructions on how to obtain it,
then paste the part after `session=` in `~/.config/aoc/token`

Next, set-up your repository.

```bash
cargo install cargo-generate
cargo generate bobbobbio/Advent-of-Code-Template --name advent-of-code-<YEAR>

cd advent-of-code-<YEAR>
cargo advent init --year <YEAR>
git add .
git commit -m "Initial commit"
```

# Starting a question

```bash
cargo advent new-question --name one
```

The `--name` flag is the name to use for the package, the day number is extrapolated from the name
unless but if you want to override that you can provide the `--day` flag.

Edit your solution in `one/src/main.rs`.

Your puzzle input is downloaded to `one/input.txt`

# Running a question

```bash
cargo run --package one < one/input.txt
```

# Submitting an answer

```bash
cargo advent submit --name one --part 1
cargo advent submit --name one --part 2
```

# Enabling the tests
Once you have the correct answer for a problem, add the answer to the `harness!` macro to have a
test generated.

```rust
harness!(part_1: 1234, part_2: 5678)
```
