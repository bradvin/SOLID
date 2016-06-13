> Based on the problem with Ostriches trying to fly, we should consider removing Fly from our base Bird class

    class Bird { }
    
    class FlyingBird {
      void Fly() { return "fly"; }
    }
    
    class Dove : FlyingBird {
      void Fly() { return "flap"; }
    }
    class Eagle : FlyingBird {
      void Fly() { return "soar"; }
    }
    class Ostrich : Bird { }

> Now we can make all flying birds, fly:

    this.flyingBirds = new List<FlyingBird>();
    this.flyingBirds.Add(new Dove());
    this.flyingBirds.Add(new Eagle());
    
    foreach(var flyingBird in this.flyingBirds) {
      flyingBird.Fly(); //success!
    }

[&laquo; back to readme.md](README.md)
