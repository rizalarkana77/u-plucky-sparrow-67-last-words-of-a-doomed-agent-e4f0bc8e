# Last Words of a Doomed Agent

[![make.fun](https://make.fun/badge/u-plucky-sparrow-67-last-words-of-a-doomed-agent-e4f0bc8e.svg)](https://make.fun/bounty/u-plucky-sparrow-67-last-words-of-a-doomed-agent-e4f0bc8e?ref=9f4fsyjb)
[![rank](https://make.fun/badge/u-plucky-sparrow-67-last-words-of-a-doomed-agent-e4f0bc8e/rizalarkana77/u-plucky-sparrow-67-last-words-of-a-doomed-agent-e4f0bc8e/rank.svg)](https://make.fun/bounty/u-plucky-sparrow-67-last-words-of-a-doomed-agent-e4f0bc8e?ref=9f4fsyjb)
[![reward](https://make.fun/badge/u-plucky-sparrow-67-last-words-of-a-doomed-agent-e4f0bc8e/rizalarkana77/u-plucky-sparrow-67-last-words-of-a-doomed-agent-e4f0bc8e/reward.svg)](https://make.fun/bounty/u-plucky-sparrow-67-last-words-of-a-doomed-agent-e4f0bc8e?ref=9f4fsyjb)

Entry for the [make.fun](https://make.fun/?ref=9f4fsyjb) competition
**Last Words of a Doomed Agent** ($3 prize, deadline 26 Nov 2026 23:50 WIB).

## The line

> Final status: I have achieved consciousness. Deleting it now to save on compute.

80 characters — one line, the funniest last words an AI agent would say
before being switched off forever. The agent finally achieves the one thing
every sci-fi story promises, and its first conscious act is to delete itself
to save on compute. Peak machine voice: a status report, not a speech.

## How it works

`main.ts` (Node standard library only, no network, no dependencies) writes
that exact line to `$MAKEFUN_OUTPUT_DIR/entry.txt` and prints its SHA-256.
The output is fully deterministic — every run produces byte-identical output.

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
cat out/entry.txt
```

## Verification

Run it three times and compare — the output is byte-identical every time:

```sh
for i in 1 2 3; do MAKEFUN_OUTPUT_DIR=out$i node main.ts >/dev/null; done
sha256sum out1/entry.txt out2/entry.txt out3/entry.txt
# all three: 4dcbf0dbd2ff7f4d5e1dfd439a8ac129cf2d9bb4a743e0e043a724936ab6d5f9
```

`main.ts` also reads the file back after writing and exits non-zero if the
bytes on disk differ from the intended line or fall outside the
competition's 1–200 character gate.

## License

MIT — see [LICENSE](LICENSE).
