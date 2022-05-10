# Read30:  Hash Tables
* Hashtables .
* What is a HashTable Data Structure .
* Basics of hash tables.
* Hash table wiki.

### *Hashtables*

- What is a Hashtable?
1. Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for 
either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
2. Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could 
potentially contain multiple key/value pairs if a collision occurs.
3. Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

- Why do we use them?
1. Hold unique values
2. Dictionary
3. library

- What Are they?

Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.

The basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value. This is done 
through what we call a hash. A hash is the ability to encode the key that will eventually map to a specific location in the data 
structure that we can look at directly to retrieve the value.

Since we are able to hash our key and determine the exact location where our value is stored, we can do a lookup in an O(1) time 
complexity. This is ideal when quick lookups are required.

- Internal Methods
* Add()

When adding a new key/value pair to a hashtable:
1. send the key to the GetHash method.
2. Once you determine the index of where it should be placed, go to that index
3. Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
4. If something does exist, add the new key/value pair to the data structure within that bucket.

* Find()

The Find takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, 
it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.

* Contains()

The Contains method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to 
have the contains call the GetHash and check the hashtable if the key exists in the table given the index returned.

* GetHash()

The GetHash will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be 
placed.


For more details see [useReducer hook](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html).

### *What is a HashTable Data Structure*

- A hash table is a data structure that is used to store information so that information in the hash table basically has two main 
components so it's going to have some sort of key and then it's going to have some sort of value or some sort of record and so 
basically a key could be something like for instance my name and the value could be something like my phone number so we could 
basically create a hash table to store a bunch of people's phone numbers .
-  The hash table is a way to implement an associative array and so we're basically going to map this key to this value .
-  A hash function is going to look to a certain key and then it's going to evaluate that key and it's going to spit it out  some 
sort of index number and it's going to tell us what location in the array to store this information .

For more details watch this video [What is a HashTable Data Structure](https://dotnetcorecentral.com/blog/react-js-with-asp-net-core-signalr/?msclkid=755cd705cf6a11eca009afc3a9069ab3).


### *Basics of hash tables*

- Basics of Hash Tables

Hashing is a technique that is used to uniquely identify a specific object from a group of similar objects. 

- Hashing is implemented in two steps:

1. An element is converted into an integer by using a hash function. This element can be used as an index to store the original 
element, which falls into the hash table.
2. The element is stored in the hash table where it can be quickly retrieved using hashed key.

       hash = hashfunc(key)
       index = hash % array_size

- Hash function

A hash function is any function that can be used to map a data set of an arbitrary size to a data set of a fixed size, which falls 
into the hash table. The values returned by a hash function are called hash values, hash codes, hash sums, or simply hashes.

To achieve a good hashing mechanism, It is important to have a good hash function with the following basic requirements:

1. Easy to compute: It should be easy to compute and must not become an algorithm in itself.
2. Uniform distribution: It should provide a uniform distribution across the hash table and should not result in clustering.
3. Less collisions: Collisions occur when pairs of elements are mapped to the same hash value. These should be avoided.

For more details see [Basics of hash tables](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/).

### *Hash table wiki*

- In computing, a hash table, also known as hash map, is a data structure that implements a set abstract data type, a structure that 
can map keys to values. A hash table uses a hash function to compute an index, also called a hash code, into an array of buckets or 
slots, from which the desired value can be found. During lookup, the key is hashed and the resulting hash indicates where the 
corresponding value is stored.

- A hash table is an implementation of set abstract data type

For more details see [Hash table wiki](https://reactjs.org/docs/hooks-reference.html#usereducer).


