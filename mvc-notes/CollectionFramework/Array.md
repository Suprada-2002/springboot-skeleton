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

for(int i=arr.length;i++){
  for(int j=0;j<arr[i].length;j++){
     print(arr[i][j]);
   }
}
```
## Type of Array based in elements it holds/Array Element Assignments
1. Primitive
- can hold any primitive type that can be declared to declare type.
- Boolean, byte, char, short, int, float
```
int[] arr = new int[2];
arr[0]='a'; //97
float[] = new float[2];
```
2. Objects
- Pure object can hold either the declare type or child class type/sub type.
```
Object[] obj = new Object[5];
obj[0] = new Object();
obj[1] = new String();
```
3. Abstract class type Array
- object cannot be created for Abstract class.
- cannot hold the declare type itself(Number object).
- can only hold child or sub-class object.
- 6 child: byte,short,int,long,float,double.
```
Number[] num = new Number[3];
num[0] = new Integer(1);
num[1] = new Byte("2");
```
4.Interface type Array
- object cannot be created.
- hold object of class that implement this interface.
```
Runnable[] r = new Runnable[5];
r[0] = new Thread();
print(r[0]);  // thread object
print(r[1]); //null
```

### Assigning Array Object to Array references
- parent type can hold child type classes references
```
String[] str = new String[5];
Object[] obj = str;
```
- Below will give error because there is no relation between the classes.
- short element can be promoted to int.
- short array object type cannot be promoted to int object type.
```
short[] sh = new short[];  // [S
int[] arr = sh;   // [I
```
