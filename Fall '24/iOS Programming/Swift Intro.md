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
```