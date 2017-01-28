---
layout: feature
name: 'Array'
iid: Array
status: DONE
language: swift,objectivec
abstract: "Create arrays and dictionaries using brackets ([]), and access their elements by writing the index or key in brackets."
links:
 - link:
    name: 'Swift API Reference: Generic Structure, Array'
    url: https://developer.apple.com/reference/swift/array
    description: ' - Apple Developer'
    type: reference
 - link:
    name: 'The Swift Programming Language: A Swift Tour'
    url: https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-ID1
    description: ' - Apple Developer'
    type: reference
features:
 - Variable
 - Range
---

# Swift

Create arrays and dictionaries using brackets (`[]`), and access their elements by writing the index or key in brackets.

<pre><code>var shoppingList = ["catfish", "water", "tulips", "blue paint"]
shoppingList[1] = "bottle of water"
 
var occupations = [
    "Malcolm": "Captain",
    "Kaylee": "Mechanic",
]
occupations["Jayne"] = "Public Relations"
</code></pre>

To create an empty array or dictionary, use the initializer syntax.

<pre><code>let emptyArray = [String]()
let emptyDictionary = [String: Float]()
</code></pre>

If type information can be inferred, you can write an empty array as [] and an empty dictionary as [:]—for example, when you set a new value for a variable or pass an argument to a function.

<pre><code>shoppingList = []
occupations = [:]
</code></pre>

## Range

It is possible to access items of an array with [Range](/Range) operator:

```
var accounts = ['11', '22', '33']
accounts[3...5] = ['44', '55', '66']
print(accounts)                     // Prints ['11', '22', '33', '44', '55', '66']
```



# Objective-C

Defining:

```
double balance[10];
```

Initializing:

```
double balance[5] = {1000.0, 2.0, 3.4, 17.0, 50.0};
double balance[] = {1000.0, 2.0, 3.4, 17.0, 50.0};
```

Setting a value:

```
balance[4] = 50.0;
```

Accessing a value:

```
double salary = balance[9];
```

Summary code:

```
   int n[ 10 ]; /* n is an array of 10 integers */
   int i, j;
 
   /* initialize elements of array n to 0 */         
   for ( i = 0; i < 10; i++ ) {
      n[ i ] = i + 100; /* set element at location i to i + 100 */
   }
   
   /* output each array element's value */
   for (j = 0; j < 10; j++ ) {
      NSLog(@"Element[%d] = %d\n", j, n[j] );
   }
 
```

## Multi-dimensional arrays

Defining:

```
int threedim[5][10][4];
```

Initializing:

```
int a[3][4] = {  
 {0, 1, 2, 3} ,   /*  initializers for row indexed by 0 */
 {4, 5, 6, 7} ,   /*  initializers for row indexed by 1 */
 {8, 9, 10, 11}   /*  initializers for row indexed by 2 */
};
```

Setting a value:

```
int a[3][4] = {0,1,2,3,4,5,6,7,8,9,10,11};
```

Accessing a value:

```
int val = a[2][3];
```

Summary code

```
   /* an array with 5 rows and 2 columns*/
   int a[5][2] = { {0,0}, {1,2}, {2,4}, {3,6},{4,8}};
   int i, j;
 
   /* output each array element's value */
   for ( i = 0; i < 5; i++ ) {
      for ( j = 0; j < 2; j++ ) {
         NSLog(@"a[%d][%d] = %d\n", i,j, a[i][j] );
      }
   }
```