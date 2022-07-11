# [DataStream](Pansynchro.Core.DataStream.html).Transformed(Func&lt;IDataReader, IEnumerable&lt;object[]&gt;&gt;) Method

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Applies a transformation method to the stream.

### Signature:
```
public DataStream Transformed(Func<IDataReader, IEnumerable<object[]>> transformer)
```

### Parameters:
`transformer` [Func](https://docs.microsoft.com/en-us/dotnet/api/system.func-2)&lt;[IDataReader](https://docs.microsoft.com/en-us/dotnet/api/system.data.idatareader), [IEnumerable](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)&lt;[object](https://docs.microsoft.com/en-us/dotnet/api/system.object)[]&gt;&gt;<BR>
A delegate that will read data from the data reader and produce a sequence of object arrays containing the transformed data.  Each array represents one row of data from the data reader.

### Returns:
[DataStream](Pansynchro.Core.DataStream.html)<BR>
A new data stream with the same name and settings as the old one, updated with the transformed data.

## Remarks:
**Note for transformation writers:** the following rules of thumb explain how to set up a well-behaved transformation.  Failure to follow these rules can lead to exceptions being thrown or data corruption.

Transformation methods should be apply their transformations consistently to the entire stream.  For example, all the output arrays should contain the same number of elements, in the same order, with the same types.  Essentially, the purpose of a transformation can be thought of as transforming one regular table of data into a different regular table of data.

In a normal read-transform-write workflow, the structure of the transformed data should match the stream schema in the writer's [data dictionary](Pansynchro.Core.DataDict.DataDictionary.html).

If the stream's [Settings](Pansynchro.Core.DataStream.Settings.html) property contains the `UseRcf` flag, the stream is sorted by rarely-changing fields.  Modifying these values can degrade performance if the data is being shipped across a network using the Pansynchro binary protocol.

The transformation delegate will be called once for the data stream.  It should process the entire reader, (looping until [Read()](https://docs.microsoft.com/en-us/dotnet/api/system.data.idatareader.read) returns `false`,) and then [dispose](https://docs.microsoft.com/en-us/dotnet/api/system.idisposable.dispose#remarks) it.  Different readers rely on these two behaviors in different ways, and can break if either one is not carefully observed.
