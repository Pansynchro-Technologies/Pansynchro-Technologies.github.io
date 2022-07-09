# [IReader](Pansynchro.Core.IReader.html).TestConnection() Method

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

A tooling-friendly method for verifying that a reader is configured properly and able to retrieve data.

### Signature:
```
Task<Exception?> TestConnection();
```

### Returns:
[Task](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.task-1?view=net-6.0)&lt;[Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception?view=net-6.0)?&gt;<BR>
A Task whose value once awaited is null if the test was successful, othrewise reporting any problem that occurred during the connection test.

## Remarks:
This method is designed to make it simple for tooling or scripts to setup and test a connection.  By configuring a reader and then calling `TestConnection()`, code can quickly verify that the configuration is valid and the data is reachable.  It returns any relevant `Exception` rather than throwing it, to avoid needing to wrap the call in a try block.
