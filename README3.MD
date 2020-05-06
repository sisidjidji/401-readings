# read3


- File and stream I/O (input/output) refers to the transfer of data either to or from a storage medium.

- In the .NET Framework, the System.IO namespaces contain types that enable reading and writing, both synchronously and asynchronously, on data streams and files.

- Here are some commonly used file and directory classes:

1. File - provides static methods for creating, copying, deleting, moving, and opening files, and helps create a FileStream object.

2. FileInfo - provides instance methods for creating, copying, deleting, moving, and opening files, and helps create a FileStream object.

3. Directory - provides static methods for creating, moving, and enumerating through directories and subdirectories.

4. DirectoryInfo - provides instance methods for creating, moving, and enumerating through directories and subdirectories.

4. Path - provides methods and properties for processing directory strings in a cross-platform manner.

- You should always provide robust exception handling when calling filesystem methods

- Streams involve three fundamental operations:

1. Reading - transferring data from a stream into a data structure, such as an array of bytes.

2. Writing - transferring data to a stream from a data source.

3. Seeking - querying and modifying the current position within a stream.

- Here are some commonly used reader and writer classes:

1. BinaryReader and BinaryWriter – for reading and writing primitive data types as binary values.

2. StreamReader and StreamWriter – for reading and writing characters by using an encoding value to convert the characters to and from bytes.

3. StringReader and StringWriter – for reading and writing characters to and from strings.

4. TextReader and TextWriter – serve as the abstract base classes for other readers and writers that read and write characters and strings, but not binary data.

- Compression refers to the process of reducing the size of a file for storage. 


- The following classes are frequently used when compressing and decompressing files and streams:

ZipArchive – for creating and retrieving entries in the zip archive.

ZipArchiveEntry – for representing a compressed file.

ZipFile – for creating, extracting, and opening a compressed package.

ZipFileExtensions – for creating and extracting entries in a compressed package.

DeflateStream – for compressing and decompressing streams using the Deflate algorithm.

GZipStream – for compressing and decompressing streams in gzip data format.


- Isolated storage is a data storage mechanism that provides isolation and safety by defining standardized ways of associating code with saved data.

- The following classes are frequently used when implementing isolated storage:

IsolatedStorage – provides the base class for isolated storage implementations.

IsolatedStorageFile – provides an isolated storage area that contains files and directories.

IsolatedStorageFileStream - exposes a file within isolated storage.

- he .NET for Windows 8.x Store apps contains many of the types for reading from and writing to streams; however, this set does not include all the .NET Framework I/O types.


