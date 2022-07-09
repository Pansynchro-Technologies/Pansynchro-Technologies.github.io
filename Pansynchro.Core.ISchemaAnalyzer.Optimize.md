# [ISchemaAnalyzer](Pansynchro.Core.ISchemaAnalyzer.html).Optimize(DataDictionary, Action&lt;string&gt;) Method

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Attempt a more in-depth analysis to determine metadata that can improve on-the-wire sync performance.

### Signature:
```
Task<DataDictionary> Optimize(DataDictionary dict, Action<string>? report)
```

### Parameters:
`dict` [DataDictionary](Pansynchro.Core.DataDict.DataDictionary.html)<BR>
The dictionary to optimize.  This should be the result of a call to [OptimizeAsync](Pansynchro.Core.ISchemaAnalyzer.AnalyzeAsync.html) from this same ISchemaAnalyzer instance.

`report` [Action](https://docs.microsoft.com/en-us/dotnet/api/system.action-1?view=net-6.0)&lt;[string](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=net-6.0)&gt;?<BR>
A tooling-friendly option to pass a delegate for the task to report its progress.

### Returns:
[Task](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.task-1?view=net-6.0)&lt;[DataDictionary](Pansynchro.Core.DataDict.DataDictionary.html)&gt;<BR>
A task that will return the optimized DataDictionary when awaited.  **Note:** This is a new DataDictionary, not a modification of the existing instance.  The old value passed in will remain unchanged.

## Remarks:
When the analyzer implements [ISourcedConnector](Pansynchro.Core.ISourcedConnector.html), it is necessary to supply a [Data Source](Pansynchro.Core.IDataSource) before calling this method.  Failing to do so will raise an exception.

As the optimizer is an async method, it makes no guarantee that it will run on the same thread that it was invoked from.  Code that passes a callback to the `report` parameter must be aware of this and capable of safely handling callbacks from other threads.  In particular, the callback could come from a thread other than the main UI thread, which might then require special handling to use the passed string in UI code.

Be aware that, depending on the type and amount of data to be analyzed, the optimizer can take a significant amount of time to run.  This is why it's implemented as a separate method from `AnalyzeAsync`; `AnalyzeAsync` looks at metadata and runs very quickly, but `Optimize` scans the data itself.

Not all connectors necessarily implement this, beyond a [default implementation](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/tutorials/default-interface-methods-versions) that returns the passed data dictionary unmodified.
