# TypingMaster
build browser based UI to practice typing 

##High-Level Design
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
