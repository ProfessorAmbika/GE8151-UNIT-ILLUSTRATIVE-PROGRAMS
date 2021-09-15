# Problem Statement
___
**Shankar and Vijay are playing a game of integers in which Shankar chooses an integer in his mind (can be any integer value with in range of 1 to 100 ) and Vijay had to find that integer through some guesses.**
___

_Shankar can provides 3 hints to Vijay ,each hint can be one of the below types:_
* Type 1 : Guess is Low
* Type 2 : Guess is High
* Type 3 : You guessed my number!

Now Vijay has to make some guesses in order to find Shankar's integer.
___

**Note:**  vijay is given only 10 chances to guess the number and if vijay wins the game then return true otherwise return false.



# Solution
~~~python
"""Guess the Number Try to guess the secret number based on hints."""

import random

def ask_for_guess():
    '''returns an integer number as guessed by the user'''
    while True:
        guess = input('> ')  # Enter the guess.

        if guess.isdecimal():
            return int(guess)  # Convert string guess to an integer.
        print('Please enter a number between 1 and 100.')

print('*** Guess the Number ***')
print()
secretNumber = random.randint(1, 100)  # Select a random number.
print('I am thinking of a number between 1 and 100.')

for i in range(10):  # Give the player 10 guesses.
    print('You have {} guesses left. Take a guess.'.format(10 - i))

    guess = ask_for_guess()
    if guess == secretNumber:
        break  # Break out of the for loop if the guess is correct.

    # Offer a hint:
    if guess < secretNumber:
        print('Your guess is too low.')
    if guess > secretNumber:
        print('Your guess is too high.')

# Reveal the results:
if guess == secretNumber:
    print('Yay! You guessed my number!')
else:
    print('Game over. The number I was thinking of was', secretNumber)
~~~

replit-https://replit.com/@profsathish/GuessANumberGame#main.py