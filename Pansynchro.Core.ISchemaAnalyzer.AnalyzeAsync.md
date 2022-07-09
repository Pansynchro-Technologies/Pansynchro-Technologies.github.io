# [ISchemaAnalyzer](Pansynchro.Core.ISchemaAnalyzer.html).AnalyzeAsync(string) Method

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Analyzes the data to produce a [DataDictionary](Pansynchro.Core.DataDict.DataDictionary.html).

### Signature:
```
ValueTask<DataDictionary> AnalyzeAsync(string name);
```

### Parameters:
`name` [string](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=net-6.0)<BR>
An arbitrary name for the data dictionary.  Should describe the data in an easily-understandable way.

### Returns:
[ValueTask](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.valuetask-1?view=net-6.0)&lt;[DataDictionary](Pansynchro.Core.DataDict.DataDictionary.html)&gt;<BR>
A task that will return the completed DataDictionary when awaited.

## Remarks:
When the analyzer implements [ISourcedConnector](Pansynchro.Core.ISourcedConnector.html), it is necessary to supply a [Data Source](Pansynchro.Core.IDataSource) before calling this method.  Failing to do so will raise an exception.
