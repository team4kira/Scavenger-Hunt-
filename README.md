# Scavenger-Hunt-

# A Scavenger Hunt made with Python

def ask_question(question, correct_answer, statement):
    while True:
        answer = input(question + "\nYour answer: ")
        if answer.lower() == correct_answer.lower():
            print("Correct! " + statement + "\n")
            input("Press Enter to move to the next question.\n")
            return True
        else:
            print("Incorrect answer. Try again.")

def scavenger_hunt():
    questions = [
    {"question": "What is the capital of France?", "answer": "Paris", "statement": "Go to Denny's."},
    {"question": "What is 5 + 7?", "answer": "12", "statement": "Go to the mall."},
    {"question": "What is the largest planet in our solar system?", "answer": "Jupiter", "statement": "Head to the park."}
  ]

    for q in questions:
        ask_question(q["question"], q["answer"], q["statement"])

    print("Congratulations! You've completed the Scavenger Hunt!")

if __name__ == "__main__":
    scavenger_hunt()
