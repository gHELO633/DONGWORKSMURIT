Here is a customized Motor Parts & Accessories Shop program that handles inventory selection, calculates tiered loyalty discounts, adds sales tax, and prints an itemized receipt.


# MotoTech Parts & Accessories Shop

print("==========================================")
print("     MOTOTECH PARTS & ACCESSORIES SHOP    ")
print("==========================================")
print("Available Items:")
print("1. Synthetic Engine Oil (1L) - P450.00")
print("2. Performance Brake Pads    - P350.00")
print("3. Drive Chain Set           - P850.00")
print("------------------------------------------")

# Inputs
item_code = int(input("Enter Item Number (1-3): "))
quantity = int(input("Enter Quantity: "))
has_loyalty = input("Do you have a MotoTech VIP Loyalty Card? (yes / no): ").strip().lower()

# Item selection and price mapping
if item_code == 1:
    item_name = "Synthetic Engine Oil (1L)"
    unit_price = 450.00
elif item_code == 2:
    item_name = "Performance Brake Pads"
    unit_price = 350.00
elif item_code == 3:
    item_name = "Drive Chain Set"
    unit_price = 850.00
else:
    item_name = "Universal Spare Part"
    unit_price = 200.00

# Base calculation
subtotal = unit_price * quantity

# Discount calculation based on Loyalty Card status
if has_loyalty == "yes":
    if subtotal >= 1000:
        discount_rate = 0.15  # 15% discount for bulk motor parts orders
        loyalty_status = "VIP Mechanic (15% Off)"
    else:
        discount_rate = 0.10  # 10% standard loyalty discount
        loyalty_status = "Rider Member (10% Off)"
else:
    discount_rate = 0.00
    loyalty_status = "Non-Member (0% Off)"

discount_amount = subtotal * discount_rate
discounted_subtotal = subtotal - discount_amount

# Tax calculation (12% VAT applied after discount)
tax_rate = 0.12
tax_amount = discounted_subtotal * tax_rate
final_total = discounted_subtotal + tax_amount

# Output Receipt
print("\n==========================================")
print("             OFFICIAL RECEIPT             ")
print("==========================================")
print(f"Item/Part:        {item_name} x{quantity}")
print(f"Subtotal:         P{subtotal:.2f}")
print(f"Loyalty Tier:     {loyalty_status}")
print(f"Discount:       - P{discount_amount:.2f}")
print(f"VAT (12%):      + P{tax_amount:.2f}")
print("------------------------------------------")
print(f"TOTAL AMOUNT DUE: P{final_total:.2f}")
print("==========================================")
print("      Ride safe! Thank you for buying!    ")



Why This Fits the Motor Parts Concept:




Motorcycle Niche: Uses real auto/motorcycle items (Engine Oil, Brake Pads, Chain Sets).


Tiered Loyalty Logic: Rewards regular riders or mechanics with 10% off for small purchases and 15% off for higher-value orders (P1,000+).


Complete Financial Computations: Correctly handles Subtotal, Discount, 12% VAT Tax, and Final Total.




