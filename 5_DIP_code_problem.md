> Example code showing tightly coupled dependancies

    class CustomerService {
      void ActivateLogin() {
        var log = new TextFileLogger();
        log.logEvent("Customer is being activated");
    
        var emailService = new MailchimpEmailService();
        emailService.SendWelcomeEmail(this);
      }
    }

The CustomerService class is now tightly coupled to the TextFileLogger and MailchimpEmailService implementation. How can we decouple this mess?

[&laquo; back to readme.md](README.md) | [view the refactored code &raquo;](5_DIP_code_refactor.md)
