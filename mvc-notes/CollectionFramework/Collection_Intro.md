# Collection Framework
- Growable in nature : no worry about size.
- can hold both heterogenous and homogenous objects.
- implemented based on standard DS : ready-made methods are available to use as per requirement.

|Array|Collection|
|-----|-----|
|Memory point of view,its waste of space|use to stop memory wastage|
|no underlying DS|In-built Ds and algorithm (for searching,sorting)|
|can hold primitive type & object type both | can only hold object types|

## 2 Dominant Interface
- use to represent a group of discrete object as a single data unit.
- 9 dominant interface
## 1. Collection Interface
```
|-- list interface : insertion order is preserved, duplicated allowed
    |--- arraylist class
    |--- linkedlist class
    |--- vector class
        |--- Stack class
|-- Set Interface : insertion order is not preserved, duplicate not allowed
    |--- HashSet class
    |--- SortedSet Interface
        |--- Navigable Set
            |--- TreeSet Class
|-- Queue Interface
    |--- Priority Queue Class
    |--- Blocking Queue Class
        |--- Priority Blocking Queue
        |--- Linked Blocking Queue
```

> Vector & Stack are legacy classes. They were already available from java v1. and later added to collection.

## 2. Map Interface
- represent value as key-value pair.
a. HashMap class
- Linked HashMap
b. WeakHashMap class
c.IdentityHashMap class
d. HashTable class
- Properties class
- extends an Abstract class: Dictionary
e. Sorted Map Interface
- child Interface: Navigable Map -> TreeMap class
