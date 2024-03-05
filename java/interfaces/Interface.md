# Interface

- we don not have to declare the interface type abstract, because this modifier is implicitly declared, for all interfaces
-  all members on an interface are implicitly public
- the three declarations shown are same

```java
interface FlightEnabled {  
    public abstract void takeOff();  
    
    abstract void land();  
    
    void fly();  
}

```


### Declaring an interface

- An interface is usually named, according to the set of behaviors it describes.

```java
public interface FlightEnabled {}
```