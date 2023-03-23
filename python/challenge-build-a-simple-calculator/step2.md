# Validate User Input

Validate the user input to make sure it is correct. Check that the user has entered two numbers and a valid operation (+, -, \*, or /). Use the `isdigit()` method to check if a string contains only digits.

If the input is invalid, print an error message and return to Step 1.

Please enter the following code:

```python
# Validating User Input
    if not (num1.isdigit() and num2.isdigit()):
        print("Please enter valid numbers")
        return
    elif operation not in ["+", "-", "*", "/"]:
        print("Please enter a valid operation")
        return
```
