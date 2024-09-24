                def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error! Division by zero."
    return x / y

# Main function to run the calculator
def calculator():
    print("Welcome to the Simple Calculator!")
    
    # Get user input
    try:
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))
    except ValueError:
        print("Invalid input! Please enter numeric values.")
        return
    
    print("Choose an operation:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")

    operation = input("Enter your choice (1/2/3/4): ")

    if operation == '1':
        result = add(num1, num2)
        print(f"The result of {num1} + {num2} = {result}")
    elif operation == '2':
        result = subtract(num1, num2)
        print(f"The result of {num1} - {num2} = {result}")
    elif operation == '3':
        result = multiply(num1, num2)
        print(f"The result of {num1} * {num2} = {result}")
    elif operation == '4':
        result = divide(num1, num2)
        print(f"The result of {num1} / {num2} = {result}")
    else:
        print("Invalid operation choice! Please choose 1, 2, 3, or 4.")

# Run the calculator
calculator()
