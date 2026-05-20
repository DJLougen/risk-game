# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2024

### Added
- ✨ Complete Risk board game implementation
- 🌍 3D board rendering with Three.js
- 🗺️ 42 territories across 6 continents with proper adjacency
- 🎮 Full game rules: Claim → Reinforce → Attack → Fortify
- 🎲 Animated dice combat system
- 🤖 Heuristic AI with 3 difficulty levels (Easy/Normal/Hard)
- 🧠 LLM integration (OpenAI-compatible API support)
- 🏆 Continent bonuses and strategic gameplay
- 👥 1-5 AI opponents
- 🎨 Color-coded players with animated selection rings
- 📊 Territory labels with army counts
- 💻 Pure HTML/CSS/JS - no build step required
- 🚀 GitHub Pages deployment
- 📖 Comprehensive README with screenshots
- 🤝 Contributing guidelines
- 📝 Issue templates for bugs and features

### Technical Details
- Single-file architecture (index.html)
- Zero dependencies
- ES6+ JavaScript
- Three.js for 3D rendering
- Canvas-based sprite labels
- Efficient adjacency lookups (precomputed)
- Graceful error handling for LLM integration

### Game Features
- **Setup Modal**: Configure players, difficulty, and AI mode
- **Territory Claiming**: Strategic initial placement phase
- **Reinforcement**: Army placement based on territories and continents
- **Combat**: Risk-style dice battles with animated rolls
- **Fortification**: Move armies between connected territories
- **Victory**: Eliminate all opponents to win

### AI Capabilities
- Evaluates strategic territory value
- Prioritizes continent control
- Reinforces border territories
- Attacks with favorable odds (3:1 ratio)
- Fortifies weak positions
- Adapts to game state changes

### LLM Integration
- OpenAI-compatible chat completions API
- Context-aware game state serialization
- Structured move responses
- Timeout handling (5s default)
- Automatic fallback to heuristic AI
- Configurable endpoint and model

[1.0.0]: https://github.com/DJLougen/risk-game/releases/tag/v1.0.0
