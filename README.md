# synergy

An esoteric programming language where the only keywords are corporate buzzwords. Every program reads like a standup meeting, and the computer runs it.

- **Try it:** [Synergy console](https://amandata.dev/synergy.html) — type a buzzword, hit enter, watch the variables
- **Learn it:** [Synergy wiki](https://amandata.dev/synergy-wiki.html) — every command in plain language
- **Read about it:** [a programming language but it's all corporate buzzword](https://amandata.dev/blog.html?p=synergy-corporate-buzzword-esolang)

## The language (v2)

Synergy v2 runs on **named counters**: integer variables with names like `headcount` or `budget`. Every counter starts at 0 and holds an unbounded integer. Two counters with increment, decrement, and a zero-test are already Turing complete (a Minsky machine).

| Buzzword | Does |
|---|---|
| `hire x` | add 1 to x |
| `layoff x` | subtract 1 from x |
| `increase x by 40` | add 40 to x |
| `decrease x by 40` | subtract 40 from x |
| `set x to 72` | set x to 72 |
| `while x is nonzero` … `circle back` | loop while x is not 0 |
| `share out x` | output x as a character (ASCII) |
| `report x` | output x as a number |
| `gather feedback into x` | read a character into x |
| `hit a bottleneck` | halt the program |

Any line starting with `per my last email` is a comment.

Numbers are also letters. 72 is H, 105 is i, 32 is a space, that's ASCII.

## v1

Version 1 used a brainfuck-style tape (cells + pointer). v2 replaced it with named counters because the tape fits corporate speak poorly: it's one anonymous pointer through identical cells, while standup language is good at names and quantities. The v1 interpreter is preserved in git history.

## Files

- `synergy.js` — the interpreter. `Synergy.run(source, input)` and `Synergy.createSession()` for stateful use, in the browser or node. Also includes `Synergy.fromBrainfuck()` for a best-effort translation.
- `hello.synergy` — hello world, written as meeting notes.
- `index.html` — a little playground.

## Example

```
per my last email, just saying hi

set h to 72, share out h,
set i to 105, share out i.

hit a bottleneck.
```

outputs `Hi`.

Built by [Mandy](https://amandata.dev) because every meeting could have been an email, but this one compiles.
