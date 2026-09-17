ayni Pseudocode 

start 
output "-"*50
output "         Welcome to Dongworkszxc, what can we do for you?"
output "-"*50
Output [1] = Motor Services
Output [2] = Basic Maintenance
 
DECLARE choice, choice1, choice2, quantity, cash integer
DECLARE price, subtotal, discount_rate, discount_amount, discounted_subtotal, tax_rate, tax_amount, final_total, change, balance float
DECLARE service, has_loyalty, loyalty_status string

Input choice
Output Enter Your Choice of Service:

If choice == 1
Output [1] - Motor Services
Output 1. Fuel Injection - P250.00
Output 2. CVT Tuning - P350.00

fuel_injection = 250
cvt_tuning = 350
tax_rate = 0.12

Input choice1
Output Enter Your Service Choice:


	If choice1 == 1
		service = "Fuel Injection"
		output = f"• Fuel Injection                            - ₱{fuel_injection:.2f}"

		input quantity
		output Enter Service Quantity

		input has_loyalty
		output Do you have a Dongworkszxc Loyalty Card? (yes / no): 

		subtotal = quantity * fuel_	injection

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
	end if

	Output	f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}

	Input cash
	Output Enter Your Cash:

	If cash >= subtotal
	   change = cash - subtotal
	   discount_amount = subtotal * discount_rate
	   discounted_subtotal = subtotal - discount_amount
	   tax_amount = discounted_subtotal * tax_rate
	   final_total = discounted_subtotal + tax_amount
	
		Output ==================================================
		Output OFFICIAL RECEIPT
		Output ==================================================
		Output f"Service:           {service} x {quantity}"
		Output f"Subtotal Service ₱{subtotal:.2f}"
		Output f"Cash:             ₱{cash:.2f}"
		Output f"Change:           ₱{change:.2f}"
		Output f"Loyalty Tier:      {loyalty_status}"
		Output f"Discount:       - ₱{discount_amount:.2f}"
		Output f"VAT (12%):      + ₱{tax_amount:.2f}"
		Output --------------------------------------------------
		Output f"TOTAL AMOUNT DUE: P{final_total:.2f}"
		Output ==================================================
		Output Ride safe! Thank you for Choosing us!
		Output ==================================================


		else
		  Output ==================================================
		  balance = subtotal - cash
		  Output Insufficient Cash
		  Output f"Balance: ₱{balance}"
		  Output ==================================================
	end if

	elif choice 1 ==2:
		service = "CVT Tuning"
		output f"• CVT Tuning                                - {cvt_tuning:.2f}"
		
		input quantity
		output Enter Service Quantity

		input has_loyalty
		output Do you have a Dongworkszxc Loyalty Card? (yes / no): 

		subtotal = quantity * cvt_tuning
	
		
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

		
		Output	f"Your  Subtotal for your Service/s is: ₱{subtotal:.2f}

		Input cash
		Output Enter Your Cash:
	end elif
		If cash >= subtotal
	  	  change = cash - subtotal
	  	  discount_amount = subtotal * discount_rate
	  	  discounted_subtotal = subtotal - discount_amount
	  	  tax_amount = discounted_subtotal * tax_rate
	  	  final_total = discounted_subtotal + tax_amount
	
		Output ==================================================
		Output OFFICIAL RECEIPT
		Output ==================================================
		Output f"Service:           {service} x {quantity}"
		Output f"Subtotal Service ₱{subtotal:.2f}"
		Output f"Cash:             ₱{cash:.2f}"
		Output f"Change:           ₱{change:.2f}"
		Output f"Loyalty Tier:      {loyalty_status}"
		Output f"Discount:       - ₱{discount_amount:.2f}"
		Output f"VAT (12%):      + ₱{tax_amount:.2f}"
		Output --------------------------------------------------
		Output f"TOTAL AMOUNT DUE: P{final_total:.2f}"
		Output ==================================================
		Output Ride safe! Thank you for Choosing us!
		Output ==================================================


		else
		  Output ==================================================
		  balance = subtotal - cash
		  Output Insufficient Cash
		  Output f"Balance: ₱{balance}"
		  Output ==================================================
	
	else:
	    output Invalid Choice!
		end if


Elif choice == 2
	Output [2] - Basic Maintenance
	Output 1. Change Engine Oil & Oil Filter - P350.00
	Output 2. Change Gear Oil - P250.00

	engine_oil = 350
    	gear_oil = 250
   	tax_rate = 0.12

	Input choice2
	Output Enter Your Service Choice:
	
	if choice2 == 1:	
		service = Change Engine Oil & Oil Filter"
		output f"• Change Engine Oil & Oil Filter                           - ₱{eng
     end if
end if 
end	



















