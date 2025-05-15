# Array
- Homogenous collection of element.
- Indexed.
- part of Java language and not Collection Fraemwork.
- Table for every array type.

```
System.out.println(arr.getClass().getName());
```
| Array type | Corresponding class Name|
|----------|-----------|
| int[] | [I|
|int[][]|[[I|
| double[]|[D|
|short[]|[S|
|byte[]|[B|
|boolean[]|[Z|

## Size of Array
- We can create an array of size 0 in java.
- For int array: character, byte, short, char and int, because they can be promoted to int.
```
int[] arr = new int['a'];  // a= 97s
```
- Negative size array: runtime-exception
- No error till size of array = 2147483647
- However we may get run-time error even if the size is smaller because of not enough heap memory.
- Not enough memory to allocate this much size. ```2147483647*4``` is required to create array. 

