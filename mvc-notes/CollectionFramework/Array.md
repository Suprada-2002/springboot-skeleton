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

## Declare
```
int[] x;
```

## Initialization
- declare + initialize
```
int[] x = {1,2,3,4,5};
```

## creating
- not initializing manually so by default initialized by 0s.
```
int[] arr = new int[3]
```

## printing values
```
print(arr);
```
- arr is a reference variable that points to array
- toString() method is called and print the following:
```
[I@33909752
name of class @ hashcode in hexadecimal
```
- by default value for object creation is null
```
int[][] arr = new int[2][];
print(arr[0][]);  // null
print(arr[0][0]);  // null-pointer exception

arr[0] = new int[2];
arr[1] = new int[3];
print(arr[0][0]); //0
```

### For-each loop to print 2-d array
- Only the base level 1-D array contains elements.
- Upper level contains reference to objects.
```
 int[][] arr = {{1,2,3}, {4,5}, {6}};
      
      for(int[] array: arr){
        for(int i:array){
          System.out.println(i);
        }
      }
```
