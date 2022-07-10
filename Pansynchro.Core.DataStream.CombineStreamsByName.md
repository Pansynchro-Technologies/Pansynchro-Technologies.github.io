# [DataStream](Pansynchro.Core.DataStream.html).CombineStreamsByName(IAsyncEnumerable&lt;DataStream&gt;) Method

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Combines multiple streams with the same name into one.

### Signature:
```
public static async IAsyncEnumerable<DataStream> CombineStreamsByName(IAsyncEnumerable<DataStream> source)
```

### Parameters:
`source` [IAsyncEnumerable](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.iasyncenumerable-1?view=net-6.0)&lt;[DataStream](Pansynchro.Core.DataStream.html)&gt;<BR>
The original sequence of data streams.

### Returns:
[IAsyncEnumerable](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.iasyncenumerable-1?view=net-6.0)&lt;[DataStream](Pansynchro.Core.DataStream.html)&gt;<BR>
A compacted sequence of data streams with like names combined.

## Remarks:
This is a convenience method, used internally by connectors that retrieve multiple inputs from their [data source](Pansynchro.Core.IDataSource) that have the same type and stream name and ought to be treated as a single continuous stream of data.
