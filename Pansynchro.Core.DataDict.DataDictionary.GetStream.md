# [DataDictionary](Pansynchro.Core.DataDict.DataDictionary.html).GetStream Method

## Definition

Namespace: Pansynchro.Core.DataDict<BR>
Assembly: Pansynchro.Core

Retrieves a stream definition from the dictionary, given its name.

### Overloads

| [GetStream(string)](#m0) | Looks up a stream definition by its full name. |
| [GetStream(StreamDescription, NameStrategy)](#m1) | Looks up a stream definition by a name object and a [NameStrategy](Pansynchro.Core.DataDict.NameStrategy). |

## <a name="m0">GetStream(string)</a>

### Parameters:
`name` [string](https://docs.microsoft.com/en-us/dotnet/api/system.string)<BR>
The full name of the stream, as a string.

### Returns:
[StreamDefinition](Pansynchro.Core.DataDict.StreamDefinition.html)

### Remarks:
This will throw an exception if the requested name is not in the dictionary.


## <a name="m1">GetStream(StreamDescription, NameStrategy)</a>

### Parameters:
`name` [StreamDescription](Pansynchro.Core.StreamDescription.html)<BR>
A stream name object representing the name of the stream.

`strategy` [NameStrategy](Pansynchro.Core.DataDict.NameStrategy.html)<BR>
A name strategy object to adapt the stream name to this dictionary.

### Returns:
[StreamDefinition](Pansynchro.Core.DataDict.StreamDefinition.html)

### Remarks:
This will throw an exception if the requested name is not in the dictionary.

This overload is used to look up a stream matching an external name, such as when syncing from one database to a different type of database that may follow different naming conventions.
