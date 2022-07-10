# IDataSource Interface

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Provides basic functionality for reading raw data from an external source.

## Remarks

A Pansynchro [reader](Pansynchro.Core.IReader) is responsible for interpreting data from an external source.  In some cases, such as SQL databases, where the data storage and the data format are two inseparable parts of one whole system, the reader will also manage the data access.  When this is not the case, (ie. when dealing with data in a common format such as CSV, JSON, or Parquet,) the reader will also implement [ISourcedConnector](Pansynchro.Core.ISourcedConnector.html) and will require a Data Source to retrieve the data.  This allows Pansynchro to treat data formats and data storage as two distinct problems to be solved independently of one another.  When a new Data Source is implemented, all sourced connectors should work with it automagically, and vice versa.

## Methods

| [GetDataAsync()](Pansynchro.Core.IDataSource.GetDataAsync.html) | Retrieves binary data from an external source. |
| [GetDataAsync(string)](Pansynchro.Core.IDataSource.GetDataAsync.html) | Retrieves a specific binary data stream from an external source. |
| [GetTextAsync()](Pansynchro.Core.IDataSource.GetTextAsync.html) | Retrieves text-based data from an external source. |
| [GetTextAsync(string)](Pansynchro.Core.IDataSource.GetTextAsync.html) | Retrieves a specific text-based data stream from an external source. |


## See Also

* [ISourcedConnector interface](Pansynchro.Core.ISourcedConnector.html)
* [IReader interface](Pansynchro.Core.IReader.html)
* [ISchemaAnalyzer interface](Pansynchro.Core.ISchemaAnalyzer.html)
