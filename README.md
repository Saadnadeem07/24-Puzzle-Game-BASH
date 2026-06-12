<h1 align="center">🧩 24-Puzzle Game (Bash)</h1>

<p align="center">
  A classic <strong>5×5 sliding-tile puzzle</strong> built entirely in pure Bash shell scripting —
  no external dependencies, just your terminal.
</p>

<p align="center">
  <img alt="Language" src="https://img.shields.io/badge/Language-Bash-4EAA25?logo=gnubash&logoColor=white">
  <img alt="Platform" src="https://img.shields.io/badge/Platform-Linux%20%7C%20macOS-blue">
  <img alt="License" src="https://img.shields.io/badge/License-MIT-green">
  <img alt="Course" src="https://img.shields.io/badge/Project-Operating%20Systems%20Lab-orange">
</p>

---

## 📖 About

The **24-Puzzle** is the bigger sibling of the famous 15-puzzle. It's a 5×5 grid filled
with tiles numbered **1–24** and one empty space. Tiles adjacent to the empty space can
slide into it. The goal is to arrange the tiles in ascending order with the empty space
in the bottom-right corner.

This project was developed as a **Mini Project for the Operating Systems Lab**, demonstrating
core shell-scripting concepts: arrays, functions, loops, conditionals, and user input handling.

---

## 🎮 Demo

```
Initial Board Configuration:
  1|  2|  3|  4|  5|
  6|  7|  8|  9| 10|
 11| 12| 13| 14| 15|
 16| 17| 18| 19| 20|
   | 21| 22| 23| 24|

Goal Board Configuration:
  1|  2|  3|  4|  5|
  6|  7|  8|  9| 10|
 11| 12| 13| 14| 15|
 16| 17| 18| 19| 20|
 21| 22| 23| 24|   |

Enter the number you want to move (0 for quit): 21
...
Congratulations! You solved the puzzle.
```

---

## 🚀 Getting Started

### Prerequisites
- A Unix-like environment with **Bash** (Linux, macOS, or WSL on Windows).

### Run the game

```bash
# Clone the repository
git clone https://github.com/Saadnadeem07/24-Puzzle-Game-BASH.git
cd 24-Puzzle-Game-BASH

# Make the script executable (first time only)
chmod +x src/puzzle.sh

# Play!
./src/puzzle.sh
```

> You can also run it directly with `bash src/puzzle.sh`.

---

## 🕹️ How to Play

1. The board starts one or more moves away from the solved state.
2. When prompted, **type the number of the tile** you want to slide into the empty space.
   - A move is only valid if that tile is **directly adjacent** (up/down/left/right) to the empty cell.
3. Keep sliding tiles until the board matches the **Goal Configuration**.
4. Enter **`0`** at any time to quit.

🎯 **Objective:** Arrange tiles `1 → 24` in order, leaving the empty cell in the bottom-right.

---

## 🗂️ Project Structure

```
24-Puzzle-Game-BASH/
├── src/
│   └── puzzle.sh           # The complete game (Bash script)
├── docs/
│   └── Project-Report.docx # Operating Systems Lab project report
├── assets/                 # Screenshots & media (optional)
├── README.md               # You are here
├── LICENSE                 # MIT License
└── .gitignore
```

---

## ⚙️ How It Works

The game is organized into small, single-purpose Bash functions:

| Function       | Responsibility                                                        |
| -------------- | --------------------------------------------------------------------- |
| `printPuzzle`  | Renders the current 5×5 board to the terminal.                        |
| `printGoal`    | Displays the target (winning) configuration.                          |
| `isGoal`       | Checks whether the current board matches the goal state.              |
| `isValidMove`  | Validates that a chosen tile is adjacent to the empty cell.           |
| `move`         | Swaps the chosen tile with the empty cell.                            |
| `playGame`     | Main game loop — reads input, validates, updates, and checks for win. |

The board is stored as a flat 25-element array, where index `i` maps to grid position
`row = i / 5`, `col = i % 5`. The empty cell is represented by `0`. Adjacency is detected
using the squared distance between the empty cell and the selected tile.

---

## 👤 Author

**Saad Nadeem**
🎓 Operating Systems Lab — Mini Project (Roll No. 21F-9104)
🔗 [GitHub @Saadnadeem07](https://github.com/Saadnadeem07)

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<p align="center"><em>If you enjoyed this little terminal puzzle, consider giving the repo a ⭐!</em></p>
