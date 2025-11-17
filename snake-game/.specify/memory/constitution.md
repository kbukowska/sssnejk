# Snake Web Game Constitution

## Project Vision
Create a minimal, pure JavaScript implementation of the classic Snake game that runs directly in any modern web browser without external dependencies.

## Core Principles

### 1. Simplicity First
- **Pure JavaScript**: No frameworks, libraries, or build tools required
- **Single HTML file**: All code contained in one HTML document for maximum portability
- **Minimal complexity**: Focus on core Snake gameplay mechanics only
- **Clean separation**: Distinct game logic, rendering, and input handling

### 2. Performance & Compatibility
- **Browser compatibility**: Works in all modern browsers (Chrome 80+, Firefox 75+, Safari 13+, Edge 80+)
- **Lightweight**: Total file size under 10KB
- **Smooth gameplay**: 60fps rendering with requestAnimationFrame
- **Responsive**: Adapts to different screen sizes

### 3. User Experience
- **Instant playability**: No loading screens or setup required
- **Intuitive controls**: Arrow keys and WASD for movement
- **Clear feedback**: Visual indication of score, game state, and collisions
- **Accessibility**: Keyboard-only navigation support

### 4. Code Quality
- **Readable code**: Clear variable names and logical organization
- **No external dependencies**: Everything runs offline
- **Error handling**: Graceful handling of edge cases
- **Maintainable**: Well-structured code for easy modification

## Technical Requirements

### Minimum Viable Product (MVP)
1. **Game Board**: Fixed-size grid (20x20 cells minimum)
2. **Snake Movement**: Continuous movement in four directions
3. **Food System**: Random food placement and consumption
4. **Growth Mechanics**: Snake grows when eating food
5. **Collision Detection**: Wall and self-collision ends game
6. **Score Tracking**: Display current score
7. **Game States**: Start, playing, and game over states

### Core Features
- Snake starts with length of 3 segments
- Food appears as single pixel/cell
- Score increases by 1 point per food consumed
- Game speed remains constant (no acceleration)
- Simple restart mechanism

### User Interface
- Canvas-based rendering for smooth graphics
- Score display prominently visible
- Game over screen with restart option
- Minimal, clean visual design

## Technical Constraints

### Must Have
- Single HTML file with embedded CSS and JavaScript
- No external asset files or dependencies
- Canvas 2D rendering context only
- Standard HTML5 APIs only
- Total lines of code under 200

### Must Not Have
- No WebGL or advanced graphics APIs
- No audio or sound effects
- No animations beyond basic movement
- No multiplayer functionality
- No high score persistence
- No mobile touch controls

## Success Criteria

### Functional
- ✅ Snake moves smoothly in four directions
- ✅ Food spawns randomly on empty cells
- ✅ Snake grows when consuming food
- ✅ Game ends on collision (wall or self)
- ✅ Score updates correctly
- ✅ Game can be restarted

### Quality
- ✅ Runs at consistent 60fps on modern hardware
- ✅ File size under 10KB
- ✅ No console errors or warnings
- ✅ Works offline without internet connection
- ✅ Responsive to window resizing

### User Experience
- ✅ Game loads instantly
- ✅ Controls feel responsive
- ✅ Visual feedback is clear and immediate
- ✅ Game state is always obvious to player

## Non-Goals
- Advanced graphics or animations
- Sound effects or music
- Mobile device support
- High score leaderboards
- Multiple difficulty levels
- Custom themes or skins
- Pause functionality
- Speed progression

## Governance
This constitution serves as the foundation for all development decisions. Any feature or implementation choice should align with these principles of simplicity, performance, and pure JavaScript implementation.

**Version**: 1.0.0 | **Ratified**: 2025-11-17 | **Last Amended**: 2025-11-17
