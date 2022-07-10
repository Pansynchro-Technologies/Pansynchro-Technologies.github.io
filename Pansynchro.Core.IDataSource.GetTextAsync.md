# [IDataSource](Pansynchro.Core.IDataSource.html).GetTextAsync Method

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

The GetTextAsync methods retrieves data from the data source as a [TextReader](https://docs.microsoft.com/en-us/dotnet/api/system.io.textreader).

### Overloads:

| [GetTextAsync()](#m0) | Retrieves binary data from an external source. |
| [GetTextAsync(string)](#m1) | Retrieves a specific binary data stream from an external source. |

## <a name="m0">GetDataAsync()</a>

## Returns:
| [IAsyncEnumerable](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.iasyncenumerable-1)&lt;([string](https://docs.microsoft.com/en-us/dotnet/api/system.string) name, [TextReader](https://docs.microsoft.com/en-us/dotnet/api/system.io.textreader) data)&gt; | A sequence of [value tuples](https://docs.microsoft.com/en-us/dotnet/api/system.valuetuple-2) containing a stream name and a [TextReader](https://docs.microsoft.com/en-us/dotnet/api/system.io.textreader) carrying the textual data. |

## Remarks:
This method retrieves all of the data available to the data source according to its configuration.  Each TextReader returned should be [disposed](https://docs.microsoft.com/en-us/dotnet/api/system.idisposable#remarks) before the next one is loaded, to avoid resource leaks.


## <a name="m1">GetDataAsync(string)</a>

### Parameters:
`name` [string](https://docs.microsoft.com/en-us/dotnet/api/system.string)<BR>
The stream name to read.

## Returns:
| [IAsyncEnumerable](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.iasyncenumerable-1)&lt; [TextReader](https://docs.microsoft.com/en-us/dotnet/api/system.io.textreader))&gt; | A sequence of [TextReader](https://docs.microsoft.com/en-us/dotnet/api/system.io.textreader)s carrying the textual data. |

## Remarks:
This method will retrieve all of the data that matches the provided stream name.  (Mapping of stream names to source data elements is typically provided as a part of the data source's configuration.)  It is specified as an async enumerable rather than a single text reader because there can easily be multiple data elements that logically make sense as a single data stream.  (For example, a folder containing several CSV files matching the same schema, each one corresponding to a single day worth of data.)  Merging multiple streams of data with the same name into a single stream is the responsibility of the [reader.](Pansynchro.Core.IReader.html)  The convenience method [DataStream.CombineStreamsByName](Pansynchro.Core.DataStream.CombineStreamsByName.html) can help with this task.
