import random

def number_guess_game():
    # Randomly select a number between 1 and 100
    number_to_guess = random.randint(1, 100)
    attempts = 0
    print("Welcome to the Number Guessing Game!")
    print("I have selected a number between 1 and 100. Try to guess it.")

    while True:
        # Take user input for their guess
        guess = input("Enter your guess: ")

        # Ensure the user input is a valid integer
        if not guess.isdigit():
            print("Please enter a valid number.")
            continue

        guess = int(guess)
        attempts += 1

        # Check if the guess is correct
        if guess < number_to_guess:
            print("Too low! Try again.")
        elif guess > number_to_guess:
            print("Too high! Try again.")
        else:
            print(f"Congratulations! You've guessed the correct number {number_to_guess} in {attempts} attempts.")
            break

# Run the game
if __name__ == "__main__":
    number_guess_game()
