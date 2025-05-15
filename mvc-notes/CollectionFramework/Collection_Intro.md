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

## Methods
- No direct implementation/no concrete class that provide implementation of Collection Framework.
- Methods present can be used in any type classes because they are present in Collection Interface.
1. boolean add(Object o)
- adds object to the invoking collection.
- ex: In case of Set, if object is already there, it will return false as duplicate is not allowed.
2. boolean addAll(Collection c)
- adds collection to the invoking collection.
- adding one list to another.
3. boolean remove(Object o)
4. boolean removeAll(Collection c)
5. boolean retainAll(Collection c)
- remove all elements from invoking element except element present in Collection c.
6. boolean contains(Object o)
- return true if object is present in invoking collection.
7. Iterator iterator()
- provides cursor to get objects of collection one by one.
8. Object[] toArray()
- converts invoking Collection to Array.

> Collection vs Collections
- Collection is a base interface for List, Set, Queue, whereas Collections is a Utility class/support tool which contains variety of useful methods that work with Collection.
- contains predefined static methods that can be used while working with Collection.
- ex: sort(), reverse(), shuffle(), disjoint(), binarySearch()
