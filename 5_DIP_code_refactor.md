> refactor dependencies out into general interfaces

    interface ILogger {
        void LogEvent(string event);
    }
    interface IMailService {
        void SendWelcomeEmail(Customer customer);
    }

> Then create specific concreate implementations that can be tested:

    class TextFileLogger : ILogger {
      void LogEvent(string event) {
        /* write to a file on disk */
      }
    }
    
    class MailchimpEmailService : IMailService {
      void SendWelcomeEmail(Customer customer) {
        /* connect to Mailchimp API and send email to customer.email */
      }
    }

> The customer class should not rely on the concrete implementations, but rather the interfaces:

    class CustomerService {
      private ILogger _logger;
      private IMailService _mailer;
      public CustomerService(ILogger logger, IMailService mailService) {
        this._logger = logger;
        this._mailer = mailService;
      }

      void ActivateLogin(Customer customer) {
        this._logger.logEvent("Customer " + customer.name + " is being activated");
        this._mailer.SendWelcomeEmail(customer);
      }
    }

> We can now easliy swap out the dependencies for different implementations with no changes to the CustomerService

[&laquo; back to readme.md](README.md)
