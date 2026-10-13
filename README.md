# Puzzle Arena: Algorithm Battle

BFS, DFS, A* and Greedy search race to solve the **same puzzle**, with live stats on nodes explored, time and path length.

**Live demo:** `https://<your-username>.github.io/puzzle-arena/`

## Features
- Three puzzles: 8-Puzzle, Maze, Water Jug
- Four algorithms: BFS, DFS, A*, Greedy best-first
- Live stats per algorithm: nodes explored, time, path length, finish rank
- Speed slider, new random puzzle each time, solution path replay
- Single `index.html`, no build step, no dependencies

## Run locally
Open `index.html` in any browser.

## How it works
Each puzzle defines `start`, `goal(state)`, `next(state)` and `h(state)`. One generic `search(puzzle, algorithm)` function runs all four algorithms and returns the explored order, path and measured time. The race replays the explored order for all four at the same nodes-per-frame speed.

| Puzzle | Heuristic |
|---|---|
| 8-Puzzle | Manhattan distance of tiles |
| Maze | Manhattan distance to exit |
| Water Jug | 0 at goal, else 1 (admissible) |

Searches stop at 60,000 nodes (DFS can hit this on the 8-puzzle).

## Slides
See `slides/Puzzle-Arena.pptx`.

## Author
Krisha Kohli, B.Tech CSE, Manipal University Jaipur

## License
MIT
