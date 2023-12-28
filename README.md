# Shopping-Cart-Program
Shopping Cart Program 

print("shopping cart program")

foods = []
prices = []
total = 0

while True:
    food = input("Enter a food to buy ( q to quite) : ")
    if food == "q":
        break
    else:
        while True:
            try:
                price = float(input(f"Enter the price of a {food}: Rs. "))
                if price >= 0:
                    break
                else:
                    print("Please enter a valid price. ")
            except ValueError:
                print("please enter a valid number for the price")
        foods.append(food)
        prices.append(price)
print()

print('-------- YOUR ORDER CART-------')


for item, price in zip(foods, prices):
    print(f"{item}: Rs. { price: .2f}")

total =sum(prices)

print(f"Your total is : Rs.{total}")

