# Map Interface
- Part of collection framework.
- Represent object as a key-value pair.
- Keys & values are objects and can be of any data type.
- Keys can't be duplicate but value can.
- Each key-value pair is called an entry.

## Hashing
- Hash Function is a function in which when we supply an object,it generates address of that object.
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
