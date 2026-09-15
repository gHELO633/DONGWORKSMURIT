CATEGORIES = {
    1: {
        "title": "Major Services",
        "items": {
            1: ("Fuel Injection", 250.00),
            2: ("CVT Tuning", 350.00),
            3: ("Tuning / Repack Front/Rear Suspension", 270.00),
            4: ("Wiring", 150.00),
            5: ("Fork Wire", 300.00),
            6: ("FI Cleaning", 450.00),
            7: ("Reset ECU", 150.00),
            8: ("FI Cleaning", 125.00),
            9: ("Change Tire", 500.00),
        }
    },
    2: {
        "title": "Basic Maintenance",
        "items": {
            1: ("Change Engine Oil & Oil Filter", 350.00),
            2: ("Change Gear Oil", 250.00),
            3: ("Brake Check", 150.00),
            4: ("Throttle Body Cleaning", 200.00),
            5: ("Spark Plug Check", 300.00),
            6: ("Air Filter Check/Replacement", 150.00),
            7: ("CVT Cleaning", 250.00),
            8: ("FI Cleaning", 200.00),
        }
    }
}

TAX_RATE = 0.12

def calculate_discount(has_loyalty, subtotal):
    """Calculates discount rate and status based on loyalty and spend."""
    if has_loyalty == "yes":
        if subtotal >= 1000:
            return 0.15, "VIP Member (15% OFF)"
        return 0.10, "Normal Member (10% OFF)"
    return 0.00, "Non-Member (0% OFF)"

def process_transaction():
    cart = []  # List to store multiple services: [{"name": name, "price": price, "qty": qty, "total": total}]
    
    while True:
        # 1. Main Category Menu
        print("=" * 50)
        print("           DANGERKROSS SERVICES           ")
        print("=" * 50)
        print("[1] - Major Services")
        print("[2] - Basic Maintenance")
        print("=" * 50)
        
        try:
            main_choice = int(input("Enter Your Choice of Service Category [1-2]: "))
            if main_choice not in CATEGORIES:
                print("INVALID CHOICE! Please select only between [1-2].\n")
                continue

            category = CATEGORIES[main_choice]
            items = category["items"]

            # 2. Sub-Category Menu
            print("\n" + "=" * 50)
            print(f"           {category['title'].upper()}           ")
            print("=" * 50)
            for key, (name, price) in items.items():
                print(f"[{key}] - {name:<38} - ₱{price:.2f}")
            print("=" * 50)

            sub_choice = int(input(f"Enter Your Choice of Service [1-{len(items)}]: "))
            if sub_choice not in items:
                print(f"INVALID CHOICE! Please select only between [1-{len(items)}].\n")
                continue

            service_name, unit_price = items[sub_choice]
            print(f"\n*** Selected: {service_name} - ₱{unit_price:.2f} ***")

            quantity = int(input("Enter Service Quantity: "))
            item_total = unit_price * quantity
            
            # Save selected service to cart
            cart.append({
                "name": service_name,
                "unit_price": unit_price,
                "qty": quantity,
                "total": item_total
            })
            print(f"-> Added {quantity}x {service_name} to cart.")

            # Prompt for additional services
            more = input("\nWould you like to add another service? (yes / no): ").strip().lower()
            if more != "yes":
                break

        except ValueError:
            print("Invalid input! Please enter numbers only.\n")

    if not cart:
        print("No services selected. Exiting transaction.")
        return

    # 3. Overall Checkout Processing
    has_loyalty = input("\nDo you have a Dangerkross Loyalty Card? (yes / no): ").strip().lower()
    
    overall_subtotal = sum(item["total"] for item in cart)
    discount_rate, loyalty_status = calculate_discount(has_loyalty, overall_subtotal)
    
    print(f"\nYour Subtotal for all Service/s is: ₱{overall_subtotal:.2f}")
    
    while True:
        try:
            cash = float(input("Enter Your Cash: ₱"))
            if cash < overall_subtotal:
                balance = overall_subtotal - cash
                print("\n" + "=" * 50)
                print("Insufficient Cash!")
                print(f"Balance Due: ₱{balance:.2f}")
                print("=" * 50 + "\n")
                continue
            break
        except ValueError:
            print("Please enter a valid cash amount.")

    # 4. Final Calculations
    change = cash - overall_subtotal
    discount_amount = overall_subtotal * discount_rate
    discounted_subtotal = overall_subtotal - discount_amount
    tax_amount = discounted_subtotal * TAX_RATE
    final_total = discounted_subtotal + tax_amount

    # 5. Itemized Official Receipt Display
    print("\n" + "=" * 50)
    print("                 OFFICIAL RECEIPT                ")
    print("=" * 50)
    print("SERVICES RENDERED:")
    for item in cart:
        print(f" - {item['name']} (x{item['qty']}) @ ₱{item['unit_price']:.2f} = ₱{item['total']:.2f}")
    
    print("-" * 50)
    print(f"Subtotal Service:    ₱{overall_subtotal:.2f}")
    print(f"Cash:                ₱{cash:.2f}")
    print(f"Change:              ₱{change:.2f}")
    print(f"Loyalty Tier:        {loyalty_status}")
    print(f"Discount:            ₱{discount_amount:.2f}")
    print(f"VAT (12%):           ₱{tax_amount:.2f}")
    print("=" * 50)
    print(f"TOTAL AMOUNT DUE:    ₱{final_total:.2f}")
    print("=" * 50)
    print("          Ride safe! Thank you for Choosing us!    \n")

if __name__ == "__main__":
    process_transaction()
 




