This is a template for a repository to do [Advent of Code](http://adventofcode.com) in Rust.

# How to set-up

```bash
cargo install cargo-generate
cargo generate bobbobbio/Advent-of-Code-Template --name advent-of-code-<YEAR>

cd advent-of-code-<YEAR>
echo <YEAR> > aoc-year
echo "These are my solutions for Advent of Code <YEAR>" > README.md
```

# Starting a question

```bash
cargo advent new-question --name one
```
