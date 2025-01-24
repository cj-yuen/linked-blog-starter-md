>assign values to member variables before the constructor body
>	after function header, use ":" to begin [[Initialization Lists]] 

```C++
class Person {
private:
	int age;
	std::string name;
public:
	Person(int myAge, std::string myName);
	Person();
	
	~Person();
}

Person::Person(int myAge, std::string myName)
	: age(myAge), name(myName)
{}

Person::Person()
	: Person(50, "John Doe")
{}
```
>[[Destructors]] (as "~Person()")

