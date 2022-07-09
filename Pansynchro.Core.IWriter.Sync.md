# [IWriter](Pansynchro.Core.IWriter.html).Sync(IAsyncEnumerable&lt;DataStream&gt;, DataDictionary) Method

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Writes out the data from a sequence of [DataStream](Pansynchro.Core.DataStream.html)s.

### Signature:
```
Task Sync(IAsyncEnumerable<DataStream> streams, DataDictionary dest);
```

### Parameters:
`streams` [IAsyncEnumerable](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.iasyncenumerable-1?view=net-6.0)&lt;[DataStream](Pansynchro.Core.DataStream.html)&gt;<BR>
The data to be written, retrieved from an [IReader](Pansynchro.Core.IReader.html), possibly after having been processed by an [ITransformerer](Pansynchro.Core.ITransformer.html).

`dest` [DataDictionary](Pansynchro.Core.DataDict.DataDictionary.html)<BR>
A Data Dictionary describing the data to be written.

### Returns:
[Task](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.task?view=net-6.0)<BR>
A Task representing the progress and completion of the long-running async write operation.

## Remarks:
When the writer implements [ISinkConnector](Pansynchro.Core.ISinkConnector.html), it is necessary to supply a [Data Sink](Pansynchro.Core.IDataSink) before calling this method.  Failing to do so will raise an exception.
