# [DataStream](Pansynchro.Core.DataStream.html).Reader Property

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Represents the data contained by a stream.

## Signature
```
public IDataReader Reader { get; }
```

## Remarks

This [IDataReader](https://docs.microsoft.com/en-us/dotnet/api/system.data.idatareader) instance is used to access the data of the stream.

*Note to data stream consumers:* The reader should always be read all the way to the end, (until [Read()](https://docs.microsoft.com/en-us/dotnet/api/system.data.idatareader.read) returns `false`,) and then [disposed,](https://docs.microsoft.com/en-us/dotnet/api/system.idisposable.dispose#remarks) before fetching the next data stream in a sequence.  Different connectors can break in different ways if either of these two points are not observed.
