# UML Class Diagram
```mermaid
classDiagram
    Bank --> Account
    Account <|-- SavingsAccount
    Account <|-- CheckingAccount
    class Bank {
       -String Name
       -List accounts
       + create_account(self, account_type, account_number, acccount_holder_name, balance, interest_rate = None, overdraft_limit = None):
       + delete_account(self, account_number):
       + find_account(self, account_number):
       + list_accounts(self):
   }
   class Account{
      -int account_number
      -string account_holder_name
      -float balance
      + deposit(self, amount):
      + withdraw(self, amount):
      + get_balance(self):
      + display(self):
    }
   class SavingsAccount{
      -float interest_rate
      + calculate_interest(self):
      + display(self):
    }
    class CheckingAccount{
      -float overdraft_limit
      + withdraw(self, amount):
      + display(self):
    }

