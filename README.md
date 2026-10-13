# Hangman

A classic word-guessing game for the command line, written in Python. Guess the hidden word one letter at a time before you run out of attempts.

## Features

- Random word chosen from a built-in word list
- ASCII art that updates with each wrong guess
- Tracks guessed letters and rejects repeated or invalid input
- Win and lose messages that reveal the word
- Option to play again after each round

## Requirements

- Python 3.6 or higher
- No external libraries needed

## Installation

1. Clone or download this repository:

   ```bash
   git clone https://github.com/your-username/hangman.git
   cd hangman
   ```

2. That's it. There is nothing else to install.

## Usage

Run the game:

```bash
python hangman.py
```

### How to Play

1. The game picks a secret word and shows it as blanks, like `_ _ _ _ _ _`.
2. Type one letter and press Enter.
3. If the letter is in the word, it is revealed in every position where it appears.
4. If not, you lose one attempt and the hangman drawing grows.
5. You win by guessing every letter. You lose after 6 wrong guesses.

### Example

```
Word: _ _ _ _ _ _
Wrong guesses left: 6
Guessed: 

Guess a letter: e
Good guess!

Word: _ _ _ _ E _
Wrong guesses left: 6
Guessed: e

Guess a letter: z
Wrong!

  +---+
  |   |
  O   |
      |
      |
      |
=========
Wrong guesses left: 5
```

## Project Structure

```
hangman/
├── hangman.py    # Main game
├── words.txt     # Optional custom word list
└── README.md     # This file
```

## How It Works

- **Lists and sets** store the word, the guessed letters, and the wrong guesses.
- **Loops** keep the game running until the player wins or runs out of attempts.
- **Functions** handle displaying the board, checking guesses, and restarting the game.
- **if-elif** statements decide whether a guess is correct, repeated, or invalid.
- **The `random` module** picks a different word each round.

## Customization

- Add your own words to the word list (one per line in `words.txt`).
- Change the number of allowed wrong guesses by editing `MAX_ATTEMPTS` in `hangman.py`.

## Future Improvements

- Difficulty levels based on word length
- Word categories (animals, countries, movies)
- Hint feature
- Score tracking across rounds
- Simple GUI version

## License

This project is licensed under the MIT License.
