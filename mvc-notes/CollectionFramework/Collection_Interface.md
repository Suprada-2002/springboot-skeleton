# List Interface
- Ordered : Insertion order is preserved.
- Duplicate allowed.
- positional Access to elements 
- Object of List is not allowed, but instance can be created using its implementing classes.
```
List a = new ArrayList();
List b = new LinkedList();
List c = new Vector();
List d = new Stack();
```

## ArrayList
- Resizable array.
- underlying DS: Array.
- accepts heterogenous objects.
- New size: ```(x * 3/2) + 1```, where x = Initial array size.
- Original array is copied to New one & discarded.
```
ArrayList a = new ArrayList(Collection c);
```
1. add();
2. remove(index/Object);
3. Object get(index);
- Convert to Generic ArrayList, because using Raw type ArrayList can result in run-time exception, also there is a headache for programmers to perform type casting at runtime.
- Hence Generics make collection type safe and solve the problem of typecasting so that run-time exceptions can be avoided.
```
ArrayList<String> a = new ArrayList<String>();
```

### Serializable & Cloneable Interface
- use collection to hold & transfer a group of objects from one location to other.
- To send object across a network, it is mandatory that the object should be serializable i.e. Object should implement ```serializable interface```.
- That's why every collection class/interface by default implements/extends serializable.
- Ever Collection class implements ```Cloneable interface``` by which we can reduce duplicates or duplicate objects, so that we can operate on those objects & later compare them with the original ones if necessary.
- Also objects can recovered id something goes wrong.


### Random Access Interface
- ArrayList implements ```random access interface```.
- present in java.util package & does not contain any methods.
- It is just a marker interface which is generally used ArrayList/vector class to indicate that it support fast random access.
```
Random Access Interface
	|-- Marker Interface
```
- Hence **suitable to perform retrieval** operation frequently.
- **Not recommended for insertion/deletion in middle**, because for single addition/deletion many sifts of elements is required.

## LinkedList
- Every element is a separate object with data & address part.
- heterogenous
- null insertion is possible
```
Non-parameterized constructor
LinkedList ll = new LinkedList();

Parametrized constructor
LinkedList ll = new LinkedList(Collection c); : creates equivalent linked list for c.
```

> ArrayList vs LinkedList

| ArrayList | LinkedList |
|----|----|
|Bad for insert/delete in middle|best choice|
|best for retriving(Indexed-array)|not best because to find  positon of ele, traverse the whole list|

## Vector
- resizable/growable array.
- underlying DS: array.
- Heterogenous object allowed
- Implements Cloneable, Serializable and random access interface.
- size(): current number of elements it is holding.
- capacity(): total elements it can hold.
> All methods are synchronized i.e. Only one thread can access a method at a time. so Vector are **thread safe**.

> Performance: time threads are required to wait to operate on its methods.

- New Size: ```Current size*2```.
- Capacity can be defined:
```
Vector v = new Vector(60);

Vector v = new Vector(capacity, incrementalCapacity);
Vector v = new Vector(100, 5); //increment by 5 not double the size
Vector v = new Vector(Collection c); //get equivalent vector for c
```

|ArrayList|Vector|
|----|---|
|Methods Not Synchronized| Methods are Synchronized |
|Not Thread Safe|Thread Safe|
|Performance is high|Low performance|
|Not legacy class, came in v 1.2|Legacy class v 1|

## Stack
- Underlying DS: stack
- LIFO
```
Only one Constructor:
Stack s = new Stack();
```
- Methods:
1. push()
2. pop()
3. peek()
4. boolean isEmpty()
5. index search(Object)
