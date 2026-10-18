# synergy

An esoteric programming language where the only keywords are corporate buzzwords. Brainfuck-complete, so it can compute anything — but every program reads like a bad standup meeting.

## The language

| Buzzword | Does |
|---|---|
| `move the needle` | increment the current cell |
| `take a step back` | decrement the current cell |
| `pivot` | move to the next cell |
| `deep dive` | move to the previous cell |
| `share out` | output the current cell as a character |
| `gather feedback` | read one input character into the cell |
| `sync up` … `circle back` | loop while the current cell is nonzero |
| `hit a bottleneck` | halt the program |

Any line starting with `per my last email` is a comment.

## Files

- `synergy.js` — the interpreter. `Synergy.run(source, input)` in the browser, or `require('./synergy.js')` in node. Also includes `Synergy.fromBrainfuck()` to translate brainfuck programs into corporate.
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
