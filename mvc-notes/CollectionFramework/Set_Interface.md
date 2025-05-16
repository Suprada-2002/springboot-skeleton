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
