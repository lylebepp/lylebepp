import random

def guess_the_number():
    # Define the range for the random number
    lower_bound = 1
    upper_bound = 100

    # Generate a random number between lower_bound and upper_bound
    number_to_guess = random.randint(lower_bound, upper_bound)
    
    attempts = 0
    guess = None

    print(f"Guess the number between {lower_bound} and {upper_bound}")

    while guess != number_to_guess:
        try:
            guess = int(input("Enter your guess: "))
            attempts += 1
            
            if guess < number_to_guess:
                print("Too low! Try again.")
            elif guess > number_to_guess:
                print("Too high! Try again.")
            else:
                print(f"Congratulations! You've guessed the number {number_to_guess} in {attempts} attempts.")
        except ValueError:
            print("Please enter a valid integer.")

# Run the game
if __name__ == "__main__":
    guess_the_number()
