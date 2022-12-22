import time as t

pin = 4256
balance = 100000

print("Welcome to ATM Dear User...", end = "\n\n")

ch = 9

while (True):
    print("\t\t0. Logout")
    print("\t\t1. Display Account Balance")
    print("\t\t2. Cash Withdrawal")
    print("\t\t3. Cash Deposit")
    print("\t\t4. Change PIN")
    print("\t\t5. Return Card")
    ch = int(input("Enter number of choice > "))
    print("\n\n")

    if ch == 0:
        print("Exiting...")
        t.sleep(2)
        print("Logout Successful.... Thank you!\n\n")
        break

    elif ch in (1,2,3,4,5):
        tries = 3
        while (tries!=0):
            inp = int(input("Please enter 4-digit PIN > "))

            if inp == pin:
                print("Login successful!\n\n")

                if ch == 1:
                    print("Loading Account Balance...")
                    t.sleep(1.5)
                    print("Your current balance is Rs.", balance, end = "\n\n\n")
                    break
                elif ch == 2:
                    print("Opening Cash Withdrawal...")
                    t.sleep(1.5)

                    while(True):
                        withdrawal = float(input("Enter the amount to withdraw > "))

                        if withdrawal>balance:
                            print("Can't withdraw Rs.", withdrawal)
                            print("Please enter a lower amount!")
                            continue

                        else:
                            print("Withdrawing Rs.", withdrawal)
                            confirm = input("Confirm? Y/N > ")
                            if confirm in ('Y', 'y'):
                                balance-=withdrawal
                                print("Amount withdrawn - Rs.", withdrawal)
                                print("Remaining balance - Rs.",balance, end = "\n\n\n")
                                break

                            else:
                                print("Cancelling transaction...")
                                t.sleep(1)
                                print("Transaction Cancelled!\n\n")
                                break

                    break

                elif ch == 3:
                    print("Loading Cash Deposit...")
                    t.sleep(1.5)

                    deposit = int(input("Enter the amount you wish to deposit > "))
                    print("Depositing Rs.", deposit)
                    confirm = input("Confirm? Y/N > ")
                    if confirm in ('Y', 'y'):
                        balance+=deposit
                        print("Amount deposited - Rs.", deposit)
                        print("Updated balance - Rs.",balance, end = "\n\n\n")
                    else:
                        print("Cancelling transaction...")
                        t.sleep(1)
                        print("Transaction Cancelled!\n\n")

                    break


                elif ch == 4:
                    print("Loading PIN Change...")
                    t.sleep(1.5)

                    newpin = int(input("Enter your new PIN > "))

                    print("Changing PIN to", newpin)
                    confirm = input("Confirm? Y/N > ")
                    if confirm in ('Y', 'y'):
                        pin = newpin
                        print("PIN changed successfully! \n\n")
                    else:
                        print("Cancelling PIN change...")
                        t.sleep(1)
                        print("Process Cancelled!\n\n")

                    break

                else:
                    print("Loading Card Return...")
                    t.sleep(1.5)

                    print("Returning your ATM Card")
                    confirm = input("Confirm? Y/N > ")
                    if confirm in ('Y', 'y'):
                        print("Card returned successfully! \n\n")
                    else:
                        print("Cancelling process...")
                        t.sleep(1)
                        print("Process Cancelled!\n\n")

                    break

            else:
                tries-=1
                print("PIN incorrect! Number of tries left -", tries, end = "\n\n")

        else:
            print("Exiting...")
            t.sleep(2)
            print("You have been logged out. Thank you!\n\n")
            break


    else:
        print("Invalid input!")
        print("\t\t0. Enter 0 to Logout and Exit!")
        continue
