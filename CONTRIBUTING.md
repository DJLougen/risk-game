# Contributing to Risk — Global Domination

Thank you for your interest in contributing! This document provides guidelines and information for contributors.

## 🎯 Ways to Contribute

### Bug Reports
- Use the [Bug Report template](https://github.com/DJLougen/risk-game/issues/new?template=bug_report.md)
- Include browser version and OS
- Describe steps to reproduce
- Add screenshots if applicable

### Feature Requests
- Use the [Feature Request template](https://github.com/DJLougen/risk-game/issues/new?template=feature_request.md)
- Explain the use case
- Describe expected behavior
- Consider implementation complexity

### Code Contributions

#### Getting Started
```bash
git clone https://github.com/DJLougen/risk-game.git
cd risk-game
# Open index.html in your browser
# Edit and refresh to test changes
```

#### Code Style
- Use consistent indentation (2 spaces)
- Comment complex logic
- Keep functions focused and small
- Use descriptive variable names

#### Testing
- Test in multiple browsers (Chrome, Firefox, Safari)
- Test with different player counts (2-6 players)
- Test AI behavior at different difficulties
- Test LLM integration if modifying that code

#### Submitting Changes
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Test thoroughly
5. Commit with clear messages (`git commit -m 'Add amazing feature'`)
6. Push to your branch (`git push origin feature/amazing-feature`)
7. Open a Pull Request

## 📋 Project Structure

```
risk-game/
├── index.html              # Main game file (HTML/CSS/JS)
├── README.md               # Project documentation
├── LICENSE                 # MIT license
├── screenshots/            # Game screenshots
└── .github/                # GitHub templates
```

## 🎮 Feature Ideas

Here are some areas where contributions would be valuable:

### High Priority
- **Save/Load System**: Persist game state to localStorage
- **Sound Effects**: Add audio feedback for actions
- **Mobile Controls**: Improve touch interface
- **Performance**: Optimize rendering for lower-end devices

### Medium Priority
- **Replay System**: Record and playback games
- **Statistics**: Track win rates, territories conquered, etc.
- **More AI Personalities**: Different strategic approaches
- **Custom Maps**: Alternative board layouts

### Nice to Have
- **Multiplayer**: Real-time play via WebSocket
- **Tournaments**: Bracket-style competitions
- **Achievements**: Unlock badges for milestones
- **Themes**: Different visual styles

## 🐛 Common Issues

### Adjacency Errors
If territories have incorrect connections:
- Check `TERRITORY_DEFS` adjacency arrays
- Run symmetry validation (see code comments)
- Ensure bidirectional links

### AI Getting Stuck
If AI doesn't make moves:
- Check `aiTurnHeuristic()` phase handling
- Verify `G.processing` flag management
- Add debug logging to identify blocked state

### Rendering Issues
If 3D elements don't appear:
- Check browser console for Three.js errors
- Verify WebGL support
- Test on different browsers

## 🔧 Development Tips

### Debugging
- Use browser DevTools console
- Add `console.log()` statements for state tracking
- Use breakpoints in browser debugger
- Check Network tab for LLM API calls

### Testing LLM Integration
- Use Ollama locally for easy testing
- Mock API responses with browser DevTools
- Test error handling (timeouts, invalid responses)
- Verify fallback to heuristic AI

### Performance Profiling
- Use browser Performance tab
- Monitor frame rate during gameplay
- Check for memory leaks in long games
- Profile AI decision-making time

## 📝 Commit Message Guidelines

Use clear, descriptive commit messages:

```
feat: add save/load game functionality
fix: correct adjacency between Alaska and Kamchatka
docs: update README with new screenshots
style: improve code formatting in AI module
refactor: simplify territory selection logic
test: add validation for continent bonuses
```

## 🤝 Code of Conduct

- Be respectful and constructive
- Focus on the problem, not the person
- Welcome newcomers and help them learn
- Assume good intentions

## ❓ Questions?

Open a [Discussion](https://github.com/DJLougen/risk-game/discussions) for questions that aren't bugs or feature requests.

---

Thank you for contributing! 🎲
