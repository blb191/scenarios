# Solution
```python
import unittest
from io import StringIO
from unittest.mock import patch

def run_simple_calculator(num1, num2, operation):
    with patch('sys.stdout', new=StringIO()) as fake_out:
        with patch('builtins.input', side_effect=[num1, num2, operation]):
            simple_calculator()
    return fake_out.getvalue().strip()

class TestStep1(unittest.TestCase):
    
    def test_input_numbers_and_operation(self):
        with patch('builtins.input', side_effect=["10", "5", "+"]):
            num1, num2, operation = get_user_input()
        self.assertEqual(num1, "10")
        self.assertEqual(num2, "5")
        self.assertEqual(operation, "+")

class TestStep2(unittest.TestCase):
    
    def test_valid_input(self):
        result = validate_user_input("10", "5", "+")
        self.assertEqual(result, None)
        
    def test_invalid_input(self):
        result = validate_user_input("abc", "def", "@")
        self.assertEqual(result, "Please enter valid numbers")

class TestStep3(unittest.TestCase):
    
    def test_addition(self):
        result = perform_calculation(10, 5, "+")
        self.assertEqual(result, 15.0)

    def test_subtraction(self):
        result = perform_calculation(10, 5, "-")
        self.assertEqual(result, 5.0)

    def test_multiplication(self):
        result = perform_calculation(10, 5, "*")
        self.assertEqual(result, 50.0)

    def test_division(self):
        result = perform_calculation(10, 5, "/")
        self.assertEqual(result, 2.0)

class TestStep4(unittest.TestCase):
    
    def test_display_result(self):
        with patch('sys.stdout', new=StringIO()) as fake_out:
            display_result(15.0)
        self.assertEqual(fake_out.getvalue().strip(), "Result: 15.0")

if __name__ == '__main__':
    unittest.main()