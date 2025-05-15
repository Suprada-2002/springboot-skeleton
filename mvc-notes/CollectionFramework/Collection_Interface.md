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
