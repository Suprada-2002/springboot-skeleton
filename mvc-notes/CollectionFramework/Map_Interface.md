# Map Interface
- Part of collection framework.
- Represent object as a key-value pair.
- Keys & values are objects and can be of any data type.
- Keys can't be duplicate but value can.
- Each key-value pair is called an entry.

## Hashing
- Hash Function is a function in which when we supply an object,it generates address of that object.
- Applide to keys of HashMap.
- convert large strings to small string that represent the same things.
- Object class has 2 functions:
- Both mehtods need to be overriden.
```
hashCode() 
equals() 
```

### hashCode() function
- generates a unique code for object like a hash function.
- ***@ Objects can have same hash code***
1. Always return an integer.
2. 2 equal objects will have same number.
- After that modulo of hash code to the size of the table to get the index and stored in hash table.
> Collisons
- When same hash code is generated for 2 different objects, it is called ```collision```.
- One of way to deal with collision is to put the objects that collide in a linked list.
- in that case hash table will be an array of list.

## HashMap Class
- Underlying DS: hash table.
- Insertion Order not preserved.
- No duplicate keys.
- Key can be null only once. Values can be null more than once.
- Key & value both can be heterogenous.
-   Implements Serializable, Cloneable interface. Extends an abstract class ```Abstract Map```.
- **Best choice for search operations**, because it uses hashing to store data.
