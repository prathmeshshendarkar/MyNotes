1. Every function or arrays or objects or strings in javascript has prototype object as a property. These object has all features such as reverse, slice, etc
2. Prototype property of javascript lets you use common methods or parameters that should be accessible to all other instance of that data type.
3. For ex: If we create array and we want every other array to have a common method that they can execute, now instead of creating constructor function or some other method, what if there was a way.
4. We can use prototype feature of javascript to have a common method. For all the arrays that we will create.

## Prototype Inheritance using class
![[Pasted image 20240715004625.png]]

![[Pasted image 20240715010130.png]]

Below is the code for above prototype inheritance.
```
// Prototype inheritance with class
// Since we got it covered why do we require Prototype inheritance
class Vehicle {
    constructor(vehicleName){
      this.vehicleName = vehicleName;
    }
    
    hornokplease(){
      console.log("Yeah Horn Horn");
    }
  }
  
  class Bus extends Vehicle {
    constructor(busName){
      super('Bus');
      this.busName = busName;
    }
    
    busNumber(nums){
      console.log(`Alright so your bus number is ${nums}`);
    }
  }
  
  const busVehicle = new Bus('Runwal Bus');
  console.log(busVehicle.busName);
  busVehicle.busNumber('MH 123');
  
  // Below is prototype chaining
  busVehicle.hornokplease();
  console.log("Break Line");
  
  const randomVehicle = new Vehicle('random Vehicle');
  randomVehicle.busNumber('XD 123');
```

