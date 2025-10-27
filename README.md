# Tic-Toc-Tue Game 🎮

A playful take on the classic Tic-Tac-Toe (or "Tic-Toc-Tue" for that mid-week vibe)! Built with vanilla JavaScript, this 3x3 grid game lets two players (X and O) battle it out. First to three in a row wins—simple, addictive, and zero-install fun.

![Game Screenshot](images/game-board.png) *(Add a screenshot once built!)*

## Live Demo
- [Play Now](https://hemantydvv.github.io/tic-toc-tue-game/) *(Deploy via GitHub Pages—see Setup below)*

## Features
- **Two-Player Mode**: Alternate turns between X and O—no AI, just pure head-to-head.
- **Win Detection**: Auto-checks rows, columns, and diagonals for victory.
- **Draw Handling**: Spots ties when the board fills up.
- **Reset Button**: Start a fresh game anytime.
- **Responsive Design**: Plays nice on desktop or mobile.
- **Fun Twist**: "Tic-Toc-Tue" theme—perfect for Tuesday game nights!

## How to Play
1. **Load the Game**: Open `index.html` in your browser.
2. **Take Turns**: Click a cell to place your mark (X starts!).
3. **Win Conditions**: Get three in a row (horizontal, vertical, or diagonal).
4. **End Game**: Winner gets a congrats message; ties prompt a rematch.
5. **Reset**: Hit the button to clear the board.

**Pro Tip**: Block your opponent's lines—strategy over luck!

## Tech Stack
| Category | Tools |
|----------|-------|
| **Frontend** | HTML5 (grid structure), CSS3 (styling & animations), JavaScript (logic & events) |
| **Deployment** | GitHub Pages (free hosting) |
| **Tools** | VS Code (editor), Git (version control) |

Core logic in `script.js`: Event listeners on cells, array for board state, function to check wins.

## Setup & Run Locally
1. **Clone the Repo**:
2. **Open in Browser**: Double-click `index.html` or use a local server (e.g., VS Code Live Server).
3. **Deploy to GitHub Pages** (for live demo):
- Go to repo Settings > Pages.
- Set Source: "Deploy from a branch" > main > `/ (root)` > Save.
- Site live in minutes at `https://hemantydvv.github.io/tic-toc-tue-game/`.

## Code Structure
- `index.html`: Game board and UI elements.
- `style.css`: Grid layout, hover effects, win highlights.
- `script.js`: 
```javascript
// Example snippet: Win check function
function checkWin(player) {
 const wins = [
   [0,1,2], [3,4,5], [6,7,8], // Rows
   [0,3,6], [1,4,7], [2,5,8], // Columns
   [0,4,8], [2,4,6] // Diagonals
 ];
 return wins.some(combo => combo.every(cell => board[cell] === player));
}
