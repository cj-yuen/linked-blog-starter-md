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
var name: String = "John"`

name! + "Smith" // "John Smith"
name?.uppercased() // "JOHN"

if let actualName = name {
	print(actualName)
}
```

### Forced Unwraping
```Swift
let prices: [String: Int]? = nil

if prices != nil {
	// Forced Unwrapping
	prices!["Sushi"] 
} else {
	print("Prices not available")
}
```

### Optional Binding
```Swift
let prices: [String: Int]? = nil

// Optional binding
if let actualPrices = prices { // could have let prices
	prices["Sushi"] 
} else {
	print("Prices not available")
}
```

### Optional Chaining
```Swift
let prices: [String: Int]? = nil

// Optional binding
if let prices { 
	prices["Sushi"] 
} else {
	print("Prices not available")
}

// Optional Chaining
let numberOfPrices: Int? = prices?.count

// let numberOfPrices: Int = (prices?.count) ?? 0 
// set default value in case of nil
```
>if `nil` returns `nil`


## Functions
```Swift
func myFunction() -> Void { // the return type: Void
	print("Hi I am a function!")
}

myFunction() // call function

func greet(name: String, age: Int? = nil) -> Int { // function w/args (labeled)
	print("Hi \(name), I am a function!")
	return 2 + 2
}

great(name: "John") // call function w/label
```

### First-Class Functions (Lambdas)
```Swift
let emoji = ["😭", "😎", "🤣"]
func repeatThrice(string: String) -> String {
	return "\(string)\(string)\(string)"
}

emoji.map(repeatThrice)

// Closure
emoji.map({ string in
	return "\(string)\(string)\(string)"
})

// or 
emoji.map({ return "\($0)\($0)\($0)" })

// trailing closure & assumes 1 line return
emoji.map { "\($0)\($0)\($0)" }
```

## Classes
```Swift
// Mark: - Classes
class Receipt {
	var items: [String]
	var amount = Double 
	var numberOfItems: Int { // quasi-property/method
		items.count
	}
	// Initialization
	init(items: [String], amount: Int) { 
		self.items = []
	}
	// method
	func applyDiscount(percent: Int) {
		amount *= (100 - percent)/100
	}
}

// construct Receipt instance 
let receipt = Receipt(items: ["Polishing Cloth"], amount: 19) 
receipt.applyDiscount(percent: 20)
receipt.nubmrOfItems
```

## Structs
```Swift
struct Receipt {
	var items: [String]
	var amount: Double 
	var numberOfItems: Int {
		items.count
	}
	// Initialization
	init(items: [String], amount: Int) { 
		self.items = []
	}
	// methods
	mutating func applyDiscount(percent: Double) {
		amount *= (100 - percent)/100
	}
}

// construct Receipt instance 
var receipt = Receipt(items: ["Polishing Cloth"], amount: 19) 
receipt.applyDiscount(percent: 20)
receipt.nubmrOfItems

receipt.items.append("Apple Vision Pro")
receipt.numberOfItems

// now receipt2 is a copy of receipt
let receipt2 = receipt
receipt2.items.append("Mac Pro")
```


## Enumerations
```Swift
@frozen public enum 
```


## Protocols 
```Swift
protocol ComputerStore {
	var name: String { get }
	func buy Computer() -> Receipt
}
```

### Built-in Protocol
```Swift
public protocol Equatable {
	static func == (lhs: Self, rhs: Self) -> Bool
}
```


## Extensions
```Swift
extension Receipt: Equatable {
	static func ==(lhs: Receipt, rhs: Receipt) -> Bool {
		return lhs.items = rhs.items && lhs.amount == rhs.amount
	}
}
```
>add methods after-the-fact


## Error Handling 
```Swift
enum BankError: Error {
	case insufficientFunds
}

struct BankAccount {
	var funds: Int
	mutating func transfer()
}

var alice = BankAccount(funds: 0)
var bob = BankAccount(funds: 100)

do {
	try alice.transfer(amount: 100, to: &bob)
} catch {
		 print("Couldn't transfer money: \(error)")
}
```

### Other Error Handlings
`try!` & `try?`