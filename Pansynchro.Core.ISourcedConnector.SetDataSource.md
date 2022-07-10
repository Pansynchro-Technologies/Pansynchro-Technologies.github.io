# [ISourcedConnector](Pansynchro.Core.ISourcedConnector.html).SetDataSource(IDataSource) Method

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Connects an ISourcedConnector to a [data source](Pansynchro.Core.IDataSource.html).

### Signature:
```
void SetDataSource(IDataSource source);
```

### Parameters:
`source` [IDataSource](Pansynchro.Core.IDataSource.html)<BR>
A Data Source to retrieve data for the connector to read.

## Remarks:
When a [reader](Pansynchro.Core.IReader.html) or [analyzer](Pansynchro.Core.ISchemaAnalyzer.html) implements [ISourcedConnector](Pansynchro.Core.ISourcedConnector.html), it is necessary to supply a [Data Source](Pansynchro.Core.IDataSource.html) before calling any other method on the reader or analyzer.  Failing to do so will raise an exception.
