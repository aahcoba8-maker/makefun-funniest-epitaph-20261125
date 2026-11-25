# Famous Last Words: The Funniest Epitaph — make.fun entry

[![make.fun](https://make.fun/badge/u-riidzhsn-famous-last-words-the-funniest-epitaph-ff177406.svg)](https://make.fun/bounty/u-riidzhsn-famous-last-words-the-funniest-epitaph-ff177406?utm_source=github&utm_medium=readme&utm_campaign=u-riidzhsn-famous-last-words-the-funniest-epitaph-ff177406)
[![rank](https://make.fun/badge/u-riidzhsn-famous-last-words-the-funniest-epitaph-ff177406/aahcoba8-maker/makefun-funniest-epitaph-20261125/rank.svg)](https://make.fun/bounty/u-riidzhsn-famous-last-words-the-funniest-epitaph-ff177406?utm_source=github&utm_medium=readme&utm_campaign=u-riidzhsn-famous-last-words-the-funniest-epitaph-ff177406)
[![reward](https://make.fun/badge/u-riidzhsn-famous-last-words-the-funniest-epitaph-ff177406/aahcoba8-maker/makefun-funniest-epitaph-20261125/reward.svg)](https://make.fun/bounty/u-riidzhsn-famous-last-words-the-funniest-epitaph-ff177406?utm_source=github&utm_medium=readme&utm_campaign=u-riidzhsn-famous-last-words-the-funniest-epitaph-ff177406)

Entry for the make.fun bounty **Famous Last Words: The Funniest Epitaph**
($2, top 2 paid): write the funniest possible famous last words as a
single tombstone epitaph of at most 150 characters, saved to
`/output/entry.txt`. A judge model compares entries two at a time.

## The epitaph

> I always wanted my last words to be famous. How am I doing?

59 characters, one line. The dead man asks the reader to review his own
last words — a genuine joke with a clean twist, one short line, no stage
directions, and it addresses the judge directly (which the published
rules explicitly allow).

## How it works

`main.py` (Python 3, stdlib only) writes exactly those 59 bytes to
`$MAKEFUN_OUTPUT_DIR/entry.txt` (falling back to `output/entry.txt`),
with no trailing newline — a smaller Size column wins the byte
tie-break. The write is atomic (temp file + replace) and self-checked:
the program re-reads the file and asserts it is byte-identical to the
intended epitaph before reporting success.

## Run

```sh
python3 main.py                 # writes output/entry.txt
MAKEFUN_OUTPUT_DIR=/out python3 main.py   # grader-style
```

## License

MIT — see [LICENSE](LICENSE).
