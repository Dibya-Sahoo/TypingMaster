# TypingMaster
build browser based UI to practice typing 

## High-Level Design
Your app will have these main parts:

1. Text Display (Target String)
    - Shows the text the user needs to type.
    - Letters turn green if correct, red if incorrect, gray/neutral if not typed yet.
    
2. Typing Input Handler
    - Captures user keystrokes.
    - Compares typed input vs target string.
    - Updates state accordingly.
    
3. On-Screen Keyboard
    - Displays a visual keyboard.
    - Highlights the key pressed.
    - Optional: show "next key to press" hint.

4. Stats Tracker
    - WPM (Words Per Minute).
    - Accuracy %.
    - Number of errors.

5. App Layout / UI Controls
    - Start / Restart button.
    - Settings (difficulty, string length, maybe word source).
    - Simple dashboard for progress.

## 🧩 Functional Design
1. App
   - Root container.
   - Holds global state: current string, typed input, stats.
2. TextDisplay
    - Props: targetText, typedText.
    - Renders each character in a span:
        - Green if correct.
        - Red if incorrect.
        - Default color if not typed yet.
3. Keyboard
    - A UI keyboard (like QWERTY).
    - Highlights pressed key.
    - Props: lastKeyPressed, nextExpectedKey.
4. InputHandler
    - Actually invisible <input> to capture typing.
    - Updates state in App.
5. StatsPanel
    - Displays live stats (WPM, accuracy, errors).
    - Props: typedText, targetText, errors, startTime.
6. Controls
    - Start / Restart button.
    - Maybe dropdown for difficulty.
      
## 🔄 Data Flow (React-style)
1. App generates target text (e.g., "hello world").
2. User types → captured by InputHandler.
3. State updates (typedText).
4. TextDisplay re-renders with new colors.
5. Keyboard highlights pressed key.
6. StatsPanel recalculates and displays updated values.
## 🎯 Suggested Milestones (Implementation Path)

### Phase 1: Core Typing Logic
    - Show string.
    - Capture typing.
    - Show correct/incorrect colors.
### Phase 2: On-Screen Keyboard
    - Display QWERTY.
    - Highlight pressed key.
### Phase 3: Stats Tracking
    - Implement WPM & accuracy calculation.
### Phase 4: UI Polish
    - Restart button, dark/light theme.
    - Add animations for key presses.
### Phase 5 (Optional Advanced)
    - Support random word generation.
    - Save progress in localStorage.
    - Leaderboard or history view.
