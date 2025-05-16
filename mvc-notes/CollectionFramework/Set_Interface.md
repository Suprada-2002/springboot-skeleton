# Set Interface
- No Duplicates.
- Insertion Order is not preserved.
- Accept heterogenous objects.
- No indexing

## HashSet
- Unserlying DS: Hash Table.
- can add null value.
- Implements Serializable and Cloenable Interface.
- suitable if **seraching is the frequent** operation, becuase elements are inserted in form of has code,so searching becomes very easy.
- Hashing is the fastest ever algorithm for search.
- Initial capacity: **16.**
- New size : current **size * 2**.
- 4 constrcuctors:
```
HashSet hs = new HashSet();
HashSet hs = new HashSet(capacity); 
HashSet hs = new HashSet(capacity, loadfactor);  // 100, .80f
HashSet hs = new HashSet(Collection c); // equivalent HashSet of c.
```
> Load factor: represents at what level the hash map capacity should be changed.

> Default load factor: 0.75 or 75%. Hence after 75%is filled, it doubles the size.

### HashTable
- For every passed objects,it generates a hash code.
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
- Duplicates not allowded.
- Homogenous Elements allowded.
- Insertion is done according to some sorting order.
```
SortedSet ss = new TreeSet();
```
- 7 Methods in Sorted Set Interface:
1. Object first() : first element of treeset/sortedset.
2. Object last() : last element
3. SortedSet headSet(Object o) : all values coming before o.
4. SortedSet tailSet(Object o) : all values coming after o,including o.
5. SortedSet subSet(Object a, Object b) : all values between a & b, inlcuding a.
6. Comparator comparator() : order of sorted set. Natural sorting null is null.

### NavigableSet Interface
- child interface of Sorted Set.
- Contains methods related to Navigation functionality.
- used to report the closest matches for a given search target/element.
```
NavigableSet<> ns = new TreeSet();
```
- Methods of naviagbleSet Interface:
1. ns.floor(Objec c) : Greatest element that is less than or equal to c, null is no such element.
2. ns.lower(Object c) : Greatest element that is less than c, null is no such element.
3. ns.celling(Object c) : Least element that is greater than or equal to c, null is no such element.
4. ns.higher(Object c) : Least element that is greater than c, null if no such element.
5. ns.pollFirst() : retrieve & remove the first least element or return null if no such element.
6. ns.pollLast() :  retrieve & remove the first highest element or return null if no such element.
7. desecdingSet() : return set in descending order.
