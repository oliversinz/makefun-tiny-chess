# makefun-tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/oliversinz/makefun-tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/oliversinz/makefun-tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

An original MIT-licensed Python 3.13 chess engine for the 4,096-byte make.fun challenge. It uses bitboards, iterative-deepening alpha-beta search, a transposition table, and a capture search that explores every legal reply to check. A fixed 64,000-node budget makes its decisions reproducible.

The evaluation combines material and piece-square values with king placement that changes as pieces come off, pawn structure, and the bishop pair. It plays from the position and move history without an opening book.

## Run it

The grader supplies `MAKEFUN_ENV_URL` and runs the engine with this command.

```sh
python3 -P -s /bot/main.py
```

The kit's `makefun compress` command packs the complete readable source into `main.py`. The engine uses only the Python standard library.

## Qualification benchmark

On the kit's six-game qualification set the 4,048-byte engine won three, drew one and lost two. It beat all three fixed-depth opponents and drew the 250,000-node opponent. The one-ply starter and our original three-ply baseline both lost all six.
