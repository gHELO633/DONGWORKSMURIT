Start
Output [1] = Motor Services
Output [2] = Basic Maintenance

DECLARE choice, choice1, choice2, quantity, cash integer
DECLARE price, subtotal, discount_rate, discount_amount, discounted_subtotal, tax_rate, tax_amount, final_total, change, balance float
DECLARE service, has_loyalty, loyalty_status string

Output Welcome to Service Station, what can we do for you?
Output Enter Your Choice of Service:
Input choice

If choice == 1
Output [1] - Motor Services
Output 1. Fuel Injection - P250.00
Output 2. CVT Tuning - P350.00

tax_rate = 0.12

Output Enter Your Service Choice:
Input choice1

If choice1 == 1
service = "Fuel Injection"
price = 250
Elif choice1 == 2
service = "CVT Tuning"
price = 350
else
Output Invalid choice


Output Enter Service Quantity:
Input quantity

Output Do you have a Loyalty Card? (yes / no):
Input has_loyalty

subtotal = quantity * price

If has_loyalty == "yes"
If subtotal >= 1000
discount_rate = 0.15
loyalty_status = "VIP Member (15% OFF)"
else
discount_rate = 0.10
loyalty_status = "Normal Member (10% OFF)"

else
discount_rate = 0.00
loyalty_status = "Non-Member (0% OFF)"


Output Your Subtotal for your Service/s is: subtotal
Output Enter Your Cash:
Input cash

If cash >= subtotal
change = cash - subtotal
discount_amount = subtotal * discount_rate
discounted_subtotal = subtotal - discount_amount
tax_amount = discounted_subtotal * tax_rate
final_total = discounted_subtotal + tax_amount

Output ==================================================
Output OFFICIAL RECEIPT
 Output ==================================================
Output Service: service x(quantity)
Output Subtotal Service: subtotal
Output Cash: cash
Output Change: change
Output Loyalty Tier: loyalty_status
Output Discount: discount_amount
Output VAT (12%): tax_amount
Output --------------------------------------------------
Output TOTAL AMOUNT DUE: final_total
Output ==================================================
Output Ride safe! Thank you for Choosing us!
Output ==================================================
else
balance = subtotal - cash
Output ==================================================
Output Insufficient Cash
Output Balance: balance
Output ==================================================


Elif choice == 2
Output [2] - Basic Maintenance
Output 1. Change Engine Oil & Oil Filter - P350.00
Output 2. Change Gear Oil - P250.00

tax_rate = 0.12

Output Enter Your Service Choice:
Input choice2

If choice2 == 1
service = "Change Engine Oil & Oil Filter"
price = 350
Elif choice2 == 2
service = "Change Gear Oil"
price = 250
else
Output Invalid choice


Output Enter Service Quantity:
Input quantity

Output Do you have a Loyalty Card? (yes / no):
Input has_loyalty

subtotal = quantity * price

If has_loyalty == "yes"
If subtotal >= 1000
discount_rate = 0.15
loyalty_status = "VIP Member (15% OFF)"
else
discount_rate = 0.10
loyalty_status = "Normal Member (10% OFF)"

else
discount_rate = 0.00
loyalty_status = "Non-Member (0% OFF)"


Output Your Subtotal for your Service/s is: subtotal
Output Enter Your Cash:
Input cash

If cash >= subtotal
change = cash - subtotal
discount_amount = subtotal * discount_rate
discounted_subtotal = subtotal - discount_amount
tax_amount = discounted_subtotal * tax_rate
final_total = discounted_subtotal + tax_amount

Output ==================================================
Output OFFICIAL RECEIPT
 Output ==================================================
Output Service: service x(quantity)
Output Subtotal Service: subtotal
Output Cash: cash
Output Change: change
Output Loyalty Tier: loyalty_status
Output Discount: discount_amount
Output VAT (12%): tax_amount
Output --------------------------------------------------
Output TOTAL AMOUNT DUE: final_total
Output ==================================================
Output Ride safe! Thank you for Choosing us!
Output ==================================================
else
balance = subtotal - cash
Output ==================================================
Output Insufficient Cash
Output Balance: balance
Output ==================================================

else
Output Invalid Choice
end if

end
