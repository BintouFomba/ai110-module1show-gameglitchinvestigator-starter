# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [ ] Describe the game's purpose.
- [ ] Detail which bugs you found.
- [ ] Explain what fixes you applied.

## 📸 Demo Walkthrough

Describe your fixed game in numbered steps so a reader can follow along without watching a video:

1. <!-- Describe this step -->
2. <!-- Describe this step -->
3. <!-- Describe this step -->
4. <!-- Describe this step -->
5. <!-- Add more steps as needed -->

**Screenshot** *(optional)*: <!-- Insert a screenshot of your fixed, winning game here -->

## 🧪 Test Results

```
# Paste your pytest output here, e.g.:
# 🎮 Game Glitch Investigator

## 📌 Project Overview
This project is a debugged version of an AI-generated number guessing game built with Streamlit. The original game had multiple bugs affecting gameplay, scoring, and hints.

The goal of this project was to identify and fix those issues, refactor logic into separate modules, and ensure the game works correctly with automated tests.

---

## 🐞 Bugs Found
1. The secret number reset unexpectedly due to improper use of Streamlit session state.
2. Hint messages ("Higher/Lower") were incorrect or misleading.
3. The game logic mixed strings and integers inconsistently.
4. Difficulty settings were not properly applied when restarting the game.
5. Attempt counter started incorrectly, affecting gameplay balance.

---

## 🔧 Fixes Applied
- Used `st.session_state` to persist the secret number.
- Fixed logic in `check_guess()` to return correct outcomes.
- Corrected hint messages in the Streamlit UI.
- Ensured difficulty settings control number range properly.
- Reset game state correctly when starting a new game.
- Separated logic into `logic_utils.py` for better structure and testing.

---

## 🧪 Testing
Pytest was used to verify core game logic:

- Win condition works correctly
- "Too High" and "Too Low" responses are accurate

Run tests with:
# pytest tests/
# ========================= X passed in 0.XXs =========================
```

## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, describe the Enhanced UI changes here — a screenshot is optional]
