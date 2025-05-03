## 🔍 Repo-Guardian - Git Integrity Auditor and Repair Tool

[![Status](https://img.shields.io/badge/status-under_construction-yellow)](https://github.com/pv4r/repo-guardian-pv4r)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Repo-Guardian is an advanced software development project that will result in a command-line (CLI) and terminal user interface (TUI) utility capable of auditing, repairing, and re-linearizing the integrity of any .git directory, whether it contains loose objects or packed into packfiles.

## 🛠 Key Features:

- 🔎 Cryptographic audit of Git objects (SHA-1/SHA-256)
- 🧩 Reconstruction of altered histories (force-push, rebase, filter-repo)
- 📊 DAG graph generation for forensic analysis (GraphML/Graphviz)
- 🖥 Interactive TUI interface with curses
- ✅ Complete CI/CD pipeline with BDD (Behave) and ≥80% coverage

## 🛠 Repo-Guardian Commands

| Command           | Parameters                 | Description                                                                 |
|-------------------|----------------------------|-----------------------------------------------------------------------------|
| `scan`            | `<path>`                   | Audits Git objects (loose/packed) using SHA-1/SHA-256 and verifies CRCs     |
| `repair`          | `<path>`                   | Reconstructs history using `git rebase --onto` and generates repair scripts |
| `export-graph`    | `--out <file>` (required)  | Exports DAG to GraphML format with metadata (SHA, author, timestamp, status)|
| `tui`             | `<path>`                   | Interactive terminal interface with progress tracking and repair controls    |

### Usage Examples:
```bash
# Basic scan
guardian scan ./my_repo

# Export graph for analysis
guardian export-graph --out recovered.graphml

# Launch interactive interface
guardian tui ./my_repo

```

# Context Diagram

![Context Diagram](https://github.com/pv4r/repo-guardian/blob/eb12b57113169e857713c7384126b7acd210f310/docs/img/context.svg)

