>lets us organize multiple screens


## NavigationView
>deprecated in recent versions of iOS

![[Pasted image 20240928221954.png]]
```Swift
NavigationView {
	List {
		NavigationLink("Tap for analytics...") {
			Text("[pretend we have useful content]")
				.navigationTitle("Analytics")
				.navigationBarTitleDisplayMode(.inline)
		}
	}
	.navigationTitle("Bottleg Penn Mobile")
}
```

## NavigationStack
### directly linking to views
```Swift
NavigationStack {
	List {
		NavigationLink("Tap for analytics...") {
			Text("[pretend we have useful content]")
				.navigationTitle("Analytics")
				.navigationBarTitleDisplayMode(.inline)
		}
	}
	.navigationTitle("Bottleg Penn Mobile")
}
```

### presenting based on data
>allows you to modify path programmatically
```Swift
NavigationStack(path: $path) {
	List {
		NavigationLink("Tap for analytics...", value: "Analytics") 
	}
	.navigationTitle("Bottleg Penn Mobile")
	.navigationDestination(for: String.self) { value in // value passed into .navigationDestination
	Text("[pretend we have useful content]")
		.navigationTitle(value)
		.navigationBarTitleDisplayMode(.inline)
	}
}
```

## NavigationSplitView
![[Pasted image 20240928221938.png]]
```Swift
NavigationSplitView(sidebar: {
	Text("Sidebar")
}, content: {
	Text("Content")
}, detail: {
	Text("Detail")
})
.font(.largeTitle)
```
