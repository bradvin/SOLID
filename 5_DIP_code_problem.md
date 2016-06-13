> Example code showing tightly coupled dependancies

    class CustomerService {
      void ActivateLogin(Customer customer) {
        var log = new TextFileLogger();
        log.logEvent("Customer " + customer.name + " is being activated");
    
        var emailService = new MailchimpEmailService();
        emailService.SendWelcomeEmail(customer);
      }
    }

The CustomerService class is now tightly coupled to the TextFileLogger and MailchimpEmailService implementation. Why is this not ideal? What if we decide to change to another logger? Or we stop using Mailchimp for sending mails down the line? We will have to make code changes. How can we decouple this mess?

[&laquo; back to readme.md](README.md) | [view the refactored code &raquo;](5_DIP_code_refactor.md)
