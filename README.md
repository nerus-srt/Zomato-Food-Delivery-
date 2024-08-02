# Zomato-Food-Delivery-Fee
 
# Project Overview

**Project Name**: Food Delivery Fees  
**Objective**: To inform users about the delivery fees and conditions for food delivery based on their total payable amount.

## Project Requirements and Dependencies

- **Python**: Used to write the script.
- **No additional libraries required**.

## Steps

1. **User Input**:
   - Prompt the user to enter their name.
   - Prompt the user to enter their delivery address.
   - Prompt the user to enter the total payable amount.

2. **Delivery Fee Check**:
   - If the total amount is greater than 100, inform the user about free delivery.
   - If the total amount is 100 or less, inform the user about the minimum purchase requirement for free delivery.

## Code

```python
# Programmer: Suren Raj Tuladhar
# Date: 18/07/2022
# Program: Food Delivery Fees

def get_user_input():
    name = input("Enter your name: ")
    address = input("Enter your delivery address: ")
    amount = input("Enter the total payable amount: ")
    return name, address, amount

def check_delivery_fee(amount):
    try:
        amount = int(amount)
        if amount > 100:
            print("Congratulations!")
            print("Your food will be delivered in 30 minutes.")
            print("Enjoy our free delivery service.")
            print("Bon Appétit!")
            print("For more, contact us @ +971 524707211")
        else:
            print("Congratulations!")
            print("Your food will be delivered in 30 minutes.")
            print("To enjoy our free delivery service, the minimum purchase order is AED 100.")
            print("Bon Appétit!")
            print("For more, contact us @ +971 524707211")
    except ValueError:
        print("Invalid input for amount. Please enter a number.")

def main():
    name, address, amount = get_user_input()
    check_delivery_fee(amount)

if __name__ == "__main__":
    main()
