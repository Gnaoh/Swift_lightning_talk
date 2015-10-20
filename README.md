# Swift_lightning_talk

Swift : 
Apple's newest programming language designed for creating iOS and Mac applications

Xcode:
An integrated developer environment (IDE), which is a software application that includes a source code editor, debugger and usually a compiler. Swift is built with the LLVM compiler framework included in Xcode 6.

Playground: 
Interactive Swift coding environment that evaluates each statement without needing to compile and run a project. 

###Variable Types 

Static vs. Dynamic variable 

```
let staticVariable = "This value will never change"
var dynamicVariable = "This value can change"

dynamicVariable = "I just changed the value"

```

###Data Types
Strings, Integer, Float, double 

OR

Constants and variables can contain almost any characters including Unicode characters

```
let π = 3.14159
let 你好 = "你好世界"
let 🐶🐮 = "dogcow"
```

###Collection Types

3 primary collection types

![alt tag](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Art/CollectionTypes_intro_2x.png)

**Array** - Ordered collection of values

**Set** - Unordered collection of unique values

**Dictionary** - Unordered collection of key value pairs

###Control Flow

**For Loop**

```
for var index = 0; index < 3; ++index {
    print("index is \(index)")
}
```

**For In Loop**

```
let names = ["Anna", "Alex", "Brian", "Jack"]

for name in names {
    print("Hello, \(name)!")
}
```

**While Loop**

```
while condition {
    statements
}
```

###Functions

Let's write a basic function

```
func sayHello(personName: String) -> String {
    let greeting = "Hello, " + personName + "!"
    return greeting
}
```

Now let's write a function with multiple parameters

```
func sayHello(personName: String, alreadyGreeted: Bool) -> String {
    if alreadyGreeted {
        return sayHelloAgain(personName)
    } else {
        return sayHello(personName)
    }
}
print(sayHello("Tim", alreadyGreeted: true))
// prints "Hello again, Tim!"
```

We can have a function have **multiple** return values

```
func minMax(array: [Int]) -> (min: Int, max: Int) {
    var currentMin = array[0]
    var currentMax = array[0]
    for value in array[1..<array.count] {
        if value < currentMin {
            currentMin = value
        } else if value > currentMax {
            currentMax = value
        }
    }
    return (currentMin, currentMax)
}
```






