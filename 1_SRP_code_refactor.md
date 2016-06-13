> refactored UserService to better follow SRP */

    class ValidationUserService {
      void Validate(User user) { }
    }
    
    class BankingUserService {
      void MakePayment(User fromUser, User toUser) { }
    }

> each class now has a single responsibility */

> when we want to change the payment logic for a user, we only change the BankingUserService */
