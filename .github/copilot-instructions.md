# Copilot Instructions for Pay Me Card Game

## Project Overview

This is a web-based implementation of the "Pay Me" card game built as a single-page application using vanilla JavaScript and React. The game is implemented entirely in a single `index.html` file with embedded styles and scripts.

## Technology Stack

- **Frontend**: React 18 (loaded via CDN)
- **Language**: JavaScript (JSX transpiled via Babel Standalone)
- **Styling**: Inline CSS within the HTML file
- **Build**: No build process - runs directly in the browser

## Code Organization

### Structure
- All code is contained in `/index.html`
- React components are defined inline within a single `<script type="text/babel">` block
- CSS styles are in a `<style>` block in the document head
- No external dependencies or build tools required

### Component Architecture
- Main game component: `PayMeGame`
- Reusable UI components: `Card`, `MiniCard`, `WinnerHandCard`
- Game logic is embedded within React state management using hooks

## Coding Conventions

### JavaScript/React Guidelines
- Use functional components with React hooks (useState, useEffect, useRef)
- Follow camelCase naming for variables and functions
- Use descriptive variable names
- Keep components organized within the single file structure
- Use JSX for component rendering

### Style Guidelines
- CSS is organized by logical sections (layout, components, animations)
- Use responsive design patterns with `clamp()` for fluid sizing
- Maintain consistent color scheme (blue gradients, card game aesthetics)
- Use CSS animations for game interactions (card dealing, dragging, etc.)

### Game Logic
- Game state is managed through React hooks
- Card game rules are implemented in pure JavaScript functions
- AI player logic is deterministic and rule-based
- Support for multiple rounds (11 rounds total)
- Wild cards and melds follow standard card game conventions

## Important Considerations

### When Making Changes
1. **Single File Constraint**: All changes must work within the single HTML file structure
2. **Browser Compatibility**: Ensure code works in modern browsers without transpilation beyond Babel
3. **No Build Step**: Code must run directly when opening the HTML file in a browser
4. **Performance**: Be mindful of performance as all logic runs in the browser
5. **State Management**: Keep React state management clean and avoid unnecessary re-renders

### Testing Approach
- Manual testing by opening the HTML file in a browser
- Test all game phases: setup, drawing, discarding, melds, round completion
- Verify AI behavior across different game scenarios
- Test responsive design on different screen sizes

### Code Style
- Indent with 4 spaces (consistent with existing code)
- Keep lines reasonably short for readability
- Comment complex game logic clearly
- Use modern ES6+ JavaScript features (arrow functions, destructuring, etc.)

## Key Features to Preserve

- Drag-and-drop card functionality
- Touch support for mobile devices
- Animated card dealing and transitions
- Side panel with player information
- Meld building and validation
- AI opponent behavior
- Score tracking and round progression
- Wild card handling
- Responsive layout that works on desktop and mobile

## When Adding New Features

1. Consider the single-file architecture
2. Maintain the existing visual style and user experience
3. Ensure new features work with existing game mechanics
4. Test thoroughly across different browsers
5. Keep the code maintainable within the single-file constraint
6. Document complex game logic with comments

## Common Tasks

### Modifying Game Rules
- Look for validation functions (e.g., `isValidMeld`, `isValidPlay`)
- Update game constants if needed
- Test edge cases thoroughly

### Updating UI
- Locate the relevant CSS class or component
- Maintain consistent styling with existing elements
- Test responsive behavior

### Debugging
- Use browser console for debugging
- Check React component state with React DevTools
- Verify game state transitions are correct

## Best Practices

1. **Preserve Working Code**: Be surgical with changes - modify only what's necessary
2. **Test Incrementally**: After each change, verify the game still works
3. **Maintain Consistency**: Follow the existing code patterns and style
4. **Comment Wisely**: Add comments for complex game logic, but don't over-comment
5. **Mobile-First**: Consider mobile users when making UI changes
