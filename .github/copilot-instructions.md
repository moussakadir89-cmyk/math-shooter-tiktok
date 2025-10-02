# Math Shooter Challenge - TikTok Viral Game

## Project Overview

This is an interactive math shooting game optimized for TikTok sharing and viral engagement. The game features a vertical 9:16 format perfect for mobile devices and social media sharing.

## Tech Stack

- **Pure HTML/CSS/JavaScript** - No frameworks or dependencies
- **No build process** - Direct deployment to GitHub Pages
- **Mobile-first design** - Optimized for touch controls and vertical mobile screens

## File Structure

- `index.html` - Main game file (simple version)
- `index_with_audio.html` - Enhanced version with background music
- `package_info.html` - Setup and information page
- `background.mp3` - Background audio file
- `README.md` - Documentation and setup guide
- `LICENSE` - MIT License

## Coding Standards

### HTML
- Use semantic HTML5 elements
- Include proper meta tags for social media sharing (Open Graph, Twitter cards)
- Optimize for mobile viewport (9:16 aspect ratio for TikTok)
- Keep inline styles and scripts for easy deployment

### CSS
- Use CSS animations for visual effects (explosions, star twinkling, etc.)
- Maintain TikTok-optimized 9:16 aspect ratio (.game-container max-width: 375px)
- Use gradient backgrounds and modern CSS features
- Ensure touch-friendly button sizes (minimum 48px touch targets)

### JavaScript
- Pure vanilla JavaScript - no frameworks
- Use object literals for game state management
- Keep code inline in HTML files for portability
- Use requestAnimationFrame for smooth animations
- Add audio controls with proper user interaction handling

## Game Features

- Math equation generation with progressive difficulty
- Shooting mechanics with player movement
- Score tracking and level progression
- Visual effects (explosions, stars, particles)
- Social sharing functionality for TikTok
- Mobile touch controls and keyboard support
- Background music (optional)

## TikTok Optimization

- **Vertical format**: 9:16 aspect ratio
- **Viral elements**: Score challenges, engagement hooks
- **Share functionality**: Built-in caption and hashtag generation
- **Mobile-first**: Touch controls and responsive design

## Design Principles

1. **No external dependencies** - Keep it simple and portable
2. **Fast loading** - Optimize for quick engagement
3. **Viral hooks** - Include challenge elements and share prompts
4. **Mobile-friendly** - Touch controls and vertical layout
5. **Progressive difficulty** - Keep players engaged

## When Making Changes

- Test on mobile devices or use browser mobile emulation
- Ensure the 9:16 aspect ratio is maintained
- Keep all code inline (no separate .js or .css files) for easy GitHub Pages deployment
- Preserve the viral/TikTok optimization features
- Test touch controls on actual mobile devices when possible
- Verify audio works with user interaction (browsers require user gesture for audio)

## Deployment

The game is designed for direct deployment to GitHub Pages:
1. No build process required
2. Just push to main branch
3. Enable GitHub Pages in repository settings
4. Game will be live at: `https://username.github.io/math-shooter-tiktok/`

## Common Patterns

### Game State Management
```javascript
const gameState = {
    score: 0,
    level: 1,
    lives: 3,
    gameRunning: false,
    // ... other state
};
```

### Animation Pattern
```javascript
function gameLoop() {
    if (!gameState.gameRunning) return;
    // Update game logic
    requestAnimationFrame(gameLoop);
}
```

### Mobile Touch Controls
```javascript
document.getElementById('leftBtn').addEventListener('click', () => movePlayer('left'));
document.getElementById('rightBtn').addEventListener('click', () => movePlayer('right'));
document.getElementById('shootBtn').addEventListener('click', shoot);
```

## Browser Compatibility

Target modern mobile browsers (last 2 versions):
- Chrome/Safari on iOS
- Chrome on Android
- Modern desktop browsers for testing

## Performance Considerations

- Use CSS transforms for animations (hardware accelerated)
- Limit number of active game objects
- Clean up removed elements from DOM
- Use requestAnimationFrame for smooth 60fps gameplay
- Optimize audio loading with preload tags
