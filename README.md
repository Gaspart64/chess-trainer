# Chess Puzzle Trainer 🎯♟️

A web-based chess puzzle training application that runs entirely on GitHub Pages. Upload PGN files containing chess puzzles, solve them interactively, and track your mistakes for focused improvement.

## 🌟 Features

- **PGN File Upload**: Import chess puzzles from standard PGN format files
- **Interactive Chess Board**: Drag-and-drop interface for solving puzzles
- **Automatic Progression**: Moves to the next puzzle upon successful completion
- **Mistake Tracking**: Automatically saves incorrectly solved puzzles
- **Progress Statistics**: Real-time tracking of correct solutions and mistakes
- **Export Mistakes**: Download all failed puzzles as a PGN file for review
- **Fully Static**: No backend required - runs entirely in the browser
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Beautiful UI**: Modern, gradient-based design with smooth animations

## 🚀 Quick Start

### Option 1: Use GitHub Pages (Recommended)

1. Fork this repository to your GitHub account
2. Go to Settings → Pages in your repository
3. Set Source to "Deploy from a branch"
4. Select "main" branch and "/ (root)" folder
5. Click Save and wait for deployment
6. Access your app at: `https://[your-username].github.io/[repository-name]/`

### Option 2: Local Development

1. Clone the repository:
```bash
git clone https://github.com/[your-username]/chess-puzzle-trainer.git
cd chess-puzzle-trainer
```

2. Open `index.html` in your web browser:
```bash
# On macOS
open index.html

# On Linux
xdg-open index.html

# On Windows
start index.html
```

## 📖 Usage Guide

### Uploading Puzzles

1. Click the "Choose PGN File" button
2. Select a PGN file containing chess puzzles
3. The app will automatically parse and load the puzzles

### Solving Puzzles

1. The first move (opponent's move) is played automatically
2. Find and play the winning continuation
3. Drag pieces to make your move
4. If correct, the opponent's response plays automatically
5. Continue until the puzzle is solved

### Controls

- **Reset**: Restart the current puzzle
- **Skip**: Move to the next puzzle without solving
- **Download Mistakes**: Export all failed puzzles as `mistakes.pgn`

### PGN Format Requirements

The app supports standard PGN format with the following features:
- FEN positions (using the `[FEN "..."]` header)
- Standard algebraic notation
- Multiple games in a single file
- Comments and variations (automatically removed during parsing)

Example PGN format:
```pgn
[Event "Puzzle 1"]
[Site "Chess Puzzles"]
[Date "2024.01.01"]
[White "Player"]
[Black "Opponent"]
[Result "1-0"]
[FEN "r1bqkb1r/pppp1ppp/2n2n2/1B2p3/4P3/5N2/PPPP1PPP/RNBQK2R w KQkq - 0 1"]

1. Bxc6 dxc6 2. Nxe5 *

[Event "Puzzle 2"]
[Site "Chess Puzzles"]
[Date "2024.01.02"]
[White "Player"]
[Black "Opponent"]
[Result "1-0"]
[FEN "r1bqk2r/pp2bppp/2n1pn2/3p4/2PP4/2N1PN2/PP3PPP/R1BQKB1R w KQkq - 0 1"]

1. cxd5 exd5 2. Bb5 *
```

## 🛠️ Technical Architecture

### Technologies Used

- **Chess.js**: Chess logic and move validation
- **Chessboard.js**: Interactive chess board UI
- **jQuery**: DOM manipulation (required by Chessboard.js)
- **LocalStorage**: Client-side persistence for mistakes and progress
- **Pure JavaScript**: Core application logic
- **CSS3**: Modern styling with animations and gradients

### File Structure

```
chess-puzzle-trainer/
├── index.html          # Main application file
├── README.md          # This documentation
├── LICENSE            # MIT License
└── examples/          # Sample PGN files (optional)
    ├── beginner.pgn
    ├── intermediate.pgn
    └── advanced.pgn
```

### Browser Compatibility

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Mobile)

## 🔧 Configuration

### Customizing the Interface

Edit the CSS section in `index.html` to modify:
- Color scheme (gradient colors)
- Board size
- Animation speeds
- Font styles

### Extending Functionality

The `ChessPuzzleTrainer` class can be extended with:
- Timer functionality
- Hint system
- Rating system
- Multiple solution support
- Sound effects

## 📝 Data Persistence

### LocalStorage

The app uses browser LocalStorage to persist:
- Mistake collection
- Statistics (correct/incorrect counts)
- Session progress

### Exporting Data

Mistakes can be exported as a PGN file that includes:
- Original puzzle positions
- Complete move sequences
- Original headers and metadata

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch:
```bash
git checkout -b feature/your-feature-name
```

3. Make your changes and test thoroughly

4. Commit with descriptive messages:
```bash
git commit -m "Add: New feature description"
```

5. Push to your fork:
```bash
git push origin feature/your-feature-name
```

6. Create a Pull Request with:
   - Clear description of changes
   - Screenshots if UI changes
   - Test PGN files if applicable

### Development Guidelines

- Maintain code readability and add comments
- Test on multiple browsers
- Ensure mobile responsiveness
- Follow existing code style
- Update documentation for new features

## 🐛 Known Issues & Limitations

### Current Limitations

1. **GitHub Pages Storage**: Mistakes are stored in browser LocalStorage, not directly in the GitHub repository
2. **Move Notation**: Some complex notation variations may need refinement
3. **Puzzle Validation**: Limited validation of puzzle solution accuracy

### Workarounds

- **Persistent Storage**: Regularly download and commit `mistakes.pgn` to your repository manually
- **Move Format**: Ensure PGN files use standard algebraic notation

## 📚 Resources

- [PGN Specification](https://www.chessclub.com/help/PGN-spec)
- [Chess.js Documentation](https://github.com/jhlywa/chess.js)
- [Chessboard.js Documentation](https://chessboardjs.com/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)

## 📄 License

This project is licensed under the MIT License. See the LICENSE file for details.

## 🙏 Acknowledgments

- Chess.js by Jeff Hlywa
- Chessboard.js by Chris Oakman
- Chess puzzle communities for test data
- Open source contributors

## 📮 Support

For issues, questions, or suggestions:
1. Check the [Issues](https://github.com/[your-username]/chess-puzzle-trainer/issues) page
2. Create a new issue with detailed information
3. Or contribute a fix via Pull Request

## 🚧 Roadmap

Future enhancements planned:
- [ ]
