# python-project-1-Trivia-game
# 🧠 Python Trivia Game
import random  

questions = {
    "What is the keyword to define a function in python?": "def",
    "Which data type is used to store True or False Values?": "boolean",
    "What is the corrrect file extension for python values?": ".py",
    "Which symbol is used to comment i python?": "#",
    "What function is used to get input from the user?": "input",
    "How do you start a for loop in python?": "for",
    "What is the output of 2 ** 3 in python?": "8",
    "What keyword is used to import a module in python?": "import",
    "What does the len() function return?": "length",
    "What is the result of 10 // 3in python?": "3"
}

def python_trivia_game():
    questions_list = list(questions.keys())
    total_questions = 5
    score = 0

    selected_questions = random.sample(questions_list, total_questions)

    for idx, question in enumerate(selected_questions):
        print(f"{idx + 1}. {question}")
        user_answer = input("Your answer: ").lower().strip()
        correct_answer = questions[question]
         

        if user_answer == correct_answer.lower():
            print("Correct!\n")
            score += 1
        else:
            print(f"Wrong. The correct answer is: {correct_answer}.\n")

    print(f"Game over! Your final Score is: {score}/{total_questions}")

python_trivia_game()



A fun and interactive **command-line Python Trivia Game** that tests your knowledge of Python fundamentals.  
The program randomly selects 5 questions from a predefined set, checks your answers, and displays your final score.

---

## 🚀 Features
- Randomly selects 5 unique questions per game session  
- Case-insensitive answer checking  
- Displays whether each answer is correct or not  
- Keeps track of your total score  
- Simple, clean, and beginner-friendly code  

---

## 🛠️ Requirements
- Python **3.x**
- No third-party libraries are required (uses only Python’s built-in modules)

---

## 📚 Libraries Used

| Library | Type | Purpose |
|----------|------|----------|
| `random` | Built-in | Used to randomly select 5 questions from the question bank using `random.sample()` |

---

## 🧩 Functions Used

### **1. `python_trivia_game()`**
This is the **main function** that runs the entire trivia game.

#### Inside this function:
| Code Component | Description |
|----------------|--------------|
| `questions_list = list(questions.keys())` | Converts the dictionary keys (questions) into a list for easy sampling |
| `random.sample(questions_list, total_questions)` | Selects 5 random questions without repetition |
| `enumerate(selected_questions)` | Loops through each question with an index number |
| `input()` | Takes the user’s answer from the keyboard |
| `str.lower()` and `str.strip()` | Normalizes user input for case-insensitive comparison |
| `if user_answer == correct_answer.lower():` | Checks if the user's answer matches the correct one |
| `score += 1` | Increments the score for each correct answer |
| `print()` | Displays the question, correctness feedback, and final score |

---

## 🧠 Data Structures Used

### **Dictionary**
All questions and answers are stored in a Python dictionary named `questions`:
```python
questions = {
    "What is the keyword to define a function in python?": "def",
    "Which data type is used to store True or False Values?": "boolean",
    ...
}

