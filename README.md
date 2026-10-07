# Algorithm Visualizer

An interactive, animated visualizer for 7 classic algorithms, built with plain HTML, CSS and JavaScript. No libraries, no build step.

**Live demo:** https://kavya3077.github.io/algorithm-visualizer/

## Features

- 7 algorithms: Bubble Sort, Selection Sort, Insertion Sort, Merge Sort, Binary Search, BFS, DFS
- Animated characters (colored one-eyed blobs) for sorting and searching
- SVG graph animation for BFS and DFS
- Source code panel with the current line highlighted
- Step-by-step explanation message
- Time and space complexity cards
- Controls: Play/Pause, Step, Back, New array, Speed slider
- Mobile friendly

## How it works

Each algorithm is an entry in the `ALGOS` object: `name`, `code[]`, `facts`, `run(vals)`.

1. `run()` returns an array of steps, e.g. `{order, line, cmp, swp, done, fin, hit, dim, msg}`.
2. The player only moves an index over the steps.
3. `render()` draws the current step.
4. Characters keep fixed ids; a CSS transition on `left` creates the swap animation.
5. BFS and DFS use an SVG graph (`G.adj`, `G.pos`) with steps `{line, cur, vis, front, msg}`.

Adding a new algorithm means adding one entry to `ALGOS`.

## Run locally

```bash
git clone https://github.com/kavya3077/algorithm-visualizer.git
cd algorithm-visualizer
```

Then open `index.html` in a browser.

## Project structure

```
algorithm-visualizer/
├── index.html
├── README.md
├── LICENSE
└── .gitignore
```

## Complexity summary

| Algorithm | Best | Average | Worst | Space |
|-----------|------|---------|-------|-------|
| Bubble Sort | O(n) | O(n²) | O(n²) | O(1) |
| Selection Sort | O(n²) | O(n²) | O(n²) | O(1) |
| Insertion Sort | O(n) | O(n²) | O(n²) | O(1) |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) |
| Binary Search | O(1) | O(log n) | O(log n) | O(1) |
| BFS / DFS | O(V+E) | O(V+E) | O(V+E) | O(V) |

## Roadmap

- Quick Sort
- Array size slider
- Custom array input
- Comparison counter

## License

MIT, see [LICENSE](LICENSE).

## Author

Kavya Mudgil, [@kavya3077](https://github.com/kavya3077)
