# 🎯 Hangman Game – Python Bootcamp Project #7 🐍

## 📜 Project Overview
This is my **7th Python project** from the Bootcamp, and it’s all about the classic game **Hangman** 🎮.  
The program randomly selects a word, and the player must guess it **one letter at a time** before they run out of lives 💀.

It’s an exciting mix of **logic, loops, and ASCII art** 🖼️ — plus a great way to practice **Python fundamentals**!

---

## 🛠 Features
- 🎲 **Random Word Selection** – Words are imported from `hangman_words.py`.
- 🖼 **ASCII Art Logo & Stages** – Imported from `hangman_art.py` to make the game visually fun.
- ❤️ **Lives System** – Player starts with **6 lives**, losing one for each wrong guess.
- 🔁 **Continuous Play Loop** – Keeps asking for guesses until you either:
  - 🎉 **Win** by guessing all letters.
  - 💀 **Lose** when lives reach zero.
- 🔄 **Duplicate Guess Check** – Warns the player if they repeat a guess.
- 🧩 **Dynamic Word Display** – Shows progress after each guess.
- 📢 **Win/Loss Messages** – Clear game over messages with the correct word if you lose.

---

## 📂 File Structure
hangman/
│
├── main.py           # Main game logic (this file)
├── hangman_words.py  # Contains the list of words
├── hangman_art.py    # Contains the logo & stages ASCII art


## ⚙ How It Works

### 🏁 Game Setup
The program imports:
- `word_list` from `hangman_words.py`
- `logo` & `stages` from `hangman_art.py`

Then it:
- Sets `lives = 6`
- Prints the game logo at the start

---

### 🎯 Random Word Selection
- Picks a random word from `word_list`
- Creates a placeholder (`_ _ _`) for each letter

---

### ⌨ Player Guessing
- Player enters a letter
- If guessed before → program warns and skips turn
- If letter is in the word → updates display with the correct letter
- If not in the word → loses one life

---

### 🏆 / 💀 Game Over Conditions
- If no `_` remain → **You Win** 🎉
- If lives reach `0` → **You Lose** 💀 (and the correct word is revealed)

---

### 🎨 Visual Feedback
- Each wrong guess updates the Hangman ASCII art from `stages`

---

## 🎓 Skills Practiced
- Variables & Strings
- Lists & Loops
- Conditional Statements
- Importing from Other Python Files
- Using ASCII Art in Python
- Game Logic & State Management

---

## 🖼 Example Output
 _                                             
| |                                            
| |__   __ _ _ __   __ _ _ __ ___   __ _ _ __  
| '_ \ / _` | '_ \ / _` | '_ ` _ \ / _` | '_ \ 
| | | | (_| | | | | (_| | | | | | | (_| | | | |
|_| |_|\__,_|_| |_|\__, |_| |_| |_|\__,_|_| |_|
                    __/ |                      
                   |___/                       

Word to guess: _ _ _ _ _
****************************6/6 LIVES LEFT****************************
Guess a letter: a
Word to guess: a _ a _ _
****************************YOU WIN****************************
