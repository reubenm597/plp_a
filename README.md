"""
# Python Command-Line Calculator

## Description
A simple calculator that performs basic arithmetic operations.

## Usage
1. Run the script: `python calculator.py`
2. Enter two numbers
3. Choose an operation (+, -, *, /)
4. View the result

## Features
- Addition, subtraction, multiplication, division
- Error handling for invalid inputs
- Clean command-line interface

"""

def calculator():
    print("\nSimple Python Calculator")
    print("----------------------\n")
    
    try:
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))
    except ValueError:
        print("Error: Please enter valid numbers")
        return
    
    print("\nSelect operation:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")
    
    choice = input("Enter choice (1/2/3/4): ")
    
    if choice == '1':
        print(f"\nResult: {num1} + {num2} = {num1 + num2}")
    elif choice == '2':
        print(f"\nResult: {num1} - {num2} = {num1 - num2}")
    elif choice == '3':
        print(f"\nResult: {num1} * {num2} = {num1 * num2}")
    elif choice == '4':
        try:
            print(f"\nResult: {num1} / {num2} = {num1 / num2}")
        except ZeroDivisionError:
            print("\nError: Cannot divide by zero!")
    else:
        print("\nInvalid input! Please select 1-4")

if __name__ == "__main__":
    while True:
        calculator()
        again = input("\nCalculate again? (y/n): ").lower()
        if again != 'y':
            print("\nGoodbye!")
            break
