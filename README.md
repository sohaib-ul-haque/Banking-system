# Banking-system
class customer:
    def __init__(self, name, account_balance):    # ye humne use kiya hae constructor
        self.name = name
        self.account_balance = account_balance
    
    def deposit(self, ammount):    # ye function humne humne acc mein deposit k liye
        if ammount > 0:
            self.account_balance += ammount
            print(f"the {ammount} successfully deposited, your new ammount in this  account is {self.account_balance} ")
        else:
            print("the ammount should bigger than zero")
            
    def withdraw (self, ammount):   # ye humne ammount ko withdraw krne k liye function ko call krwaya hae
        if ammount > 0:
            self.account_balance -= ammount
            print(f"the ammount witdrawl {ammount} has successfully has been done, your balance is now ")
        else:
            print("insufficiant ammount")
        
    
    def remaining_ammount(self):   # ye function hum acc mein kitna ballance rehgya hae woh check krne k liye call karrahe
       
        print(f"current balance: {self.account_balance}")
        return self.account_balance
        
a = customer("sohaib", 5800)
a.deposit(1000)
a.withdraw(3000)
a.remaining_ammount()
a.withdraw(50000)
