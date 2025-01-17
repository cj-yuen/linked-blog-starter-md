1) make URLRequest
```Swift
func makeNetworkRequest() {
	let url = URL(string: "https://demo.com")!
	var request = URLRequest(url: url)
	// ...
}
```

2) use URLSession.shared to make request
```Swift
func makeNetworkRequest() {
	let url = URL(string: "https://demo.com")!
	var request = URLRequest(url: url)
	let (data, response) = try await URLSession.shared.data(for: request)
	// ...
}
```

3) Handle errors
```Swift
func makeNetworkRequest() {
	let url = URL(string: "https://demo.com")!
	var request = URLRequest(url: url)
	let (data, response) = try await URLSession.shared.data(for: request)
	guard let httpsResponse = response as? HTTPURLResponse,
		httpResponse.statusCode >= 200, httpResponse.statusCode <= 299 else {
		throw NetworkError.networkError	
	}
	// ...
}
```

4) Do something w/response data
```Swift
func makeNetworkRequest() {
	let url = URL(string: "https://demo.com")!
	var request = URLRequest(url: url)
	let (data, response) = try await URLSession.shared.data(for: request)
	guard let httpsResponse = response as? HTTPURLResponse,
		httpResponse.statusCode >= 200, httpResponse.statusCode <= 299 else {
		throw NetworkError.networkError	
	}
	print(data)
}
```

## Returned data
- has type Data (list of bytes, <u>NOT</u> a string)
	`String(data: data, encoding: .utf8)`
- many ways to use URLSession
	![[Pasted image 20241024191649.png]]
- URLSession.shared keeps track of cookies & other session related information

## Doing USEFUL things w/Data: 
>Encodable & Decodable

### Detour: JSON 
![[Pasted image 20241024193045.png]]

## Receiving Data in requests
1) Make struct matching expected JSON response
```Swift
struct Post: Identifiable, Hashable, Deocodable {
	let id: UUID
	let author: String
	let content: String
	let createdAt: Date
}
```

2) Use JSONDecoder to decode data
![[Pasted image 20241024193208.png]]

#### Specialized Decoding
![[Pasted image 20241024193228.png]]

## Sending Data in requests
1) Make struct conform to Encodable 
```Swift
struct Post: Identifiable, Hashable, Encodable {
	let id: UUID
	let author: String
	let content: String
	let createdAt: Date
}
```


2) Use JSONEncoder to encode data
![[Pasted image 20241024193340.png]]

### Type of encodedData
`let encodedData = try encoder.encode(post)`

## Sending JSON data in network request
```Swift
var request = URLRequest(url:url)
request.httpMethod = "POST"
request.addValue("application/json", forHTTPHeaderField: "Content-Type")
request.httpBody = try JSONEncoder().encode(post)
```