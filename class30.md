 # Hashtable Concepts and Methods:

## Hashtable:

A data structure that stores key-value pairs.
Utilizes a hash function to map keys to specific index locations in an array.
Provides quick O(1) time complexity for value retrieval.
## Hash:

The result of a hash function applied to a key to determine its index in the hashtable.
## Buckets:

Each index in the hashtable array is a bucket.
Buckets can hold multiple key-value pairs in case of collisions.
## Collisions:

Occur when multiple keys hash to the same index in the hashtable.
Resolved by using buckets with linked lists to store multiple key-value pairs.
## Why We Use Hashtables:

Efficient for storing and retrieving unique values.
Commonly used for implementing dictionaries and libraries.
## Structure of Hashtables:

Has a backing array to store key-value pairs.
Hashing algorithm determines the index for insertion and retrieval.
Each index contains buckets for handling collisions.
## Creating a Hash:

Typically created from an array, often with a fixed size.
Hashing algorithm converts keys into numerical values.
Hash code determines the index for key-value insertion.
## Hashmap Methods:

- set(): Adds a new key-value pair to the hashtable.
- get(): Retrieves a value by key from the hashtable.
- has(): Checks if a key exists in the hashtable.
- keys(): Returns an array of unique keys in the hashtable.
- hash(): Calculates the hash code for a given key.
## Hash Code Examples:

Hash functions can differ, resulting in different indices for keys.
Collisions can occur even with different hash functions.

## Bucket Sizes:

The number of buckets affects collision frequency.
The load factor determines when to resize the hashtable to maintain efficiency.
# Basics of Hash Tables

Hashing is a technique used to uniquely identify objects from a group using a hash function.
In hashing, large keys are converted into small keys using hash functions, and the values are stored in a data structure called a hash table.
Hashing involves two steps: converting an element into an integer using a hash function and then using that integer to access or store the element in a hash table.
## Hash Function

A hash function is used to map a data set of arbitrary size to a fixed-size data set, which falls into the hash table.
Good hash functions have the following requirements:
Easy to compute.
Uniform distribution to avoid clustering.
Minimize collisions (when two elements map to the same hash value).
## Hash Table

A hash table is a data structure used to store key/value pairs.
It uses a hash function to compute an index into an array where elements are inserted or searched.
With a good hash function, average time complexity for searching in a hash table is O(1).
## Collision Resolution Techniques

- Separate Chaining (Open Hashing):

Each element in the hash table is a linked list.
Collisions are resolved by adding elements with the same hash value to the same linked list.
Lookup time depends on the average number of keys per linked list.
- Linear Probing (Open Addressing or Closed Hashing):

All entry records are stored in the array itself.
When a collision occurs, search for the next available slot (with a fixed interval) until an empty slot is found.
Lookup time depends on the probing sequence and table size.
- Quadratic Probing:

Similar to linear probing, but the interval between successive probes is computed using a quadratic function.
Reduces clustering compared to linear probing.
- Double Hashing:

Interval between probes is determined by two hash functions.
Provides a more complex probing sequence.
Less likely to result in clustering compared to linear probing.
## Applications of Hash Tables

- Associative arrays, used in many programming languages.
- Database indexing for quick data retrieval.
- Caches to speed up data access.
- Object representation in dynamic languages like Python, JavaScript, etc.