# CP-Something

## Binary Input/Output

### File Abstraction
* Lowest Level: Sequence of Bytes
  * We refer to this as a *stream*
* How we interpret each byte (or group of bytes) depends on the context

### Data Types
Different primitive data types in java require different amounts of space
* byte: 1 byte
* short: 2 bytes
* int/float: 4 bytes
* double: 8 bytes

### Binary I/O Classes
* We have 
* Object
  * OutputStream
  * FilterOutputStream
  * ObjectOutputStream
* Object
  * InputStream
    * FileInputStream
    * FilterInputStream
      * DataInputStream
      * BufferedInputStream
    * ObjectInputStream
### Character-level Interaction
**BufferedReader/BufferedWriter** (you already have experience with these):
* Read/write individual characters or entire Strings

### Buffering
* Storage devices store data in blocks of bytes
* Often more efficient to read/write entire blocks than the equivalent size of a few bytes a time
* BufferedReader reads an entire block at once and stores data temporarily in memory
* BufferedWriter stores written data temporarily in memory and then writes the data when a block is complete

### Data-Level Interaction
Want to store primitive types in the file without having to deal directly at the byte level
* DataInputStream/DataOutputStream

* readShort(), readLong(), readDouble()
* writeShort(), writeLong(), writDouble()

### DataInput(Output)Stream
DataInputStream/DataOutputStream write/read Java primitive values and strings in a machine independent array

### Object-Level Interation
* Can read/write entire objects in one call
* Read/Write is recursive
  * If an object contains references to other objects - they are read/written, too
* Class must implement the Serializable interface

### Very Recursive
When we write/read an object:
* All 
* Can keep a variable from being written using a *transient* keyword

```
pushd - goes to a directory
popd - goes back to where you came from
```
Read/Writing to a file
