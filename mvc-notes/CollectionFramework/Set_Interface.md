# Set Interface
- No Duplicates.
- Insertion Order is not preserved.
- Accept heterogeneous objects.
- No indexing

## HashSet
- Unserlying DS: Hash Table.
- can add null value.
- Implements Serializable and Cloenable Interface.
- suitable if **seraching is the frequent** operation, because elements are inserted in form of has code,so searching becomes very easy.
- Hashing is the fastest ever algorithm for search.
- Initial capacity: **16.**
- New size : current **size * 2**.
- 4 constructors:
```
HashSet hs = new HashSet();
HashSet hs = new HashSet(capacity); 
HashSet hs = new HashSet(capacity, loadfactor);  // 100, .80f
HashSet hs = new HashSet(Collection c); // equivalent HashSet of c.
```
> Load factor: represents at what level the hash map capacity should be changed.

> Default load factor: 0.75 or 75%. Hence after 75% is filled, it doubles the size.

### HashTable
- For every passed objects, it generates a hash code.
- For index it performs mod operation of generated hash code with table size.

### LinkedHashSet
- Child class of HashSet.
- Underlying DS: combination of LinedList and Has Table.
- Insertion Order is Preserved.
- introduced in v 1.4.
- Initial Capacity: 16.
```
LinkedHashSet hs = new LinkedHashSet();
LinkedHashSet hs = new LinkedHashSet(capacity);
LinkedHashSet hs = new LinkedHashSet(capacity, loadFactor);  // 20, 1.00f
```

## SortedSet Interface
- Introduced in v 1.2.
- Insertion Order not preserved.
- Duplicates not allowed.
- Homogeneous Elements allowed.
- Insertion is done according to some sorting order.
```
SortedSet ss = new TreeSet();
```
- 7 Methods in Sorted Set Interface:
1. Object first() : first element of treeset/sortedset.
2. Object last() : last element
3. SortedSet headSet(Object o) : all values coming before o.
4. SortedSet tailSet(Object o) : all values coming after o, including o.
5. SortedSet subSet(Object a, Object b) : all values between a & b, inlcuding a.
6. Comparator comparator() : order of sorted set. Natural sorting null is null.

### NavigableSet Interface
- child interface of Sorted Set.
- Contains methods related to Navigation functionality.
- Used to report the closest matches for a given search target/element.
```
NavigableSet<> ns = new TreeSet();
```
- Methods of navigableSet Interface:
1. ns.floor(Objec c) : Greatest element that is less than or equal to c, null is no such element.
2. ns.lower(Object c) : Greatest element that is less than c, null is no such element.
3. ns.celling(Object c) : Least element that is greater than or equal to c, null is no such element.
4. ns.higher(Object c) : Least element that is greater than c, null if no such element.
5. ns.pollFirst() : retrieve & remove the first least element or return null if no such element.
6. ns.pollLast() :  retrieve & remove the first highest element or return null if no such element.
7. desecdingSet() : return set in descending order.

### TreeSet Class
- Implementing Class for SortedSet & NavigableSet Interface.
- Homogenous Elements so that elements are comparable, otherwise classCast exception at runtime.
- Null value only when treeSet is empty (Only Once), else null-pointer exception.
- Implementation is based on a balanced tree, where duplicates are not allowed & Order is not preserved.
- Insertion is done according to some sorting order.
```
          root
          / \
  ele<less  ele>root
 ```
- Constructors:
```
TreeSet ts = new TreeSet();  // default sorting order
TreeSet ts = new TreeSet(Comparator obj);  // custom sorting order
TreeSet ts = new TreeSet(SortedSet s); 
TreeSet ts = new TreeSet(Collection c);
```
- *better to go with generic syntax* to keep elements homogenous.
- **Implements Comparable Interface**.
```
public class Employee implements Comparable {
    //code
    public int compareTO(Object o){}
}

TreeSet<Employee> ts = new TreeSet<Employee>();
```

## Comparable Interface
- present in ```java.lang package```.
- Contains only one method: ``` public int compareTo(Object obj)```.
- Meant for Default Natural sorting order.
- by default JVM uses it.
```
compareTo() return an integer value
+1: right
-1: left
0: equal
```

## Comparator Interface
- Present in ```java.util package```.
- used for customized sorting order or Insert in Descending Order.
- Contains 2 methods:
```
public int compare (Object obj1, Object obj2);
public boolean equals (Object obj);
```
> Compare()

- Implementation is must in order to define customized sorting order.

> equals()

- Implementation is not required.
- As Object is super/parent class for every java class & this equals method is already present in that.
```
Example: for descending order:
public class MySorting implement Comparator{

  @Override
  public int compare(Object o1, Object o2){
    Integer d1 = (Inetegr)o1;
    Integer d2 = (Inetegr)o2;
    if(d1<d2) return +1;
    elseif(d1>d2) return -1;
    else 0;
  }
}

public class MyClass{
  public static void main(String[] args){
    TreeSet st = new TreeSet(new MySorting());
    st.add();

    print(st);
  }
}
```
