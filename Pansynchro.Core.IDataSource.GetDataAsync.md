# [IDataSource](Pansynchro.Core.IDataSource.html).GetDataAsync Method

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

The GetDataAsync methods retrieves data from the data source as a [Stream](https://docs.microsoft.com/en-us/dotnet/api/system.io.stream).

### Overloads:

| [GetDataAsync()](#m0) | Retrieves binary data from an external source. |
| [GetDataAsync(string)](#m1) | Retrieves a specific binary data stream from an external source. |

## <a name="m0">GetDataAsync()</a>

## Returns:
| [IAsyncEnumerable](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.iasyncenumerable-1)&lt;([string](https://docs.microsoft.com/en-us/dotnet/api/system.string) name, [Stream](https://docs.microsoft.com/en-us/dotnet/api/system.io.stream) data)&gt; | A sequence of [value tuples](https://docs.microsoft.com/en-us/dotnet/api/system.valuetuple-2) containing a stream name and a [Stream](https://docs.microsoft.com/en-us/dotnet/api/system.io.stream) carrying the data. |

## Remarks:
This method retrieves all of the data available to the data source according to its configuration.  Each Stream returned should be [disposed](https://docs.microsoft.com/en-us/dotnet/api/system.idisposable#remarks) before the next one is loaded, either directly by the connector attached to the data source or as part of the [data reader](https://docs.microsoft.com/en-us/dotnet/api/system.data.idatareader) that it creates from the stream data, to avoid resource leaks.


## <a name="m1">GetDataAsync(string)</a>

### Parameters:
`name` [string](https://docs.microsoft.com/en-us/dotnet/api/system.string)<BR>
The stream name to read.

## Returns:
| [IAsyncEnumerable](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.iasyncenumerable-1)&lt; [Stream](https://docs.microsoft.com/en-us/dotnet/api/system.io.stream))&gt; | A sequence of [Stream](https://docs.microsoft.com/en-us/dotnet/api/system.io.stream)s carrying the data. |

## Remarks:
This method will retrieve all of the data that matches the provided stream name.  (Mapping of stream names to source data elements is typically provided as a part of the data source's configuration.)  It is specified as an async enumerable rather than a single stream because there can easily be multiple data elements that logically make sense as a single data stream.  (For example, a folder containing several CSV files matching the same schema, each one corresponding to a single day worth of data.)  Merging multiple streams of data with the same name into a single stream is the responsibility of the [reader.](Pansynchro.Core.IReader.html)  The convenience method [DataStream.CombineStreamsByName](Pansynchro.Core.DataStream.CombineStreamsByName.html) can help with this task.
