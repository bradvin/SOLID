> Below is an example of a class not following SRP

    class UserService {
      void Validate(User user) { } 
      void MakePayment(User fromUser, User toUser) { } 
    }

> What changes can be made to better follow SRP ?

[&laquo; back to readme.md](README.md) | [view the refactored code &raquo;](1_SRP_code_refactor.md)
