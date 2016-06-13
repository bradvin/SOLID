> see the example classes below

    class Bird {
      void Fly() { return "fly"; }
    }
    class Dove : Bird {
      void Fly() { return "flap"; }
    }    
    class Eagle : Bird {
      void Fly() { return "soar"; }
    }
    class Ostrich : Bird {
      void Fly() { throw exception("can't fly"); }
    }

> Now what happens when you run the following:

    this.birds = new List<Bird>();
    
    this.birds.Add(new Eagle());
    this.birds.Add(new Dove());
    this.birds.Add(new Ostrich());

    foreach(var bird in this.birds) {
      bird.Fly();
    }
    
> What happens when the Ostrich tried to fly?

[&laquo; back to readme.md](README.md) | [view the refactored code &raquo;](3_LSP_code_refactor.md)
