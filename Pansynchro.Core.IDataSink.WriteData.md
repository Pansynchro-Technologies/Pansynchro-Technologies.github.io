# [IDataSink](Pansynchro.Core.IDataSink.html).WriteData(string) Method

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Produces a [Stream](https://docs.microsoft.com/en-us/dotnet/api/system.io.stream) to write binary data to.

### Signature:
```
Task<Stream> WriteData(string streamName);
```

### Parameters:
`name` [string](https://docs.microsoft.com/en-us/dotnet/api/system.string)<BR>
The name of the data stream to write.

### Returns:
[Task](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.task-1)&lt;[Stream](https://docs.microsoft.com/en-us/dotnet/api/system.io.stream)&gt;<BR>
A task that will return a writeable stream when awaited.

## Remarks:
The data sink should have some configuration to determine how to use the provided stream names to save the data appropriately.
