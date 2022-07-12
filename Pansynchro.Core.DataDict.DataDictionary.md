# DataDictionary Class

## Definition

Namespace: Pansynchro.Core.DataDict<BR>
Assembly: Pansynchro.Core

Contains a description of a set of data to be processed by the Pansynchro framework.

## Remarks

The data dictionary contains a representation of the data to be processed by a sync job.  It is produced by an [analyzer](Pansynchro.Core.ISchemaAnalyzer.html), which will yield a conservative description of the data, which can then be fine-tuned as desired.  When a sync is run, the data dictionary is treated as the canonical description of the work to be done; if a database contains tables (or its tables contain fields) that are not listed in the data dictionary, they will be excluded from the sync.  A user can take advantage of this to customize their sync jobs by selectively culling certain data from the dictionary.

Take care not to add data to the dictionary that does not exist in the source data; this will cause a reader to look for data that does not exist, which will likely raise an exception or cause other errors.

## Constructors

| [DataDictionary(string, StreamDefinition[])](Pansynchro.Core.DataDict.DataDictionary.ctor.html#c0) | Initializes a new DataDictionary with a name and data stream definitions, but no advanced metadata. |
| [DataDictionary(string, StreamDefinition[], StreamDescription[][], Dictionary&lt;string, FieldType&gt;, Dictionary&lt;StreamDescription, IncrementalStrategy&gt;)](Pansynchro.Core.DataDict.DataDictionary.ctor.html#c1) | Initializes a new DataDictionary with a name, data stream definitions, dependency order data, custom types, and incremental mappings. |

## Properties

| [Name](Pansynchro.Core.DataDict.DataDictionary.Name.html) | [string](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The name of the data dictionary.  Should describe the data in an easily-understandable way. |
| [Streams](Pansynchro.Core.DataDict.DataDictionary.Streams.html) | [StreamDefinition](Pansynchro.Core.DataDict.StreamDefinition.html)[] | The set of data streams represented by this dictionary.  A stream represents a sequence of values of the same type of data, such as a single database table or CSV file. |
| [DependencyOrder](Pansynchro.Core.DataDict.DataDictionary.DependencyOrder.html) | [StreamDescription](Pansynchro.Core.StreamDescription.html)[][] | A representation of the order in which streams need to be read. This is useful when syncing to a SQL database with foreign key constraints that must be maintained. |
| [CustomTypes](Pansynchro.Core.DataDict.DataDictionary.CustomTypes.html) | [Dictionary](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2)&lt;[string](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FieldType](Pansynchro.Core.DataDict.FieldType.html)&gt; | Lists any custom types defined by the source data. |
| [Incremental](Pansynchro.Core.DataDict.DataDictionary.Incremental.html) | [Dictionary](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2)&lt;[StreamDescription](Pansynchro.Core.StreamDescription.html), [IncrementalStrategy](Pansynchro.Core.Incremental.IncrementalStrategy.html)&gt; | Stores information on which streams support incremental sync and the method by which their bookmarking is kept track of. |
| [Names](Pansynchro.Core.DataDict.DataDictionary.Names.html) | [Dictionary](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2)&lt;[string](https://docs.microsoft.com/en-us/dotnet/api/system.string), [string](https://docs.microsoft.com/en-us/dotnet/api/system.string)&gt; | A dictionary of all stream names and the names of all the fields on each stream. |

## Methods

| [GetStream(string)](Pansynchro.Core.DataDict.DataDictionary.GetStream.html#m0) | Looks up a stream definition by its full name. |
| [GetStream(StreamDescription, NameStrategy)](Pansynchro.Core.DataDict.DataDictionary.GetStream.html#m1) | Looks up a stream definition by a name object and a [NameStrategy](Pansynchro.Core.DataDict.NameStrategy).  Used to look up a stream matching an external name. |
| [HasStream(string)](Pansynchro.Core.DataDict.DataDictionary.HasStream.html) | Checks whether a stream with the given name exists in the data dictionary. |
| [LoadFromFile(string)](Pansynchro.Core.DataDict.DataDictionary.LoadFromFile.html) | Reads a data dictionary saved to disc. |
| [SaveToFile(string)](Pansynchro.Core.DataDict.DataDictionary.SaveToFile.html) | Saves a data dictionary to disc. |
| [IncrementalStrategyFor(StreamDescription)](Pansynchro.Core.DataDict.DataDictionary.IncrementalStrategyFor.html) | Returns the incremental sync strategy for a given stream. |

## See Also

* [StreamDefinition class](Pansynchro.Core.DataDict.DataDictionary.StreamDefinition.html)
* [StreamDescription class](Pansynchro.Core.DataDict.DataDictionary.StreamDescription.html)
* [ISchemaAnalyzer interface](Pansynchro.Core.ISchemaAnalyzer.html)
