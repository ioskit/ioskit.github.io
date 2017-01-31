---
layout: feature
name: 'Structure'
iid: Structure
status: DONE
language: swift,objectivec
abstract: "Structures support many of the same behaviors as classes, including methods and initializers. 
One of the most important differences between structures and classes is that structures are always copied 
when they are passed around in your code, but classes are passed by reference."
links:
 - link:
    name: 'The Swift Programming Language (Swift 3.0.1): A Swift Tour, Enumerations and Structures'
    url: https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-ID465
    description: ' - Apple Developer'
    type: reference
 - link:
    name: 'The Swift Programming Language (Swift 3.0.1): Language Guide, Classes and Structures'
    url: https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/ClassesAndStructures.html#//apple_ref/doc/uid/TP40014097-CH13-ID82
    description: ' - Apple Developer'
    type: reference
features:
 - Class
 - Enumeration
 - Subscripts
 - Properties
---

See [Class](/Class) page for a Comparison between Class and Structure.

Use `struct` to create a structure. Structures support many of the same behaviors as classes, including methods and initializers. 
One of the most important differences between structures and [Classes](/Class) is that **<u>structures are always copied</u>** 
when they are passed around in your code, but classes are passed by reference.

# Swift

```
struct Card {
    var rank: Rank
    var suit: Suit
    func simpleDescription() -> String {
        return "The \(rank.simpleDescription()) of \(suit.simpleDescription())"
    }
}
let threeOfSpades = Card(rank: .three, suit: .spades)
let threeOfSpadesDescription = threeOfSpades.simpleDescription()
```

### Memberwise Initializers for Structure Types

Unlike classes, all structures have an automatically-generated memberwise initializer, which you can use to initialize the member properties 
of new structure instances. Initial values for the properties of the new instance can be passed to the memberwise initializer by name:

```
let vga = Resolution(width: 640, height: 480)
```

### Structures and Enumerations Are Value Types
   
A value type is a type whose value is copied when it is assigned to a variable or constant, or when it is passed to a function.
   
All structures and enumerations are value types in Swift. This means that any structure and enumeration instances you create—and any value types they have as properties—are always copied when they are passed around in your code.

Consider this example, which uses the Resolution structure from the previous example:

```
let hd = Resolution(width: 1920, height: 1080)
var cinema = hd
cinema.width = 2048
print("cinema is now \(cinema.width) pixels wide")         // Prints "cinema is now 2048 pixels wide"
print("hd is still \(hd.width) pixels wide")               // Prints "hd is still 1920 pixels wide"

```


# Objective-C

The __structure tag__ is optional and each member definition is a normal variable definition, such as int i; or float f; 
or any other valid variable definition. At the end of the structure's definition, before the final semicolon, 
you can specify one or more __structure variables__ but it is optional.

```
struct Books /* structure tag */
{
   NSString *title;
   NSString *author;
   int   book_id;
} /* book */ /* structure variables */;
 
int main( )
{
   struct Books Book1;        /* Declare Book1 of type Book */
 
   /* book 1 specification */
   Book1.title = @"Objective-C Programming";
   Book1.author = @"Nuha Ali"; 
   Book1.subject = @"Objective-C Programming Tutorial";
   Book1.book_id = 6495407;

   /* print Book1 info */
   NSLog(@"Book 1 title : %@\n", Book1.title);
   NSLog(@"Book 1 author : %@\n", Book1.author);
   NSLog(@"Book 1 subject : %@\n", Book1.subject);
   NSLog(@"Book 1 book_id : %d\n", Book1.book_id);

   return 0;
}
```