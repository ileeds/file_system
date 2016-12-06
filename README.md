# file_system

Part 1 (Bitwise.java):

Performs bitwise operation on a byte or array of bytes.
Check to see if byte is set using & operator, and sets byte with | operator.
Clears set bytes with ^ operator.
ToString method to represent bytes.

Part 2 (MyFileSystem.java):

The method getDirectBlock takes parameters: file descriptor of an open file, and mode (read or write). Finds if the location of the file is within a direct, single indirect, double indirect, or triple indirect block.

The method direct is for direct blocks. If the block is empty and needs to be read, it returns a hole. If it is empty but there are no open locations, returns null. Otherwise, returns a direct block.

The methods singleIndirect and doubleIndirect (using getDirectSingle and getDirectDouble) use pointers from indirect blocks to find direct blocks.

Triple indirection has not been implemented.
