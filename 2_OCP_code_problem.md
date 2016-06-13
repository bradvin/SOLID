> Below is an example class not following the OCP

    class Customer {
      int CustomerType = 0;
  
      int GetDiscount() {
        if (this.PlayerType == 1) {
          return 50;
        } else {
          return 10;
        }
      }
    }

> What happens when I need to cater for a new CustomerType in the future?
> If I find myself needing to change class implementation, then I am doing it wrong.
> What changes can be made to better follow the OCP ?

[&laquo; back to readme.md](README.md) | [view the refactored code &raquo;](2_OCP_code_refactor.md)
