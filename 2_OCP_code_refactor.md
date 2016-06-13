> refactor Customer class to follow the OCP

    class Customer {
      int GetDiscount { return 10; }
    }
    class GoldCustomer : Customer {
      int GetDiscount { return 50; }
    }

> Then in future when we need to cater for a new CustomerType, we simply add a new CustomerTYPE class. All existing code remains unchanged. All existing tests continue to pass.

[&laquo; back to readme.md](README.md)
