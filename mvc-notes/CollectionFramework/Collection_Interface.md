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
