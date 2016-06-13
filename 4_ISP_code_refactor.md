> refactored interfaces to be segregated:

    interface IWalkingBird {
      void Walk();
    }
    
    interface IFlyingBird {
      void Fly();
    }
    
    interface ITalkingBird {
      void Talk();
    }

> Now the birds only need to implement the interfaces they care about:

    class Dove : IWalkingBird, IFlyingBird {
      void Walk() { return "slow"; }
      void Fly() { return "low"; }
    }
    
    class Eagle : IFlyingBird {
      void Fly() { return "soar"; }
    }
    
    class Ostrich : IWalkingBird {
      void Walk() { return "fast"; }
    }
    
    class Parrot : IWalkingBird, ITalkingBird {
      void Walk() { return "caged"; }
      void Talk() { return "polly"; }
    }

[&laquo; back to readme.md](README.md)
