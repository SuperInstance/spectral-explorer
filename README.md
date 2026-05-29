# ⟡ Spectral Explorer

**Interactive conservation spectral analysis across domains.**

A single-page, zero-dependency web application for exploring graph Laplacian eigenvalues, Fiedler vectors, and conservation ratios through interactive graph building and real-world network presets.

## Features

- **Interactive Graph Builder** — click to add nodes, drag between nodes to add edges
- **Real-time Spectral Analysis** — Jacobi eigenvalue algorithm computes Laplacian spectrum in pure JS
- **Conservation Ratio** — λ₂/λₙ displayed with color-coded indicator (green = well-connected, red = sparse)
- **Fiedler Vector Visualization** — nodes colored by algebraic connectivity gradient (blue → red)
- **7 Mathematical Presets** — Complete, Path, Cycle, Barbell, Random, Star, Grid graphs
- **4 Real-World Networks** — Roman Empire trade routes, Jazz ii-V-I progressions, Food Web keystone species, Criminal hierarchy
- **Edge Animation** — watch eigenvalues shift as edges are added/removed
- **Delete Mode** — remove nodes and edges interactively

## Usage

Open `index.html` in any modern browser. No server required.

```bash
# Or serve locally:
python3 -m http.server 8000
```

## How It Works

The graph Laplacian **L = D - A** is computed from the adjacency matrix, then eigenvalues are found using the **Jacobi rotation algorithm** — an iterative method for symmetric matrices that applies plane rotations to zero out off-diagonal elements.

The **conservation ratio** λ₂/λₙ measures how well-connected a graph is relative to its size. Higher ratios indicate better spectral conservation — the graph's connectivity is more "uniform."

The **Fiedler vector** (eigenvector of λ₂, the algebraic connectivity) reveals the graph's natural partition structure.

## Built With

- Pure HTML, CSS, JavaScript — zero external dependencies
- Dark theme inspired by superinstance.ai
- Canvas-based rendering with device pixel ratio support

---

*Part of the [SuperInstance](https://superinstance.ai) research on conservation spectral analysis.*

Part of the [SuperInstance OpenConstruct](https://github.com/SuperInstance/OpenConstruct) ecosystem.
