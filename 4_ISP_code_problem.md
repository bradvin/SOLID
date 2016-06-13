> the below example shows a Bird interface that does a lot:

    interface IBird {
      void Walk();
      void Fly();
      void Talk();
    }

> Now every bird that we implement, will need to be able to do all of these things.

    class Dove {
      void Walk() { return "slow"; }
      void Fly() { return "low"; }
      void Talk() { return ""; }
    }
    
    class Eagle {
      void Walk() { return ""; }
      void Fly() { return "soar"; }
      void Talk() { return ""; }
    }
    
    class Ostrich {
      void Walk() { return "fast"; }
      void Fly() { return ""; }
      void Talk() { return ""; }
    }
    
    class Parrot {
      void Walk() { return ""; }
      void Fly() { return ""; }
      void Talk() { return "polly"; }
    }    

> We are "forcing" all future birds to do all these things. Should we force this?

[&laquo; back to readme.md](README.md) | [view the refactored code &raquo;](4_ISP_code_refactor.md)
