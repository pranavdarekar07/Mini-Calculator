print("Mini Calculator")

def adds(num1, num2):
    return num1 + num2

def subtracts(num1, num2):
    return num1 - num2

def divides(num1, num2):
    if num2 == 0:
        return "Cannot divide by zero!"
    return num1 / num2

def multiplies(num1, num2):
    return num1 * num2

while True:
    try:
        num1 = float(input("Enter First Number : "))
        num2 = float(input("Enter Second Number : "))
        operations = input("Add / Sub / Div / Mul / Exit : ").replace(" ", "").lower()

        if operations == "exit":
            break
        elif operations == "add":
            result = adds(num1, num2)
            print(f"{num1} + {num2} = {result}")
        elif operations == "sub":
            result = subtracts(num1, num2)
            print(f"{num1} - {num2} = {result}")
        elif operations == "div":
            result = divides(num1, num2)
            print(f"{num1} / {num2} = {result}")
        elif operations == "mul":
            result = multiplies(num1, num2)
            print(f"{num1} * {num2} = {result}")
        else:
            print("Invalid operation. Please choose Add, Sub, Div, or Mul.")

    except ValueError:
        print("Invalid input. Please enter numbers.")
    except Exception as e:
        print(f"An error occurred: {e}")
