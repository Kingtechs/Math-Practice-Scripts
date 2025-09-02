# Math-Practice-Scripts
Something fun for my 5th Grade class to do
import random

def multiplication_quiz():
    print("Welcome to the Multiplication Quiz!")
    print("Type 'exit' anytime to quit.\n")

    score = 0
    total = 0

    while True:
        # Generate two random numbers between 1 and 12
        num1 = random.randint(1, 12)
        num2 = random.randint(1, 12)
        correct_answer = num1 * num2

        # Ask the question
        user_input = input(f"What is {num1} x {num2}? ")

        if user_input.lower() == "exit":
            break

        # Check if input is a number
        if not user_input.isdigit():
            print("Please enter a number.\n")
            continue

        # Convert input and check answer
        user_answer = int(user_input)
        total += 1

        if user_answer == correct_answer:
            print("✅ Correct!\n")
            score += 1
        else:
            print(f"❌ Wrong. The correct answer was {correct_answer}.\n")

    print(f"\nQuiz ended. You got {score} out of {total} correct.")
    print("Thanks for playing!")

if __name__ == "__main__":
    multiplication_quiz()
