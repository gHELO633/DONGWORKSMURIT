print("-"*100)
print("               Welcome To Dongworkszxc Services & Maintenance, What can we do for you?")
print("-"*100)

print("Our Services & Maintenance: ")
print("[1] = Motor Services")
print("[2] = Basic Maintenance")
print("")
name = input("Enter Your Name:")
choice = int(input("Enter Your Choice of Service: "))


if choice == 1:
    print("")
    print("(Motor Services)")
    print("1. • Fuel Injection                         - ₱250.00  ")
    print("2. • CVT Tuning                             - ₱350.00  ")
    print("3. • Tuning/Repack Front/Rear Suspension    - ₱270.00  ")
    print("4. • Wiring                                 - ₱150.00  ")
    print("5. • Tuck Wire                              - ₱200.00  ")
    print("6. • Tune Up                                - ₱450.00  ")
    print("7. • Reset ECU                              - ₱150.00  ")
    print("8. • Chain Cleaning                         - ₱135.00  ")
    print("9. • Change Tire                            - ₱550.00  ")
    fuel_injection = 250
    cvt_tuning = 350
    repack_suspension = 270
    wiring = 150
    tuck_wire = 200
    tune_up = 450
    reset_ecu = 150
    chain_cleaning = 135
    change_tire = 550
    tax_rate = 0.12

    choice1 = int(input("Enter your Service Choice: "))

    if choice1 == 1:
        service = "Fuel Injection"
        print(f"• Fuel Injection                            - ₱{fuel_injection:.2f}")
        quantity = int(input("Enter Service Quantity: "))
        has_loyalty = input("Do you have a Dongworkszxc Loyalty Card? (yes / no): ").lower()
        subtotal = quantity * fuel_injection

        if has_loyalty == "yes":
            if subtotal >= 1000:
                discount_rate = 0.15
                loyalty_status = "VIP Member (15% Off)"
            else:
                discount_rate = 0.10
                loyalty_status = "Normal Member (10% Off)"
        else:
            discount_rate = 0.00
            loyalty_status = "Non-Member (0% Off)"

        print(f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}")
        cash = int(input("Enter Your Cash: "))

        if cash >= subtotal:
            change = cash - subtotal
            discount_amount = subtotal * discount_rate
            discounted_subtotal = subtotal - discount_amount
            tax_amount = discounted_subtotal * tax_rate
            final_total = discounted_subtotal + tax_amount

            print("\n==========================================")
            print("             OFFICIAL RECEIPT             ")
            print("==========================================")
            print(f"Customer Name: {name}")
            print(f"Service:           {service} x {quantity}")
            print(f"Subtotal Service: ₱{subtotal:.2f}")
            print(f"Cash:             ₱{cash:.2f}")
            print(f"Change:           ₱{change:.2f}")
            print(f"Loyalty Tier:      {loyalty_status}")
            print(f"Discount:       - ₱{discount_amount:.2f}")
            print(f"VAT (12%):      + ₱{tax_amount:.2f}")
            print("------------------------------------------")
            print(f"TOTAL AMOUNT DUE: P{final_total:.2f}")

            print("==========================================")
            print("      Ride safe! Thank you for Choosing us!    ")

        else:
            print("\n==========================================")
            balance = subtotal - cash
            print("Insufficient Cash!")
            print(f"Balance: ₱{balance}")
            print("==========================================")

    elif choice1 == 2:
        service = "CVT Tuning"
        print(f"• CVT Tuning                                - {cvt_tuning:.2f}")
        quantity = int(input("Enter Service Quantity: "))
        has_loyalty = input("Do you have a Dongworkszxc Loyalty Card? (yes / no): ").lower()
        subtotal = quantity * cvt_tuning

        if has_loyalty == "yes":
            if subtotal >= 1000:
                discount_rate = 0.15
                loyalty_status = "VIP Member (15% Off)"
            else:
                discount_rate = 0.10
                loyalty_status = "Normal Member (10% Off)"
        else:
            discount_rate = 0.00
            loyalty_status = "Non-Member (0% Off)"

        print(f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}")
        cash = int(input("Enter Your Cash: "))

        if cash >= subtotal:
            change = cash - subtotal
            discount_amount = subtotal * discount_rate
            discounted_subtotal = subtotal - discount_amount
            tax_amount = discounted_subtotal * tax_rate
            final_total = discounted_subtotal + tax_amount

            print("\n==========================================")
            print("             OFFICIAL RECEIPT             ")
            print("==========================================")
            print(f"Customer Name: {name}")
            print(f"Service:           {service} x {quantity}")
            print(f"Subtotal Service: ₱{subtotal:.2f}")
            print(f"Cash:             ₱{cash:.2f}")
            print(f"Change:           ₱{change:.2f}")
            print(f"Loyalty Tier:      {loyalty_status}")
            print(f"Discount:       - ₱{discount_amount:.2f}")
            print(f"VAT (12%):      + ₱{tax_amount:.2f}")
            print("------------------------------------------")
            print(f"TOTAL AMOUNT DUE: ₱{final_total:.2f}")

            print("==========================================")
            print("      Ride safe! Thank you for Choosing us!    ")

        else:
            print("\n==========================================")
            balance = subtotal - cash
            print("Insufficient Cash!")
            print(f"Balance: ₱{balance}")
            print("==========================================")

    elif choice1 == 3:
        service = "Tuning/Repack Front/Rear Suspension"
        print(f"• Tuning/Repack Front/Rear Suspension       - {repack_suspension:.2f}")
        quantity = int(input("Enter Service Quantity: "))
        has_loyalty = input("Do you have a Dongworkszxc Loyalty Card? (yes / no): ").lower()
        subtotal = quantity * repack_suspension

        if has_loyalty == "yes":
            if subtotal >= 1000:
                discount_rate = 0.15
                loyalty_status = "VIP Member (15% Off)"
            else:
                discount_rate = 0.10
                loyalty_status = "Normal Member (10% Off)"
        else:
            discount_rate = 0.00
            loyalty_status = "Non-Member (0% Off)"

        print(f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}")
        cash = int(input("Enter Your Cash: "))

        if cash >= subtotal:
            change = cash - subtotal
            discount_amount = subtotal * discount_rate
            discounted_subtotal = subtotal - discount_amount
            tax_amount = discounted_subtotal * tax_rate
            final_total = discounted_subtotal + tax_amount

            print("\n==========================================")
            print("             OFFICIAL RECEIPT             ")
            print("==========================================")
            print(f"Customer Name: {name}")
            print(f"Service:           {service} x {quantity}")
            print(f"Subtotal Service: ₱{subtotal:.2f}")
            print(f"Cash:             ₱{cash:.2f}")
            print(f"Change:           ₱{change:.2f}")
            print(f"Loyalty Tier:      {loyalty_status}")
            print(f"Discount:       - ₱{discount_amount:.2f}")
            print(f"VAT (12%):      + ₱{tax_amount:.2f}")
            print("------------------------------------------")
            print(f"TOTAL AMOUNT DUE: ₱{final_total:.2f}")

            print("==========================================")
            print("      Ride safe! Thank you for Choosing us!    ")

        else:
            print("\n==========================================")
            balance = subtotal - cash
            print("Insufficient Cash!")
            print(f"Balance: ₱{balance}")
            print("==========================================")



    elif choice1 == 4:
        service = "Wiring"
        print(f"• Wiring                                   - {wiring:.2f}")
        quantity: int = int(input('Enter Service Quantity : '))
        has_loyalty = input("Do you have a Dongworkszxc Loyalty Card? (yes / no): ").lower()
        subtotal = quantity * wiring

        if has_loyalty == "yes":
            if subtotal >= 1000:
                discount_rate = 0.15
                loyalty_status = "VIP Member (15% Off)"
            else:
                discount_rate = 0.10
                loyalty_status = "Normal Member (10% Off)"
        else:
            discount_rate = 0.00
            loyalty_status = "Non-Member (0% Off)"

        print(f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}")
        cash = int(input("Enter Your Cash: "))

        if cash >= subtotal:
            change = cash - subtotal
            discount_amount = subtotal * discount_rate
            discounted_subtotal = subtotal - discount_amount
            tax_amount = discounted_subtotal * tax_rate
            final_total = discounted_subtotal + tax_amount

            print("\n==========================================")
            print("             OFFICIAL RECEIPT             ")
            print("==========================================")
            print(f"Customer Name: {name}")
            print(f"Service:           {service} x {quantity}")
            print(f"Subtotal Service: ₱{subtotal:.2f}")
            print(f"Cash:             ₱{cash:.2f}")
            print(f"Change:           ₱{change:.2f}")
            print(f"Loyalty Tier:      {loyalty_status}")
            print(f"Discount:       - ₱{discount_amount:.2f}")
            print(f"VAT (12%):      + ₱{tax_amount:.2f}")
            print("------------------------------------------")
            print(f"TOTAL AMOUNT DUE: ₱{final_total:.2f}")

            print("==========================================")
            print("      Ride safe! Thank you for Choosing us!    ")

        else:
            print("\n==========================================")
            balance = subtotal - cash
            print("Insufficient Cash!")
            print(f"Balance: ₱{balance}")
            print("==========================================")

    elif choice1 == 5:
        service = "Tuck Wire "
        print(f"• Tuck Wire                                - {tuck_wire:.2f}")
        quantity = int(input("Enter Service Quantity : "))
        has_loyalty = input("Do you have a Dongworkszxc Loyalty Card? (yes / no): ").lower()
        subtotal = quantity * tuck_wire

        if has_loyalty == "yes":
            if subtotal >= 1000:
                discount_rate = 0.15
                loyalty_status = "VIP Member (15% Off)"
            else:
                discount_rate = 0.10
                loyalty_status = "Normal Member (10% Off)"
        else:
            discount_rate = 0.00
            loyalty_status = "Non-Member (0% Off)"

        print(f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}")
        cash = int(input("Enter Your Cash: "))

        if cash >= subtotal:
            change = cash - subtotal
            discount_amount = subtotal * discount_rate
            discounted_subtotal = subtotal - discount_amount
            tax_amount = discounted_subtotal * tax_rate
            final_total = discounted_subtotal + tax_amount

            print("\n==========================================")
            print("             OFFICIAL RECEIPT             ")
            print("==========================================")
            print(f"Customer Name: {name}")
            print(f"Service:           {service} x {quantity}")
            print(f"Subtotal Service: ₱{subtotal:.2f}")
            print(f"Cash:             ₱{cash:.2f}")
            print(f"Change:           ₱{change:.2f}")
            print(f"Loyalty Tier:      {loyalty_status}")
            print(f"Discount:       - ₱{discount_amount:.2f}")
            print(f"VAT (12%):      + ₱{tax_amount:.2f}")
            print("------------------------------------------")
            print(f"TOTAL AMOUNT DUE: ₱{final_total:.2f}")

            print("==========================================")
            print("      Ride safe! Thank you for Choosing us!    ")

        else:
            print("\n==========================================")
            balance = subtotal - cash
            print("Insufficient Cash!")
            print(f"Balance: ₱{balance}")
            print("==========================================")

    elif choice1 == 6:
        service = "Tune Up"
        print(f"• Tune Up                                  - {tune_up:.2f}")
        quantity = int(input("Enter Service Quantity : "))
        has_loyalty = input("Do you have a Dongworkszxc Loyalty Card? (yes / no): ").lower()
        subtotal = quantity * tune_up

        if has_loyalty == "yes":
            if subtotal >= 1000:
                discount_rate = 0.15
                loyalty_status = "VIP Member (15% Off)"
            else:
                discount_rate = 0.10
                loyalty_status = "Normal Member (10% Off)"
        else:
            discount_rate = 0.00
            loyalty_status = "Non-Member (0% Off)"

        print(f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}")
        cash = int(input("Enter Your Cash: "))

        if cash >= subtotal:
            change = cash - subtotal
            discount_amount = subtotal * discount_rate
            discounted_subtotal = subtotal - discount_amount
            tax_amount = discounted_subtotal * tax_rate
            final_total = discounted_subtotal + tax_amount

            print("\n==========================================")
            print("             OFFICIAL RECEIPT             ")
            print("==========================================")
            print(f"Customer Name: {name}")
            print(f"Service:           {service} x {quantity}")
            print(f"Subtotal Service: ₱{subtotal:.2f}")
            print(f"Cash:             ₱{cash:.2f}")
            print(f"Change:           ₱{change:.2f}")
            print(f"Loyalty Tier:      {loyalty_status}")
            print(f"Discount:       - ₱{discount_amount:.2f}")
            print(f"VAT (12%):      + ₱{tax_amount:.2f}")
            print("------------------------------------------")
            print(f"TOTAL AMOUNT DUE: ₱{final_total:.2f}")

            print("==========================================")
            print("      Ride safe! Thank you for Choosing us!    ")

        else:
            print("\n==========================================")
            balance = subtotal - cash
            print("Insufficient Cash!")
            print(f"Balance: ₱{balance}")
            print("==========================================")

    elif choice1 == 7:
        service = "Reset ECU"
        print(f"• Reset ECU                                 - {reset_ecu:.2f}")
        quantity = int(input("Enter Service Quantity : "))
        has_loyalty = input("Do you have a Dongworkszxc Loyalty Card? (yes / no): ").lower()
        subtotal = quantity * reset_ecu

        if has_loyalty == "yes":
            if subtotal >= 1000:
                discount_rate = 0.15
                loyalty_status = "VIP Member (15% Off)"
            else:
                discount_rate = 0.10
                loyalty_status = "Normal Member (10% Off)"
        else:
            discount_rate = 0.00
            loyalty_status = "Non-Member (0% Off)"

        print(f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}")
        cash = int(input("Enter Your Cash: "))

        if cash >= subtotal:
            change = cash - subtotal
            discount_amount = subtotal * discount_rate
            discounted_subtotal = subtotal - discount_amount
            tax_amount = discounted_subtotal * tax_rate
            final_total = discounted_subtotal + tax_amount

            print("\n==========================================")
            print("             OFFICIAL RECEIPT             ")
            print("==========================================")
            print(f"Customer Name: {name}")
            print(f"Service:           {service} x {quantity}")
            print(f"Subtotal Service: ₱{subtotal:.2f}")
            print(f"Cash:             ₱{cash:.2f}")
            print(f"Change:           ₱{change:.2f}")
            print(f"Loyalty Tier:      {loyalty_status}")
            print(f"Discount:       - ₱{discount_amount:.2f}")
            print(f"VAT (12%):      + ₱{tax_amount:.2f}")
            print("------------------------------------------")
            print(f"TOTAL AMOUNT DUE: ₱{final_total:.2f}")

            print("==========================================")
            print("      Ride safe! Thank you for Choosing us!    ")

        else:
            print("\n==========================================")
            balance = subtotal - cash
            print("Insufficient Cash!")
            print(f"Balance: ₱{balance}")
            print("==========================================")

    elif choice1 == 8:
        service = "Chain Cleaning"
        print(f"• Chain Cleaning                             - {chain_cleaning:.2f}")
        quantity = int(input("Enter Service Quantity : "))
        has_loyalty = input("Do you have a Dongworkszxc Loyalty Card? (yes / no): ").lower()
        subtotal = quantity * chain_cleaning

        if has_loyalty == "yes":
            if subtotal >= 1000:
                discount_rate = 0.15
                loyalty_status = "VIP Member (15% Off)"
            else:
                discount_rate = 0.10
                loyalty_status = "Normal Member (10% Off)"
        else:
            discount_rate = 0.00
            loyalty_status = "Non-Member (0% Off)"

        print(f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}")
        cash = int(input("Enter Your Cash: "))

        if cash >= subtotal:
            change = cash - subtotal
            discount_amount = subtotal * discount_rate
            discounted_subtotal = subtotal - discount_amount
            tax_amount = discounted_subtotal * tax_rate
            final_total = discounted_subtotal + tax_amount

            print("\n==========================================")
            print("             OFFICIAL RECEIPT             ")
            print("==========================================")
            print(f"Customer Name: {name}")
            print(f"Service:           {service} x {quantity}")
            print(f"Subtotal Service: ₱{subtotal:.2f}")
            print(f"Cash:             ₱{cash:.2f}")
            print(f"Change:           ₱{change:.2f}")
            print(f"Loyalty Tier:      {loyalty_status}")
            print(f"Discount:       - ₱{discount_amount:.2f}")
            print(f"VAT (12%):      + ₱{tax_amount:.2f}")
            print("------------------------------------------")
            print(f"TOTAL AMOUNT DUE: ₱{final_total:.2f}")

            print("==========================================")
            print("      Ride safe! Thank you for Choosing us!    ")

        else:
            print("\n==========================================")
            balance = subtotal - cash
            print("Insufficient Cash!")
            print(f"Balance: ₱{balance}")
            print("==========================================")

    elif choice1 == 9:
        service = "Change Tire"
        print(f"• Change Tire                                - {change_tire:.2f}")
        quantity = int(input("Enter Service Quantity : "))
        has_loyalty = input("Do you have a Dongworkszxc Loyalty Card? (yes / no): ").lower()
        subtotal = quantity * change_tire

        if has_loyalty == "yes":
            if subtotal >= 1000:
                discount_rate = 0.15
                loyalty_status = "VIP Member (15% Off)"
            else:
                discount_rate = 0.10
                loyalty_status = "Normal Member (10% Off)"
        else:
            discount_rate = 0.00
            loyalty_status = "Non-Member (0% Off)"

        print(f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}")
        cash = int(input("Enter Your Cash: "))

        if cash >= subtotal:
            change = cash - subtotal
            discount_amount = subtotal * discount_rate
            discounted_subtotal = subtotal - discount_amount
            tax_amount = discounted_subtotal * tax_rate
            final_total = discounted_subtotal + tax_amount

            print("\n==========================================")
            print("             OFFICIAL RECEIPT             ")
            print("==========================================")
            print(f"Customer Name: {name}")
            print(f"Service:           {service} x {quantity}")
            print(f"Subtotal Service: ₱{subtotal:.2f}")
            print(f"Cash:             ₱{cash:.2f}")
            print(f"Change:           ₱{change:.2f}")
            print(f"Loyalty Tier:      {loyalty_status}")
            print(f"Discount:       - ₱{discount_amount:.2f}")
            print(f"VAT (12%):      + ₱{tax_amount:.2f}")
            print("------------------------------------------")
            print(f"TOTAL AMOUNT DUE: ₱{final_total:.2f}")

            print("==========================================")
            print("      Ride safe! Thank you for Choosing us!    ")

        else:
            print("\n==========================================")
            balance = subtotal - cash
            print("Insufficient Cash!")
            print(f"Balance: ₱{balance}")
            print("==========================================")
    else:
        print("Invalid Choice! Please select Between (1-9) Only!")
else:
    print("Invalid Choice! Please select Between (1-2) Only!")


if choice == 2:
    print("")
    print("(Basic Maintenance: )")
    print("1. • Change Engine Oil & Oil Filter        - ₱350  ")
    print("2. • Change Gear Oil                       - ₱250  ")
    print("3. • Break Check                           - ₱150  ")
    print("4. • Throttle Body Cleaning                - ₱200 ")
    print("5. • Spark Plug Check                      - ₱100  ")
    print("6. • Air Filter Check/Replacement          - ₱150  ")
    print("7. • CVT Cleaning                          - ₱200  ")
    print("8. • FI Cleaning                           - ₱250 ")

    engine_oil = 350
    gear_oil = 250
    break_check = 150
    throttle_body = 200
    spark_plug = 100
    air_filter = 150
    cvt_cleaning = 200
    fi_cleaning = 250
    tax_rate = 0.12

    choice2 = int(input("Enter Your Choice of Service: "))

    if choice2 == 1:
        service = "Change Engine Oil & Oil Filter"
        print(f"• Change Engine Oil & Oil Filter                           - ₱{engine_oil:.2f}")
        quantity = int(input("Enter Service Quantity: "))
        has_loyalty = input("Do you have a Dongworkszxc Loyalty Card? (yes / no): ").lower()
        subtotal = quantity * engine_oil

        if has_loyalty == "yes":
            if subtotal >= 1000:
                discount_rate = 0.15
                loyalty_status = "VIP Member (15% Off)"
            else:
                discount_rate = 0.10
                loyalty_status = "Normal Member (10% Off)"
        else:
            discount_rate = 0.00
            loyalty_status = "Non-Member (0% Off)"

        print(f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}")
        cash = int(input("Enter Your Cash: "))

        if cash >= subtotal:
            change = cash - subtotal
            discount_amount = subtotal * discount_rate
            discounted_subtotal = subtotal - discount_amount
            tax_amount = discounted_subtotal * tax_rate
            final_total = discounted_subtotal + tax_amount
            print("\n==========================================")
            print("             OFFICIAL RECEIPT             ")
            print("==========================================")
            print(f"Customer Name: {name}")
            print(f"Service:           {service} x {quantity}")
            print(f"Subtotal Service: ₱{subtotal:.2f}")
            print(f"Cash:             ₱{cash:.2f}")
            print(f"Change:           ₱{change:.2f}")
            print(f"Loyalty Tier:      {loyalty_status}")
            print(f"Discount:       - ₱{discount_amount:.2f}")
            print(f"VAT (12%):      + ₱{tax_amount:.2f}")
            print("------------------------------------------")
            print(f"TOTAL AMOUNT DUE: P{final_total:.2f}")

            print("==========================================")
            print("      Ride safe! Thank you for Choosing us!    ")

        else:
            print("\n==========================================")
            balance = subtotal - cash
            print("Insufficient Cash!")
            print(f"Balance: ₱{balance}")
            print("==========================================")

    elif choice2 == 2:
        service = "Change Gear Oil"
        print(f"• Change Gear Oil                                          - {gear_oil:.2f}")
        quantity = int(input("Enter Service Quantity: "))
        has_loyalty = input("Do you have a Dongworkszxc Loyalty Card? (yes / no): ").lower()
        subtotal = quantity * gear_oil

        if has_loyalty == "yes":
            if subtotal >= 1000:
                discount_rate = 0.15
                loyalty_status = "VIP Member (15% Off)"
            else:
                discount_rate = 0.10
                loyalty_status = "Normal Member (10% Off)"
        else:
            discount_rate = 0.00
            loyalty_status = "Non-Member (0% Off)"

        print(f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}")
        cash = int(input("Enter Your Cash: "))

        if cash >= subtotal:
            change = cash - subtotal
            discount_amount = subtotal * discount_rate
            discounted_subtotal = subtotal - discount_amount
            tax_amount = discounted_subtotal * tax_rate
            final_total = discounted_subtotal + tax_amount

            print("\n==========================================")
            print("             OFFICIAL RECEIPT             ")
            print("==========================================")
            print(f"Customer Name: {name}")
            print(f"Service:           {service} x {quantity}")
            print(f"Subtotal Service: ₱{subtotal:.2f}")
            print(f"Cash:             ₱{cash:.2f}")
            print(f"Change:           ₱{change:.2f}")
            print(f"Loyalty Tier:      {loyalty_status}")
            print(f"Discount:       - ₱{discount_amount:.2f}")
            print(f"VAT (12%):      + ₱{tax_amount:.2f}")
            print("------------------------------------------")
            print(f"TOTAL AMOUNT DUE: ₱{final_total:.2f}")

            print("==========================================")
            print("      Ride safe! Thank you for Choosing us!    ")

        else:
            print("\n==========================================")
            balance = subtotal - cash
            print("Insufficient Cash!")
            print(f"Balance: ₱{balance}")
            print("==========================================")

    elif choice2 == 3:
        service = "Break Check"
        print(f"• Break Check                                              - {break_check:.2f}")
        quantity = int(input("Enter Service Quantity: "))
        has_loyalty = input("Do you have a Dongworkszxc Loyalty Card? (yes / no): ").lower()
        subtotal = quantity * break_check

        if has_loyalty == "yes":
            if subtotal >= 1000:
                discount_rate = 0.15
                loyalty_status = "VIP Member (15% Off)"
            else:
                discount_rate = 0.10
                loyalty_status = "Normal Member (10% Off)"
        else:
            discount_rate = 0.00
            loyalty_status = "Non-Member (0% Off)"

        print(f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}")
        cash = int(input("Enter Your Cash: "))

        if cash >= subtotal:
            change = cash - subtotal
            discount_amount = subtotal * discount_rate
            discounted_subtotal = subtotal - discount_amount
            tax_amount = discounted_subtotal * tax_rate
            final_total = discounted_subtotal + tax_amount
            print("\n==========================================")
            print("             OFFICIAL RECEIPT             ")
            print("==========================================")
            print(f"Customer Name: {name}")
            print(f"Service:           {service} x {quantity}")
            print(f"Subtotal Service: ₱{subtotal:.2f}")
            print(f"Cash:             ₱{cash:.2f}")
            print(f"Change:           ₱{change:.2f}")
            print(f"Loyalty Tier:      {loyalty_status}")
            print(f"Discount:       - ₱{discount_amount:.2f}")
            print(f"VAT (12%):      + ₱{tax_amount:.2f}")
            print("------------------------------------------")
            print(f"TOTAL AMOUNT DUE: ₱{final_total:.2f}")

            print("==========================================")
            print("      Ride safe! Thank you for Choosing us!    ")

        else:
            print("\n==========================================")
            balance = subtotal - cash
            print("Insufficient Cash!")
            print(f"Balance: ₱{balance}")
            print("==========================================")

    elif choice2 == 4:
        service = "Throttle Body Cleaning"
        print(f"• Throttle Body Cleaning                                           - {throttle_body:.2f}")
        quantity = int(input("Enter Service Quantity: "))
        has_loyalty = input("Do you have a Dongworkszxc Loyalty Card? (yes / no): ").lower()
        subtotal = quantity * throttle_body
        if has_loyalty == "yes":
            if subtotal >= 1000:
                discount_rate = 0.15
                loyalty_status = "VIP Member (15% Off)"
            else:
                discount_rate = 0.10
                loyalty_status = "Normal Member (10% Off)"
        else:
            discount_rate = 0.00
            loyalty_status = "Non-Member (0% Off)"

        print(f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}")
        cash = int(input("Enter Your Cash: "))

        if cash >= subtotal:
            change = cash - subtotal
            discount_amount = subtotal * discount_rate
            discounted_subtotal = subtotal - discount_amount
            tax_amount = discounted_subtotal * tax_rate
            final_total = discounted_subtotal + tax_amount

            print("\n==========================================")
            print("             OFFICIAL RECEIPT             ")
            print("==========================================")
            print(f"Customer Name: {name}")
            print(f"Service:           {service} x {quantity}")
            print(f"Subtotal Service: ₱{subtotal:.2f}")
            print(f"Cash:             ₱{cash:.2f}")
            print(f"Change:           ₱{change:.2f}")
            print(f"Loyalty Tier:      {loyalty_status}")
            print(f"Discount:       - ₱{discount_amount:.2f}")
            print(f"VAT (12%):      + ₱{tax_amount:.2f}")
            print("------------------------------------------")
            print(f"TOTAL AMOUNT DUE: ₱{final_total:.2f}")

            print("==========================================")
            print("      Ride safe! Thank you for Choosing us!    ")

        else:
            print("\n==========================================")
            balance = subtotal - cash
            print("Insufficient Cash!")
            print(f"Balance: ₱{balance}")
            print("==========================================")

    elif choice2 == 5:

        service = "Spark Plug Check"
        print(f"• Spark Plug Check                                             - {spark_plug:.2f}")
        quantity = int(input("Enter Service Quantity: "))
        has_loyalty = input("Do you have a Dongworkszxc Loyalty Card? (yes / no): ").lower()
        subtotal = quantity * spark_plug

        if has_loyalty == "yes":
            if subtotal >= 1000:
                discount_rate = 0.15
                loyalty_status = "VIP Member (15% Off)"
            else:
                discount_rate = 0.10
                loyalty_status = "Normal Member (10% Off)"
        else:
            discount_rate = 0.00
            loyalty_status = "Non-Member (0% Off)"

        print(f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}")
        cash = int(input("Enter Your Cash: "))

        if cash >= subtotal:
            change = cash - subtotal
            discount_amount = subtotal * discount_rate
            discounted_subtotal = subtotal - discount_amount
            tax_amount = discounted_subtotal * tax_rate
            final_total = discounted_subtotal + tax_amount

            print("\n==========================================")
            print("             OFFICIAL RECEIPT             ")
            print("==========================================")
            print(f"Customer Name: {name}")
            print(f"Service:           {service} x {quantity}")
            print(f"Subtotal Service: ₱{subtotal:.2f}")
            print(f"Cash:             ₱{cash:.2f}")
            print(f"Change:           ₱{change:.2f}")
            print(f"Loyalty Tier:      {loyalty_status}")
            print(f"Discount:       - ₱{discount_amount:.2f}")
            print(f"VAT (12%):      + ₱{tax_amount:.2f}")
            print("------------------------------------------")
            print(f"TOTAL AMOUNT DUE: ₱{final_total:.2f}")

            print("==========================================")
            print("      Ride safe! Thank you for Choosing us!    ")

        else:
            print("\n==========================================")
            balance = subtotal - cash
            print("Insufficient Cash!")
            print(f"Balance: ₱{balance}")
            print("==========================================")

    elif choice2 == 6:
        service = "Air Filter Check/Replacement"
        print(f"• Air Filter Check/Replacement                                          - {air_filter:.2f}")
        quantity = int(input("Enter Service Quantity: "))
        has_loyalty = input("Do you have a Dongworkszxc Loyalty Card? (yes / no): ").lower()
        subtotal = quantity * air_filter

        if has_loyalty == "yes":
            if subtotal >= 1000:
                discount_rate = 0.15
                loyalty_status = "VIP Member (15% Off)"
            else:
                discount_rate = 0.10
                loyalty_status = "Normal Member (10% Off)"
        else:
            discount_rate = 0.00
            loyalty_status = "Non-Member (0% Off)"

        print(f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}")
        cash = int(input("Enter Your Cash: "))

        if cash >= subtotal:
            change = cash - subtotal
            discount_amount = subtotal * discount_rate
            discounted_subtotal = subtotal - discount_amount
            tax_amount = discounted_subtotal * tax_rate
            final_total = discounted_subtotal + tax_amount

            print("\n==========================================")
            print("             OFFICIAL RECEIPT             ")
            print("==========================================")
            print(f"Customer Name: {name}")
            print(f"Service:           {service} x {quantity}")
            print(f"Subtotal Service: ₱{subtotal:.2f}")
            print(f"Cash:             ₱{cash:.2f}")
            print(f"Change:           ₱{change:.2f}")
            print(f"Loyalty Tier:      {loyalty_status}")
            print(f"Discount:       - ₱{discount_amount:.2f}")
            print(f"VAT (12%):      + ₱{tax_amount:.2f}")
            print("------------------------------------------")
            print(f"TOTAL AMOUNT DUE: ₱{final_total:.2f}")

            print("==========================================")
            print("      Ride safe! Thank you for Choosing us!    ")

        else:
            print("\n==========================================")
            balance = subtotal - cash
            print("Insufficient Cash!")
            print(f"Balance: ₱{balance}")
            print("==========================================")

    elif choice2 == 7:
        service = "CVT Cleaning"
        print(f"• CVT Cleaning                                          - {cvt_cleaning:.2f}")
        quantity = int(input("Enter Service Quantity: "))
        has_loyalty = input("Do you have a Dongworkszxc Loyalty Card? (yes / no): ").lower()
        subtotal = quantity * cvt_cleaning

        if has_loyalty == "yes":
            if subtotal >= 1000:
                discount_rate = 0.15
                loyalty_status = "VIP Member (15% Off)"
            else:
                discount_rate = 0.10
                loyalty_status = "Normal Member (10% Off)"
        else:
            discount_rate = 0.00
            loyalty_status = "Non-Member (0% Off)"

        print(f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}")
        cash = int(input("Enter Your Cash: "))

        if cash >= subtotal:
            change = cash - subtotal
            discount_amount = subtotal * discount_rate
            discounted_subtotal = subtotal - discount_amount
            tax_amount = discounted_subtotal * tax_rate
            final_total = discounted_subtotal + tax_amount

            print("\n==========================================")
            print("             OFFICIAL RECEIPT             ")
            print("==========================================")
            print(f"Customer Name: {name}")
            print(f"Service:           {service} x {quantity}")
            print(f"Subtotal Service: ₱{subtotal:.2f}")
            print(f"Cash:             ₱{cash:.2f}")
            print(f"Change:           ₱{change:.2f}")
            print(f"Loyalty Tier:      {loyalty_status}")
            print(f"Discount:       - ₱{discount_amount:.2f}")
            print(f"VAT (12%):      + ₱{tax_amount:.2f}")
            print("------------------------------------------")
            print(f"TOTAL AMOUNT DUE: ₱{final_total:.2f}")

            print("==========================================")
            print("      Ride safe! Thank you for Choosing us!    ")

        else:
            print("\n==========================================")
            balance = subtotal - cash
            print("Insufficient Cash!")
            print(f"Balance: ₱{balance}")
            print("==========================================")

    elif choice2 == 8:
        service = "FI Cleaning "
        print(f"• FI Cleaning                                           - {fi_cleaning:.2f}")
        quantity = int(input("Enter Service Quantity: "))
        has_loyalty = input("Do you have a Dongworkszxc Loyalty Card? (yes / no): ").lower()
        subtotal = quantity * fi_cleaning

        if has_loyalty == "yes":
            if subtotal >= 1000:
                discount_rate = 0.15
                loyalty_status = "VIP Member (15% Off)"
            else:
                discount_rate = 0.10
                loyalty_status = "Normal Member (10% Off)"
        else:
            discount_rate = 0.00
            loyalty_status = "Non-Member (0% Off)"

        print(f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}")
        cash = int(input("Enter Your Cash: "))

        if cash >= subtotal:
            change = cash - subtotal
            discount_amount = subtotal * discount_rate
            discounted_subtotal = subtotal - discount_amount
            tax_amount = discounted_subtotal * tax_rate
            final_total = discounted_subtotal + tax_amount

            print("\n==========================================")
            print("             OFFICIAL RECEIPT             ")
            print("==========================================")
            print(f"Customer Name: {name}")
            print(f"Service:           {service} x {quantity}")
            print(f"Subtotal Service: ₱{subtotal:.2f}")
            print(f"Cash:             ₱{cash:.2f}")
            print(f"Change:           ₱{change:.2f}")
            print(f"Loyalty Tier:      {loyalty_status}")
            print(f"Discount:       - ₱{discount_amount:.2f}")
            print(f"VAT (12%):      + ₱{tax_amount:.2f}")
            print("------------------------------------------")
            print(f"TOTAL AMOUNT DUE: ₱{final_total:.2f}")

            print("==========================================")
            print("      Ride safe! Thank you for Choosing us!    ")

        else:
            print("\n==========================================")
            balance = subtotal - cash
            print("Insufficient Cash!")
            print(f"Balance: ₱{balance}")
            print("==========================================")
    else:
        print("Invalid Choice! Please choose Between (1-8) Only!")




















