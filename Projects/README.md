# Bagels - A Deductive Logic Game

## Problem Statement
**Bagels** is a number deduction game where the player must guess a secret three-digit number based on clues provided by the game. The program offers three types of hints in response to each guess:

- **"Pico"**: A correct digit is present but in the wrong position.
- **"Fermi"**: A correct digit is in the correct position.
- **"Bagels"**: No digit is correct.

The player has **10 attempts** to guess the secret number correctly.

## Code
Below is the complete Python implementation of the **Bagels** game:

```python
"""Bagels, by Al Sweigart"""
import random

NUM_DIGITS = 3  # Number of digits in the secret number
MAX_GUESSES = 10  # Maximum number of guesses allowed

def main():
    print('''Bagels, a deductive logic game.
By Al Sweigart

I am thinking of a {}-digit number with no repeated digits.
Try to guess what it is. Here are some clues:
When I say:    That means:
  Pico         One digit is correct but in the wrong position.
  Fermi        One digit is correct and in the right position.
  Bagels       No digit is correct.
'''.format(NUM_DIGITS))
    
    while True:
        secretNum = getSecretNum()
        print('I have thought up a number.')
        print('You have {} guesses to get it.'.format(MAX_GUESSES))
        
        numGuesses = 1
        while numGuesses <= MAX_GUESSES:
            guess = ''
            while len(guess) != NUM_DIGITS or not guess.isdecimal():
                print('Guess #{}: '.format(numGuesses))
                guess = input('> ')
            
            clues = getClues(guess, secretNum)
            print(clues)
            numGuesses += 1
            
            if guess == secretNum:
                break
            if numGuesses > MAX_GUESSES:
                print('You ran out of guesses. The answer was {}.'.format(secretNum))
        
        print('Do you want to play again? (yes or no)')
        if not input('> ').lower().startswith('y'):
            break
    print('Thanks for playing!')

def getSecretNum():
    """Returns a string made up of NUM_DIGITS unique random digits."""
    numbers = list('0123456789')
    random.shuffle(numbers)
    secretNum = ''.join(numbers[:NUM_DIGITS])
    return secretNum

def getClues(guess, secretNum):
    """Returns a string with the pico, fermi, bagels clues for a guess and secret number pair."""
    if guess == secretNum:
        return 'You got it!'
    
    clues = []
    for i in range(len(guess)):
        if guess[i] == secretNum[i]:
            clues.append('Fermi')
        elif guess[i] in secretNum:
            clues.append('Pico')
    
    if len(clues) == 0:
        return 'Bagels'
    else:
        clues.sort()
        return ' '.join(clues)

if __name__ == '__main__':
    main()
```


## Example Output
Here is an example session of the program:

```
Bagels, a deductive logic game.
By Al Sweigart

I am thinking of a 3-digit number with no repeated digits.
Try to guess what it is. Here are some clues:
When I say:    That means:
  Pico         One digit is correct but in the wrong position.
  Fermi        One digit is correct and in the right position.
  Bagels       No digit is correct.

I have thought up a number.
You have 10 guesses to get it.

Guess #1:
> 123
Pico

Guess #2:
> 456
Bagels

Guess #3:
> 178
Pico Pico

Guess #7:
> 791
Fermi Fermi

Guess #8:
> 791
You got it!

Do you want to play again? (yes or no)
> no
Thanks for playing!
```
## How it Works
Keep in mind that this program uses not integer values but rather string
values that contain numeric digits. For example, '426' is a different value
than 426. We need to do this because we are performing string comparisons
with the secret number, not math operations. Remember that '0' can be
a leading digit: the string '026' is different from '26', but the integer 026 is
the same as 26.

## Exploration Questions

1. **What happens when you change the `NUM_DIGITS` constant?**
2. **What happens when you change the `MAX_GUESSES` constant?**
3. **What happens if you set `NUM_DIGITS` to a number larger than 10?**
4. **What happens if you replace `secretNum = getSecretNum()` on line 30 with `secretNum = '123'`?**
5. **What error message do you get if you delete or comment out `numGuesses = 1` on line 34?**
6. **What happens if you delete or comment out `random.shuffle(numbers)` on line 62?**
7. **What happens if you delete or comment out `if guess == secretNum:` on line 74 and `return 'You got it!'` on line 75?**
8. **What happens if you comment out `numGuesses += 1` on line 44?**

---

