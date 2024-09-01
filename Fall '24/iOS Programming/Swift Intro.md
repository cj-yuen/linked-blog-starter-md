```Swift
print("Hello, world")

let name: String = "Anthony" // immutable
var section = 202 // mutable
	// assigned type int (cannot change)
var sectionDouble: Double = 202 
section = 201
```

- [[Type Inference]] 

```Swift
"This is a string!"

let name = "Jordan"
"Hello, " + name + "!" // "Hello, Jordan!"
"Hello, \(name)!" // interpolation (same as above)
```


## Arrays
```Swift
let foods = ["apple", "banna", "cherry"]

let emptyFood: [String] = []
```
- empty array need type explicitly written


## Dictionary
```Swift
let violations = [
	"1920 Commons": 36,
	"Hill House": 21
]

violations["1920 Commons"] // 36
violations["as;ldskf"] // nil

// empty dictionary (String to Int)
let violations: [String: Int] = [:]

// update dictionaries
violations["1920 Commons"] = 10000
```


## Control Flow
### If
```Swift
let quantity = 1

if quantity > 0 {
	print("1")
} else {
	print("2")
}

switch quantity {
case "CIS 1600":
	print("Oh no")
case "CIS 1210":
	print("Hello help")
default:
	print("Course not found")
}
```

### For loops
```Swift
for i in 0..<5 {
	print(i)
}

let names = ["John", "Bob"]
for name in names {
	print("Hello, \(name)!")
}
```


## Optionals
```Swift
type 'a option = 
	| None // nil
	| Some of 'a  // concrete value 
```

```Swift
var name: String? = nil // optional
var name: String = "John"

name! + "Smith" // "John Smith"
name?.uppercased() // "JOHN"

if let actualName = name {
	print(actualName)
}
```

