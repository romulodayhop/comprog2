bank = 1000

def withdrawMoney():
        global bank
        while True:
         try:
            amount = int(input("Enter ammount to withdraw: "))
            if amount > bank:
                 print("Insufficient Funds")
                 print("A. Exit Program")
                 print("B. Current Balance")
                 print("C. Re enter withdrawal amount")
                 choice = input("Enter choice: ").upper()

                 if choice == "A":
                    break
                 elif choice == "B":
                    print(f"Your current balance is: {bank}")
                    break
                 elif choice == "C":
                    continue 
                 else:
                    print("Invalid input. Try Again")
            else:
                 bank -= amount
                 print(f"Sucessfully Withrawed. Your new balance is: {bank}")
                 break

         except ValueError:
             print("Invalid Input. Please enter number only!")
             continue 
         finally:
                print("Process Done!")

        return
                
withdrawMoney()
