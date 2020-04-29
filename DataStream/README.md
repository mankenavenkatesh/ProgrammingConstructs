# What is Data Streams?
Stream is nothing but continues flow of data. it can be of any type either character or byte stream.

They are data-handling method and are used to read or write input into output sequentially.

Stream is a sequence of data elements. like when you typing something in your computer then when you press the keys it will form a data stream and then it goes to the processor for processing.

Streams are a way to handle reading/writing files, network communications, or any kind of end-to-end information exchange in an efficient way.

```
What makes streams unique, is that instead of a program reading a
file into memory all at once like in the traditional way, streams
read chunks of data piece by piece, processing its content without
keeping it all in memory.

This makes streams really powerful when working with large amounts of
data, for example, a file size can be larger than your free memory
space, making it impossible to read the whole file into the memory in
order to process it. That’s where streams come to the rescue!

Using streams to process smaller chunks of data, makes it possible to
read larger files.

```

# Examples

```
Let’s take a “streaming” services such as YouTube or Netflix for
example: these services don’t make you download the video and audio
feed all at once. Instead, your browser receives the video as a
continuous flow of chunks, allowing the recipients to start watching
and/or listening almost immediately.

```

# Where can it be used?

```
However, streams are not only about working with media or big data.
They also give us the power of ‘composability’ in our code. Designing
with composability in mind means several components can be combined
in a certain way to produce the same type of result. In Node.js it’s
possible to compose powerful pieces of code by piping data to and
from other smaller pieces of code, using streams.
```

# Stream Types
I/O Stream represents an input source or an output destination. A stream can represent many different kinds of sources and destinations, including disk files, devices, other programs, and memory arrays.

