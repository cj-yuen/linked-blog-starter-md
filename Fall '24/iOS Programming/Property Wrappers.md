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