# 🎮 Hangman Game
### ASCII-Art Word Guessing in the Terminal

> ⚠️ **DISCLAIMER:** This is a **personal learning and portfolio project**. It is a command-line Hangman word-guessing game built in Python for educational purposes. All game logic runs locally in your terminal — no data is collected, stored, or transmitted.

A colorful, ASCII-art Hangman game where you race to guess a hidden word one letter at a time before six wrong guesses complete the gallows. It features a curated word list, animated ASCII hangman stages, friendly emoji-driven feedback, input validation, and a replay loop — all in a single Python file.

![Version](https://img.shields.io/badge/Version-1.0.0-3776AB)
![Status](https://img.shields.io/badge/Status-Portfolio%20Project-F4B400)
![Platform](https://img.shields.io/badge/Platform-Console%20%28Python%29-2D6A4F)

---

## 🔗 Links

- **Source Code:** [github.com/Ashish22Gupta/Hangman-game](https://github.com/Ashish22Gupta/Hangman-game)

> 💡 *No live demo — this is a terminal application. Clone the repo and run it locally.*

---

## ✨ Implemented Features

### 🎲 Random Word Selection
- **13-Word Curated List** — Words include `blue`, `words`, `change`, `mask`, `gold`, `lamp`, `sky`, `frog`, `paint`, `sword`, `prize`, `ghost`, and `blank`.
- **Fresh Word Each Round** — `random.choice()` picks a new word on every replay, so no two games repeat back-to-back.

### 🖼️ Animated ASCII Hangman
- **6 Progressive Stages** — The gallows animate through six distinct ASCII frames as wrong guesses accumulate:
  1. Empty gallows
  2. Head appears
  3. Body appears
  4. Left arm appears
  5. Both arms appear
  6. Both legs appear — game over
- **`time.sleep(1)` Pacing** — Each stage renders with a 1-second delay, adding dramatic tension.
- **Guess Remaining** — Every wrong guess prints `"X guesses remaining"` or `"last guess remaining"`.

### 🎨 Emoji-Driven Feedback
- **Clear Win/Lose/Invalid States** — Distinct messages for:
  - ✅ Correct guess
  - ❌ Wrong guess
  - ⚠️ Already-guessed letter
  - ❗ Multi-character input
  - 👻 Empty input
  - 🎉 Win
  - 😢 Loss
- **Visual Word Progress** — After each guess, the current state of the word is printed as underscores and revealed letters.

### 🛡️ Robust Input Validation
- **Empty-Input Handling** — Catches blank entries with a "silence won't save you" message.
- **Already-Guessed Detection** — Prevents re-entering the same letter via a `guess_word` tracking list.
- **Multi-Character Guard** — Rejects inputs longer than 1 character.
- **Case-Insensitive** — All inputs are `.lower()`-cased so `A` and `a` are treated the same.

### 🔁 Replay Loop
- **Press Enter to Play** — Just pressing Enter starts a fresh round with a new word.
- **Type `exit` to Quit** — Clean exit with a friendly goodbye message.
- **Unlimited Rounds** — Play as many times as you like in one session.

### ⏳ Pre-Game Suspense
- **"Choosing a word..." Delay** — A `time.sleep(3)` pause with a "🔍 Wait choosing a word..." message before revealing the word length.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| **Python 3** | Core language — `input()`, `while` loops, `if/elif` conditionals |
| **`random`** | Word selection from the curated list |
| **`time`** | `sleep()` pacing for suspense during word reveal and hangman stages |
| **Unicode emoji** | Visual feedback throughout the terminal UI |
| **ASCII art** | Progressive hangman gallows illustrations |

---

## 📁 Project Structure

```text
Hangman-game/
└── Hangman Game.py          # Single-file Python console game
