# What is Data Buffer

Buffer is temporary placeholder in memory (ram/disk) on which data can be dumped and then processing can be done.

A Buffer object can be termed as container for a fixed amount of data. It acts as a holding tank, or temporary staging area, where data can be stored and later retrieved

# When to use Data Buffers
- Buffers are typically used when there is a difference between the rate at which data is received and the rate at which it can be processed, or in the case that these rates are variable, for example in a printer spooler or in online video streaming.

# Example Usages
```Java

   public static void main(String[] args) 
    {
        // Allocate a new non-direct byte buffer with a 50 byte capacity
        // set this to a big value to avoid BufferOverflowException
        ByteBuffer buf = ByteBuffer.allocate(50);
 
        // Creates a view of this byte buffer as a char buffer
        CharBuffer cbuf = buf.asCharBuffer();
 
        // Write a string to char buffer
        cbuf.put("How to do in java");
 
        // Flips this buffer. The limit is set to the current position and then
        // the position is set to zero. If the mark is defined then it is
        // discarded
        cbuf.flip();
 
        String s = cbuf.toString(); // a string
 
        System.out.println(s);
    }
}

https://howtodoinjava.com/java7/nio/java-nio-2-0-working-with-buffers/

```

```Go


https://golang.org/src/bytes/buffer.go
```

- References

- https://en.wikipedia.org/wiki/Data_buffer
- https://www.youtube.com/watch?v=I6kCtfeAZiA

