# My-Project
class Bank1:
    accno=0     #to store aacount number
    name=""     #name of the accountan
    balance=0   #balance of the accountan
    #function to open an account
    def openAccount(self):
        print("Enter Account number:")
        self.accno=int(input())   #user account number
        print("Enter name:")
        self.name=input()
        print("Enter minimum balance")
        self.balance=float(input())
        
    def showAccount(self):
        print("User account details Vichu Bank of India")
        print("User Account Number:",self.accno)
        print("User Name:",self.name)
        print("Minimum Balance:",self.balance)
        
    def deposit(self):
        amt=0
        print("Enter the Amount to be Deposited")
        amt=float(input())
        self.balance+=amt
        print("Balance After Deposit:",self.balance)
    def withdraw(self):
        amt=0
        print("Enter the Amount to withdraw:")
        amt=float(input())
        if self.balance>=amt:
            self.balance-=amt
        else:
            print("Insufficiengt Balance")
        print("Balance After Withdraw:",self.balance)
        
        
        
class execute:
    b1=Bank1()
    print("^^^^^^^^^^^^^^")   #Decoration part
    print("^^^WELCOME^^^")
    print("^^^^^^^^^^^^^^^^")
    while True:     #loop for continuos process
        print("Press any key")
        print("1.Initail\n2.ShowAccount\n3.Deposit\n4.Withdraw\n5.exit")
        print("Enter your choice")
        option=int(input())#12345
        match option:
            case 1:
                print("Welcome for initial setup")
                b1.openAccount()
            case 2:
                b1.showAccount()
            case 3:
                b1.deposit()
            case 4:
                b1.withdraw()
            case 5:
                print("Existing transactions")
                break;
    """b1=Bank1()
    b1.openAccount()
    b1.showAccount()
    b1.deposit()
    b1.withdraw()"""

