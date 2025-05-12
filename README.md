# NUMBER-GUESSING-GAME--
main.py
import random 

low = 1
high = 100

answer = random.randint(low, high)
guesses = 0
is_running = True

print("Python Number Guessing Game")
print(f"Select a number between {low} and {high}")

while is_running:
    guess = input("Enter your guess:- ")
    
    if guess.isdigit():
        guess = int(guess)
        guesses += 1

        if guess < low or guess > high:
            print("Out of range")
            print(f"select a number between {low} and {high}")
        elif guess < answer:
            print("Too low! Try again!")
        elif guess > answer:
            print("Too high! Try again!")
        else:
            print(f"CORRECT!The answer was {answer} ")
            print(f"Number of guesses: {guesses} ")
            is_runnung = False            
        
    else:
        print("Invalid") 
        print(f"select a number between {low} and {high}")   
