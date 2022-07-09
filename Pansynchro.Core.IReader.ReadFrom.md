# [IReader](Pansynchro.Core.IReader.html).ReadFrom(DataDictionary) Method

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Reads data from the connector into a sequence of [DataStream](Pansynchro.Core.DataStream.html)s.

### Signature:
```
IAsyncEnumerable<DataStream> ReadFrom(DataDictionary source);
```

### Parameters:
`source` [DataDictionary](Pansynchro.Core.DataDict.DataDictionary.html)<BR>
A Data Dictionary describing the data to be retrieved.

### Returns:
[IAsyncEnumerable](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.iasyncenumerable-1?view=net-6.0)&lt;[DataStream](Pansynchro.Core.DataStream.html)&gt;<BR>
The sequence of Data Streams read by the connector.

## Remarks:
When the reader implements [ISourcedConnector](Pansynchro.Core.ISourcedConnector.html), it is necessary to supply a [Data Source](Pansynchro.Core.IDataSource) before calling this method.  Failing to do so will raise an exception.

A [DataStream](Pansynchro.Core.DataStream.html) consists of three parts: a stream name, settings metadata, and a [data reader.](https://docs.microsoft.com/en-us/dotnet/api/system.data.idatareader?view=net-6.0)  The reader implements [IDisposable](https://docs.microsoft.com/en-us/dotnet/api/system.idisposable?view=net-6.0), and must be disposed before retrieving the next DataStream.  Failing to do so can cause resource leaks and performance problems, and will also raise exceptions on some readers.    It can be disposed directly, or indirectly by calling `Dispose()` on the DataStream.
