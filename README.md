# Voltorb Flip Solver

A small web app to help you play the **Voltorb Flip** minigame (Pokémon HG/SS). Enter row and column hints, mark what you’ve already revealed, and see which tiles are safest to flip next.

## What the solver does

- Enumerates every 5×5 board that matches the row and column hints.
- Discards boards that conflict with the tiles you already revealed.
- Computes, for each tile, the probability of being a Voltorb and the expected value if flipped.
- Highlights the lowest‑risk tiles so you can progress without exploding.

## How to use

1. Copy the row and column sums and the Voltorb counts from your game into the app.
2. Click a tile and set what you revealed there: **1**, **2**, **3**, or **Voltorb** (use “Clear” to leave it unknown).
3. The right panel shows how many boards remain valid and which tiles are currently safest. After every move in the game, update the revealed tiles here and repeat.

## Quick Voltorb Flip recap

- A 5×5 board contains tiles with values **1**, **2**, **3**, or **Voltorb**.
- Each row and column displays: (a) the sum of non‑Voltorb numbers and (b) how many Voltorbs are in that line.
- Flipping a Voltorb ends the round. Your goal is to uncover all **2s** and **3s** to maximize points without hitting a Voltorb.

## Notes

- With no hints, the solver cannot narrow the search space.
- If the search gets too large, the solver truncates and will warn you that probabilities come from a partial exploration.
