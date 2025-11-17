# Tasks: Snake Web Game

**Input**: Design documents from `.specify/memory/`
**Prerequisites**: plan.md (required), spec.md (required for user stories), constitution.md

**Project Type**: Single HTML file implementation

## Format: `[ID] [P?] [Story] Description`

- **[P]**: Can run in parallel (no dependencies)
- **[Story]**: Which user story this task belongs to (US1, US2, US3)
- All code will be in single file: `snake-game.html`

---

## Phase 1: Setup (Project Foundation)

**Purpose**: Initialize single-file HTML structure and basic framework

- [ ] T001 Create `snake-game.html` with basic HTML5 structure and meta tags
- [ ] T002 Add canvas element with proper dimensions for 20x20 grid minimum
- [ ] T003 [P] Add embedded CSS for styling and layout
- [ ] T004 [P] Add JavaScript section with game namespace and basic structure

---

## Phase 2: Foundational (Core Architecture)

**Purpose**: Essential game infrastructure that ALL user stories depend on

**⚠️ CRITICAL**: No user story work can begin until this phase is complete

- [ ] T005 Implement game state management system (PLAYING, GAME_OVER states)
- [ ] T006 Create grid system with coordinate mapping and cell size calculations  
- [ ] T007 Initialize canvas context and basic rendering setup
- [ ] T008 Implement requestAnimationFrame game loop structure
- [ ] T009 [P] Add keyboard event listeners for arrow keys and WASD
- [ ] T010 [P] Create utility functions for coordinate validation and grid bounds

**Checkpoint**: Foundation ready - user story implementation can now begin

---

## Phase 3: User Story 1 - Game Launch and Basic Play (Priority: P1) 🎯 MVP

**Goal**: User opens HTML file and immediately plays Snake with arrow key controls

**Independent Test**: Open HTML file, use arrow keys to move snake, snake eats food and grows

### Implementation for User Story 1

- [ ] T011 [P] [US1] Create Snake data structure (array of {x,y} coordinates, starting with 3 segments)
- [ ] T012 [P] [US1] Create Food data structure (single {x,y} coordinate)
- [ ] T013 [US1] Implement snake rendering function (draw rectangles for each segment)
- [ ] T014 [US1] Implement food rendering function (draw single food cell)
- [ ] T015 [US1] Implement snake movement logic (update head position based on direction)
- [ ] T016 [US1] Implement direction change handling from keyboard input
- [ ] T017 [US1] Implement food-snake collision detection (head position matches food position)
- [ ] T018 [US1] Implement snake growth mechanics (add new segment when food consumed)
- [ ] T019 [US1] Implement random food spawning on empty grid cells
- [ ] T020 [US1] Integrate movement, rendering, and collision in main game loop

**Checkpoint**: Snake moves, eats food, grows - core gameplay functional

---

## Phase 4: User Story 2 - Collision Detection and Game Over (Priority: P2)

**Goal**: Game ends on wall/self collision with clear feedback and restart option

**Independent Test**: Intentionally crash snake into wall or itself, verify game over and restart

### Implementation for User Story 2

- [ ] T021 [P] [US2] Implement wall collision detection (check if head is outside grid bounds)
- [ ] T022 [P] [US2] Implement self-collision detection (check if head matches any body segment)
- [ ] T023 [US2] Implement game over state transition and movement stopping
- [ ] T024 [US2] Create game over screen rendering with "Game Over" message
- [ ] T025 [US2] Add restart functionality (spacebar or button click)
- [ ] T026 [US2] Implement game state reset (new snake, new food, score reset)
- [ ] T027 [US2] Add input validation to prevent reverse direction moves

**Checkpoint**: Game has proper boundaries and failure states with recovery

---

## Phase 5: User Story 3 - Score Display and Visual Feedback (Priority: P3)

**Goal**: User sees clear score and game state through visual indicators

**Independent Test**: Play game, verify score updates correctly and displays clearly

### Implementation for User Story 3

- [ ] T028 [P] [US3] Implement score tracking variable and increment logic
- [ ] T029 [P] [US3] Create score display rendering function
- [ ] T030 [US3] Integrate score display in main rendering loop
- [ ] T031 [US3] Add score display to game over screen
- [ ] T032 [US3] Improve visual styling (colors, fonts, layout)
- [ ] T033 [US3] Add visual feedback for game state changes
- [ ] T034 [US3] Implement responsive canvas sizing for different screen sizes

**Checkpoint**: Game has polished UI and clear feedback for all interactions

---

## Phase 6: Polish and Validation

**Purpose**: Final optimizations and requirement validation

- [ ] T035 Code review and optimization for file size (target: under 10KB)
- [ ] T036 Code review and line count optimization (target: under 200 lines)
- [ ] T037 [P] Cross-browser testing (Chrome, Firefox, Safari, Edge)
- [ ] T038 [P] Performance testing and 60fps validation
- [ ] T039 [P] Edge case testing and bug fixes
- [ ] T040 Final validation against all functional requirements (FR-001 through FR-010)
- [ ] T041 [P] Final validation against all technical requirements (TR-001 through TR-005)
- [ ] T042 [P] Final validation against all success criteria (SC-001 through SC-007)

---

## Implementation Strategy

### MVP First (User Story 1 Only)
1. Complete Phase 1: Setup
2. Complete Phase 2: Foundational (**CRITICAL** - blocks all stories)  
3. Complete Phase 3: User Story 1
4. **STOP and VALIDATE**: Test basic Snake gameplay independently
5. Demo/validate if ready for minimal Snake experience

### Incremental Delivery
1. Setup + Foundational → Core architecture ready
2. Add User Story 1 → Test independently → **MVP complete!**
3. Add User Story 2 → Test independently → Game boundaries complete
4. Add User Story 3 → Test independently → Full featured game
5. Polish → Test performance/compatibility → **Production ready**

### Quality Gates at Each Phase
- **Phase 2 Checkpoint**: Game loop runs, canvas renders, input responds
- **Phase 3 Checkpoint**: Snake moves, eats, grows - playable game
- **Phase 4 Checkpoint**: Game has proper win/lose conditions
- **Phase 5 Checkpoint**: Game has polished user experience
- **Phase 6 Checkpoint**: Game meets all constitutional requirements

---

## File Structure Tracking

Since this is a single-file implementation, track sections:

```html
snake-game.html
├── HTML structure (canvas, meta tags)
├── <style> section (CSS for layout and colors)
└── <script> section
    ├── Game state variables
    ├── Data structures (Snake, Food, Grid)
    ├── Input handling
    ├── Game logic functions
    ├── Rendering functions
    ├── Game loop and initialization
    └── Event listeners
```

---

## Critical Success Metrics

Track these throughout implementation:
- **File Size**: Monitor after each task (target < 10KB)
- **Line Count**: Monitor after each task (target < 200 lines) 
- **Performance**: Test frame rate during development
- **Functionality**: Each user story must work independently
- **Browser Compatibility**: Test on multiple browsers regularly

---

## Notes

- Each task should be completable in 30-60 minutes
- Test functionality after each task completion
- Commit/save after completing each logical task group
- Prioritize working functionality over perfect code in early phases
- Optimize for size/performance in final polish phase
- Maintain constitution compliance throughout all phases