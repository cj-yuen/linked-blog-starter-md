>classes that extend/modify functionality of some other function

## 3 levels of access
- ==private== - only instances of that class can access
- ==public== - everything can access
- ==protected== - only that class and the classes that inherit from it can access

## Example: Square inherits Geometry class w/diff implementation

```C++
class Geometry {
portected:
	int sides;
	int size;

public:
	virtual void PrintName() {
		std::cout << "GEOMTRY";
	}
	virtual void Area() = 0;
};
class Square : public Geometry {
public:
	void PrintName() override {
		std::cout << "SQUARE";
	}
	void Area() override {
		return size * size;
	}
}

```
>the ==virtual== keyword in the superclass header definition so that C++ knows to check the dynamic type of the function & determine whether to call the super-class or the sub-class version
>	add ==override== to function definition in subclass header