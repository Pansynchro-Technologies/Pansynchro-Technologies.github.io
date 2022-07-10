# DataStream Class

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

The Pansynchro framework's internal representation of a stream of data actively being synced.

## Remarks

A data stream consists of a name, some metadata flags, and an [IDataReader](https://docs.microsoft.com/en-us/dotnet/api/system.data.idatareader?view=net-6.0) instance providing access to the data itself.

## Constructors

| [DataStream(StreamDescription, StreamSettings, IDataReader)](Pansynchro.Core.DataStream.ctor.html) | Initializes a new DataStream with a stream name object, settings metadata, and a data reader. |

## Methods

| [CombineStreamsByName(IAsyncEnumerable&lt;DataStream&gt;)](Pansynchro.Core.DataStream.CombineStreamsByName.html) | Combines multiple streams with the same name into one. |

## See Also

* [IReader interface](Pansynchro.Core.IReader.html)
* [IWriter interface](Pansynchro.Core.IWriter.html)

