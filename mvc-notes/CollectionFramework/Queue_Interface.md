# Queue Interface
- introduced in java v 1.5.
- represent group of objects that are about to be processed.
- FIFO, and both ends are open : with one for insertion and other for deletion.
- methods:
1. boolean add(): add element at tail
2. boolean offer(): tail
3. E remove(): remove and return the head, if empty returns NoSuchElementException.
4. poll(): remove and return the head, if empty return null.
5. element(): view head without removing, if empty return exception.
6. peek(): view head without removing, if empty return null.


## LinkedList Class
- Introduced in java v 1.5.
- Queue has a child interface called dequeue & LinkedList directly implements that interface.
- 

## PriorityQueue Class
- Represent group of objects that are about to be processed according to some priority.
- No duplicates
- Insertion order is not preserved.
- If the Default Natural sorting order is used, heterogeneous element is not allowed.
- Null insertion not allowed.
- Default size: 11.
```
PriorityQueue pq = new PriorityQueue();
PriorityQueue pq = new PriorityQueue(capacity);
PriorityQueue pq = new PriorityQueue(capacity, Comparator c);
PriorityQueue pq = new PriorityQueue(SortedSet s);
PriorityQueue pq = new PriorityQueue(Collection c);
```

## BlockingQueue class

### Priority Blocking Queue

### Linked Blocking Queue





