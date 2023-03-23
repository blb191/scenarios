# Perform the Calculation

Once the user input has been validated, perform the calculation. Use conditional statements to determine which operation the user wants to perform and then perform the appropriate calculation.

Please enter the following code:

```python
 # Performing the Calculation
    num1 = float(num1)
    num2 = float(num2)
    if operation == "+":
        result = num1 + num2
    elif operation == "-":
        result = num1 - num2
    elif operation == "*":
        result = num1 * num2
    else:
        result = num1 / num2
```
