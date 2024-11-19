This is a template for a repository to do [Advent of Code](http://adventofcode.com) in Rust.

# How to Set Up

First you need to obtain your Advent of Code session token. See [this
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

# Starting a New Day

```bash
cargo advent new-day
```

Without any arguments it will add the next day.

If the `--name` flag is provided, it will use that as the name of the crate instead of picking one.
If the `--day` flag is provided, it will assume it is for that day instead of the next one.

If you're starting the first day for example, you can find the code in `one/src/main.rs`.

Your puzzle input is downloaded to `one/input.txt`

# Running a Day

For example, to run the first day's code.
```bash
cargo run --package one < one/input.txt
```

# Submitting an Answer

```bash
cargo advent submit
```
Without any arguments, it will submit the next unsubmitted answer.

If you want to submit a specific answer, do it like this

```bash
cargo advent submit --name one --part 1
cargo advent submit --name one --part 2
```

Or like this
```bash
cargo advent submit --day 1 --part 1
cargo advent submit --day 1 --part 2
```

# Enabling the Tests
Once you have the correct answer for a problem, add the answer to the `harness!` macro to have a
test generated.

```rust
harness!(part_1: 1234, part_2: 5678)
```
