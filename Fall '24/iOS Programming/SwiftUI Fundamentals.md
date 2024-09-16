## How to Code UI
### Manual Drawing
>issue drawing commands ==TERRIBLE== 

### Object-Oriented Widgets
>widgets based drawing ==Slightly LESS BAD==

### Declarative UI
>specify what you want on the screen 

## Views
>building blocks 
>	composed of other views (sub-component)
>are Swift structs

```Swift
struct HeaderView: View {
	var body: some View {
		HStack {
			Text()...
			Spacer()...
			Body()...
		}
	}
}
```

### Primitive Views
- Images
- Buttons
- Color
- Stacks

### View Modifier
>protocol method applied to a view or another view modifier to produce a <u>new version</u> of the original value

