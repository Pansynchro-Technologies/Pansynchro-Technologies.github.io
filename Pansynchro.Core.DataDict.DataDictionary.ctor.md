# DataDictionary Constructors

## Definition

Namespace: Pansynchro.Core.DataDict<BR>
Assembly: Pansynchro.Core

### Overloads:

| [DataDictionary(string, StreamDefinition[])](#c0) | Initializes a new DataDictionary with a name and data stream definitions, but no advanced metadata. |
| [DataDictionary(string, StreamDefinition[], StreamDescription[][], Dictionary&lt;string, FieldType&gt;, Dictionary&lt;StreamDescription, IncrementalStrategy&gt;)](#c1) | Initializes a new DataDictionary with a name, data stream definitions, dependency order data, custom types, and incremental mappings. |

## <a name="c0">DataDictionary(string, StreamDefinition[])</a>

### Parameters:
`Name` [string](https://docs.microsoft.com/en-us/dotnet/api/system.string)<BR>
The name of the data dictionary.  Should describe the data in an easily-understandable way.

'Streams' [StreamDefinition](Pansynchro.Core.DataDict.StreamDefinition.html)[]<BR>
The set of data streams represented by this dictionary.  A stream represents a sequence of values of the same type of data, such as a single database table or CSV file.

### Remarks:
This simplified constructor sets up a DataDictionary with stream definitions but no advanced metadata.  It is suitable for non-database data sources that don't provide table dependencies, custom types, etc.


## <a name="c1">DataDictionary(string, StreamDefinition[], StreamDescription[][], Dictionary&lt;string, FieldType&gt;, Dictionary&lt;StreamDescription, IncrementalStrategy&gt;)</a>

### Parameters:
`Name` [string](https://docs.microsoft.com/en-us/dotnet/api/system.string)<BR>
The name of the data dictionary.  Should describe the data in an easily-understandable way.

`Streams` [StreamDefinition](Pansynchro.Core.DataDict.StreamDefinition.html)[]<BR>
The set of data streams represented by this dictionary.  A stream represents a sequence of values of the same type of data, such as a single database table or CSV file.

`DependencyOrder` [StreamDescription](Pansynchro.Core.StreamDescription.html)[][]<BR>
A representation of the order in which streams need to be read. This is useful when syncing to a SQL database with foreign key constraints that must be maintained.

`CustomTypes` [Dictionary](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2)&lt;[string](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FieldType](Pansynchro.Core.DataDict.FieldType.html)&gt;<BR>
Lists any custom types defined by the source data.

`Incremental` [Dictionary](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2)&lt;[StreamDescription](Pansynchro.Core.StreamDescription.html), [IncrementalStrategy](Pansynchro.Core.Incremental.IncrementalStrategy.html)&gt;<BR>
Stores information on which streams support incremental sync and the method by which their bookmarking is kept track of.

### Remarks:
This is the standard constructor to set up a data dictionary with full metadata.
