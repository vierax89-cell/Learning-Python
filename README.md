# Learning-Python
This is my recorded progress in terms of learning python.
Day- 1 
Today I tried to make a functioning code for a calculator with basic functions.
The code goes as such:


def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b == 0:
        return "Error: cannot divide by zero"
    return a / b

print("Simple Calculator")
print("+, -, *, /")

while True:
    try:
        num1 = float(input("Enter first number: "))
        op = input("Enter operator (+, -, *, /): ")
        num2 = float(input("Enter second number: "))

        if op == "+":
            result = add(num1, num2)
        elif op == "-":
            result = subtract(num1, num2)
        elif op == "*":
            result = multiply(num1, num2)
        elif op == "/":
            result = divide(num1, num2)
        else:
            print("Invalid operator")
            continue

        print(f"Result: {result}")

    except ValueError:
        print("Please enter valid numbers.")

    again = input("Do another calculation? (y/n): ").lower()
    if again != "y":
        break

print("Goodbye!")
