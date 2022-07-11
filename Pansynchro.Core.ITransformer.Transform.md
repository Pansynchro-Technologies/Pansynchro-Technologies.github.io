# [ITransformer](Pansynchro.Core.ITransformer.html).Transform Method

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Provides functionality for modifying the names and contents of [data streams](Pansynchro.Core.DataStream.html).

### Signature:
```
IAsyncEnumerable<DataStream> Transform(IAsyncEnumerable<DataStream> input);
```

### Parameters:
`input` [IAsyncEnumerable](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.iasyncenumerable-1)&lt;[DataStream](Pansynchro.Core.DataStream.html)&gt;<BR>
A sequence of streams to operate on.  This should originate from the [IReader.ReadFrom](Pansynchro.Core.IReader.ReadFrom.html) method.

### Returns:
[IAsyncEnumerable](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.iasyncenumerable-1)&lt;[DataStream](Pansynchro.Core.DataStream.html)&gt;<BR>
A modified sequence of streams with the same signature as `input`.

## Remarks:
A transformer can modify any or all of the streams in a sequence.  It should use a stream's [Name](Pansynchro.Core.DataStream.Name.html) property to determine which data stream(s) it's looking for.

Developers wishing to create their own transformers can inherit from the [StreamTransformerBase](Pansynchro.Core.StreamTransformerBase.html) class, which provides a skeleton of built-in functionality for modifying data streams.
