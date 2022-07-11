# DataStream Class

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

The Pansynchro framework's internal representation of a stream of data actively being synced.

## Remarks
A data stream consists of a name, some metadata flags, and an [IDataReader](https://docs.microsoft.com/en-us/dotnet/api/system.data.idatareader) instance providing access to the data itself.

## Constructors
| [DataStream(StreamDescription, StreamSettings, IDataReader)](Pansynchro.Core.DataStream.ctor.html) | Initializes a new DataStream with a stream name object, settings metadata, and a data reader. |

## Properties
| [Name](Pansynchro.Core.DataStream.Name.html) | [StreamDescription](Pansynchro.Core.StreamDescription.html) | The full name of the stream. |
| [Settings](Pansynchro.Core.DataStream.Settings.html) | [StreamSettings](Pansynchro.Core.StreamSettings.html) | Metadata flags giving information about the stream. |
| [Reader](Pansynchro.Core.DataStream.Reader.html) | [IDataReader](https://docs.microsoft.com/en-us/dotnet/api/system.data.idatareader) | Data reader containing the stream data. |

## Methods
| [Transformed(Func&lt;IDataReader, IEnumerable&lt;object[]&gt;&gt;)](Pansynchro.Core.DataStream.Transformed.html) | Applies a transformation method to the stream. |
| [CombineStreamsByName(IAsyncEnumerable&lt;DataStream&gt;)](Pansynchro.Core.DataStream.CombineStreamsByName.html) | Combines multiple streams with the same name into one. |

## See Also

* [IReader interface](Pansynchro.Core.IReader.html)
* [IWriter interface](Pansynchro.Core.IWriter.html)
