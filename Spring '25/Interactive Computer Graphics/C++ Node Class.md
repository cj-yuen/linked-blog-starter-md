```C++
class Node { // Abstract class -> cannot instantiate just a "Node" 
	std::vector<uPtr<Node>> children;
	Polygon2D* geom;
	
	virtual mat3 computeTranform() = 0;	
	// "virtual" = it can be overwritten by subclass
	// "= 0;" = it must be implemented in subclass
	
	Node(const Node&);
	Node& operator=(const Node&);
	
	virtual uPtr<node> clone() const = 0;
};

Node::Node(const Node& n2)
	: children(), geom(n2.geom)
{
	// for(int i = 0; i < n2.children.size(); ++i) {}
	// for (const auto& n : n2.children) {}
	
	for(const uPtr<Node>& n : n2.children) {
		// this->children.push_back(n); // we're trying to copy uPtr...
		// this->children.push_back(mkU<Node>(*n)); // Node is abstract...
		
		/* WE COULD DO SOMETHING LIKE THIS (BAD FORM)
		TNode* test1 = std::dynamic_cast<TNode*>*n.get());
		if(test1 != nullptr) {
			this->cildren.push_back(mkU<TNode>(*n));
		}
		*/
		
		this->children.push_back(n->clone());
	}
	
}

// Translate Node (Subclass)
class TNode : public Node {
	flaot x, y;
	mat3 compouteTransform() const override;
	uPtr<node> clone() const override {
		return mkU<TNode>(*this);
	}
};

// Rotate Node (Subclass)
class RNode : public Node {
	float angle;
	mat3 compouteTransform() const override;
	uPtr<node> clone() const override {}
};

// Scale Node (Subclass)
class SNode :public Node {
	float x, y;
	mat3 compouteTransform() const override;
	uPtr<node> clone() const override {}
};
```

