# Get User Input

Prompt the user to enter two numbers and an operation (+, -, \*, or /). Use the `input()` function to get input from the user.

First, open up a new Python interpreter.

```bash
python3
```

Then, create a simple_calculator function.

```python
def simple_calculator() -> None:

    """
    This function prompts the user to enter two numbers and an operation (+, -, *, or /),
    validates the user input to make sure it is correct,
    performs the appropriate calculation based on the operation entered,
    and displays the result to the user.
    """
```

Next, enter the following code to get user input.

```python
#Get user input
    num1 = input("Enter the first number: ")
    num2 = input("Enter the second number: ")
    operation = input("Enter an operation (+, -, *, or /): ")
```
