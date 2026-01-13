"""
Patil's Caffe Ordering System
This script manages customer orders and calculates total billing.
"""

# Define the menu of caffe items
Caffe_Menu ={
    "Pizza" : 180,
    "Pasta" : 120,
    "Burger" : 90,
    "Salad" : 110,
    "Sandwich" : 70,
    "Coffee" :85,
}

# Greeting message
print("welcome to Patil's Caffe!")
print("Here is our menu:")

# Display the menu
print("Pizza: RS180 \nPasta: RS120 \nBurger: RS90 \nSalad: RS110 \nSandwich: RS70 \nCoffee: RS85")

order_total=0

item_1=input("Enter the first item you want to order:-")
if item_1 in Caffe_Menu:
    order_total += Caffe_Menu[item_1]
    print(f"Your item {item_1} has been added to the order.")
else:
    print(f"Sorry, {item_1} is not available in the menu.")

another_order=input("Do you want to order another item? (yes/no):-")
if another_order=="yes":
    item_2=input("Enter the second item you want to order:-")
    if item_2 in Caffe_Menu:
        order_total += Caffe_Menu[item_2]
        print(f"Your item {item_2} has been added to the ordrer.")
    else:
        print(f"Sorry, {item_2} is not available in the menu.")

print(f"Your total order amount is: RS{order_total}")
