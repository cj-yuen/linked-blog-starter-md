>objects in a [[Collections]] must be homogenous & mutable
>	however you cannot have abstract object as type in a collection
>	you can store pointers to objects in a collection to make sure they have the same memory footprint
>		`std::vector<Geometry&> objects` <u>NOT</u> fine
>		`std::vector<Geometry*> objects` <u>fine</u>

`std::array` - lives on the stack by default
`std::vector` - lives on the heap by default