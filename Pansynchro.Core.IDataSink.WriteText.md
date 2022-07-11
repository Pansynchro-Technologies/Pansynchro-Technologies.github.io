# [IDataSink](Pansynchro.Core.IDataSink.html).WriteText(string) Method

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Produces a [TextWriter](https://docs.microsoft.com/en-us/dotnet/api/system.io.textwriter) to write textual data to.

### Signature:
```
Task<TextWriter> WriteText(string streamName);
```

### Parameters:
`name` [string](https://docs.microsoft.com/en-us/dotnet/api/system.string)<BR>
The name of the data stream to write.

### Returns:
[Task](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.task-1)&lt;[TextWriter](https://docs.microsoft.com/en-us/dotnet/api/system.io.textwriter)&gt;<BR>
A task that will return a text writer when awaited.

## Remarks:
The data sink should have some configuration to determine how to use the provided stream names to save the data appropriately.

This method has a default implementation provided, which simply calls [WriteData](Pansynchro.Core.IDataSink.WriteData.html) and wraps a [StreamWriter](https://docs.microsoft.com/en-us/dotnet/api/system.io.streamwriter) around the result.