


# Readings: Classes & Memory Management

## why this topic matters as it relates to what you are studying in this module?

because in order to write more robust, efficient, and maintainable code, we have to know how classes, objects, and memory management work in the C# programming language. By understanding concepts like constructors, properties, and memory allocation on the stack and heap, developers can write more efficient and reliable code.

## Answers to questions:

1. What’s the difference between a static and an instance constructor?

a static constructor is called once per class before any static members are accessed, while an instance constructor is called each time an instance of a class is created.

2. How does the use of a static constructor differ from setting properties/values?

Setting properties/values can be done at any time during an object's lifetime

static constructor  called only once before any static member is accessed.

3. Knowing what you now know about the stack and the heap, how might you rethink the way you did projects in previous courses, to make more effecient use of memory?

avoiding unnecessary object creations. , Minimizing the use of large objects on the stack and allocating them on the heap instead.

4. Compare “Garbage Collection” in C# with the lifecycle of normal household items.

garbage collection is automatic whereas household is manual but both of them frees space occupied by things no longer in use.
______________
## Things I want to know more about

Memory management in .NET and how garbage collector works .

------------
[Home](./README.md)   