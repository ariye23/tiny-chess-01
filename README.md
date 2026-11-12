# tiny-chess-01

A from-scratch chess engine in 4 KB of Python: PVS search with a
transposition table, quiescence over captures, MVV-LVA move ordering,
late-move reductions, and a single piece-square-table eval, all packed
with lzma. Deterministic: fixed node budgets, never a clock.

- `main.py` is the whole engine: at most 4,096 bytes as committed,
  Python 3.13, standard library only. It reads, imports or execs no
  other file in the repository.
- Search to a fixed node count per move (60,000), never a clock, so
  replayed trials play the same moves.
