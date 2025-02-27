## in the Past
![[Pasted image 20250225142902.png]]

## Polygon Mesh Implementation
![[Pasted image 20250225142923.png]]

### Well-Formed Surfaces
![[Pasted image 20250225142954.png]]
![[Pasted image 20250225143008.png]]

## Simple Data Structures
- [[List of Polygon Faces Structure]]
- [[List of Edges Structure]]
- [[Vertices & Index-Based Faces Structure]]

## Computational Complexity
![[Pasted image 20250225143417.png]]

## Naive Adjacency
![[Pasted image 20250225143828.png]]

## Half-Edge Data Structure
![[Pasted image 20250225143848.png]]

## Incomplete Half-Edge Meshes
![[Pasted image 20250225143906.png]]

![[Pasted image 20250225143917.png]]

## Polls
![[Pasted image 20250225143925.png]]
### Answer
>

![[Pasted image 20250225150224.png]]
### Answer
>`vector<Face*> getAdjacents(Face* f)`

## Half-Edge Advantages
![[Pasted image 20250225150444.png]]

## Half-Edge Operations
### Split Edge
![[Pasted image 20250225150501.png]]
![[Pasted image 20250225150516.png]]
![[Pasted image 20250225150524.png]]
![[Pasted image 20250225150531.png]]
![[Pasted image 20250225150537.png]]
![[Pasted image 20250225150545.png]]
![[Pasted image 20250225150552.png]]
![[Pasted image 20250225150603.png]]

### Triangulate
![[Pasted image 20250225150629.png]]
![[Pasted image 20250225150635.png]]
![[Pasted image 20250225150641.png]]
![[Pasted image 20250225150648.png]]

### Split Edge
>when updating pointers, all pointers between elements are symmetrical (if you update `vertex v -> edge e`, then edge e must also `e -> v`
```C++
class Face {
	HalfEdge *edge;
	friend class HalfEdge;
}

class HalfEdge {
private:
	Face *face;
	HalfEdge *next;
	HalfEdge *sym;
	Vertex *vert;
	
	friend class Vertex;
	friend class Face;
	
public:
	void setVertex(Vertex *v) {
		this->vert = v;
		v->edge = this;
	}
	
	void setFace(Face *f){ 
	}
}
```

### Process .obj -> Half-Edge structure
```C++
v x y z 
v x y z 
v x y z
v x y z

f a/a/a a/a/a a/a/a
f b/b/b b/b/b b/b/b
f c/c/c c/c/c c/c/c
f d/d/d d/d/d d/d/d

void loadOBJ(QString filepath) {
	// 0. Set up file parsing boilerplate code
	
	// 1. Read all the v lines in the file
	if (line begins with "v ") {
		parse the x y z tokens for floating point numbers
		uPtr<Vertex> v = mkU<Vertex>(x, y, z);
	}
	
	std::map<pair<Vertex*, Vertex*>, HalfEdge*> symPairingData;
	
	eles if (line begins with "f") {
		uPtr<Face> f = mkU<Face>();
		HalfEdge* prev = nullptr;
		HalfEdge *firstHE = nullptr;
		
		for (each number triplet on f line) {
			uPtr<HalfEdge> e = mkU<HalfEdge>();
			int idx = triplet.firstNumber;
			Vertex *vNext = this->vertices[idx - 1].get();   // .get() returns a *
														 // pointer to the heap
			e->setVertex(vNext);
			e->setFace(f.get());
			
			Vertex *vPrev = triplet - 1 except mod number of triplets in f line;
			// I suggest wrigting code that enforces a consistent ordering
			// on the pair, for example, always putting 
			// vertex with the lower mem address as the 1st element
			pair<Vertex*, Vertex*> key = VPrev< vNext ? {vPrev, vNext} : {vNext, vPrev};
			if (symPairingData.contains(key)) {
				edge->setSym(symPairingData.at(key));
			}
			else {
				symPairingData.insert(key);
			}
			
			if (prev != nullptr) {
				prev->next = e.get();
			}
			else {
				firstHE = e.get();
			}
			prev = e.get();
		}
		prev-> next = firstHE;
	}
}
```