```C++
class Node { // Abstract class -> cannot instantiate just a "Node" 
	std::vector<uPtr<Node>> children;
	Polygon2D* geom;
	
	virtual mat3 computeTranform() = 0;	
	// "virtual" = it can be overwritten by subclass
	// "= 0;" = it must be implemented in subclass
};

// Translate Node (Subclass)
class TNode : public Node {
	flaot x, y;
	mat3 compouteTransform() const override;
};

// Rotate Node (Subclass)
class RNode : public Node {
	float angle;
	mat3 compouteTransform() const override;
};

// Scale Node (Subclass)
class SNode :public Node {
	float x, y;
	mat3 compouteTransform() const override;
};
```

