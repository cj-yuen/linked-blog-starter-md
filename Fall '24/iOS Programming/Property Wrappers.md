>attributes that add additional behavior to properties

## @State
>declares a source of truth for data local to a view 
>	redraws when the value changes 
>best for ==simple local data== (ie. toggle status, input text, or a counter)
><u>Ownership:</u> View owns the data

```Swift
struct ContentView: View {
	@State private var isOn = false
	
	var body: some View {
		Toggle("Switch", isOn: $isOn)
	}
}
```

## @Binding
>allows a view to mutate data owned by someone else
>	redraws when the underlying value changes
>best for ==sharing== state w/o owning it (ie. letting a text field edit its parent's state)
><u>Ownership:</u> Someone else owns the data (ie. a parent)

```Swift
struct ParentView: View {
	@State private var text = ""
	
	var body: some View {
		ChildView(text: $text) // let Swift know we're passing in a binding
	}
}

struct ChildView: View {
	@Binding var text: String
	
	var body: some View {
		TextField("Enter text", text: $text)
	}
}
```

## @StateObject
>lets a view respond to changes in an ObservableObject
>	redraws when a @Published property changes
>best for ==Complex Objects== owned by a view (ie. complex view model)
><u>Ownership:</u> View owns the object

```Swift
class UserModel: ObservableObject {
	@Published var name: String = ""
}
```

## @ObservedObject
>listens to an object owned by someone else
>	redraw when a @Published property changes
>best for ==passing a StateObject== to another view 

## @EnvironmentObject
>accesses shared data from the environment
>	objects are implicitly shared (not explicitly passed)
>	redraws when a @Published property changes
>best for ==sharing an object across an entire section== of an app
><u>Ownership:</u> someone else owns the data


![[Pasted image 20240919194223.png]]
