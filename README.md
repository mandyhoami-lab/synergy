# synergy

An esoteric programming language where the only keywords are corporate buzzwords. Every program reads like a standup meeting, and the computer runs it.

- **Try it:** [Synergy console](https://amandata.dev/synergy.html) — type a buzzword, hit enter, watch the tape debugger
- **Learn it:** [Synergy wiki](https://amandata.dev/synergy-wiki.html) — every command in plain language
- **Read about it:** [a programming language but it's all corporate buzzword](https://amandata.dev/blog.html?p=synergy-corporate-buzzword-esolang)

## The language

| Buzzword | Does |
|---|---|
| `move the needle` | increment the current cell |
| `take a step back` | decrement the current cell |
| `pivot` | move to the next cell |
| `deep dive` | move to the previous cell |
| `share out` | output the current cell as a character |
| `double-click on that` | output the current cell as a number |
| `run it up the flagpole` | output every cell on the tape |
| `gather feedback` | read one input character into the cell |
| `sync up` … `circle back` | loop while the current cell is nonzero |
| `low-hanging fruit` | set the current cell to 0 |
| `herding cats` | set the current cell to a random value |
| `put a pin in it` / `pull the pin` | save / restore the tape |
| `hit a bottleneck` | halt the program |

Any line starting with `per my last email` is a comment.

Numbers are also letters. 72 is H, 105 is i, 32 is a space.

## Files

- `synergy.js` — the interpreter. `Synergy.run(source, input)` and `Synergy.createSession()` for stateful use, in the browser or node. Also includes `Synergy.fromBrainfuck()` to translate brainfuck programs into corporate.
- `hello.synergy` — hello world, written as meeting notes.
- `index.html` — a little playground: paste a standup, hit "run the meeting".

## Example

```
per my last email, just saying hi

move the needle, move the needle, move the needle, move the needle,
move the needle, move the needle, move the needle, move the needle,
sync up, pivot, move the needle, move the needle, move the needle,
...
hit a bottleneck.
```

outputs `Hi`.

Built by [Mandy](https://amandata.dev) because every meeting could have been an email, but this one compiles.
