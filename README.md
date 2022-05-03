

# numberguess
Guessing Game in python
'''
1 to 100
if user guesses wrong then another clue is given
but score reduced.
'''

import random
def guessing_game():
    number = random.randint(1, 100)
    count = 1
    guesses = 10

    while 1 <= guesses:
        user_guesses = int(input("Enter number you wish to guess: "))
        if user_guesses > number:
            print("Your guess was way too high: Guess a number lower than", user_guesses)
        elif user_guesses < number:
            print("Your guess was too low: Guess a number higher than", user_guesses)
        else:
            print("You guessed the number properly")
            print(count, "number of guesses took")
            break
        guesses -= 1
        print(guesses, "guesses reduced")
        count += 1
        print()
    print("game over")
    print("Number is", number)
guessing_game()
