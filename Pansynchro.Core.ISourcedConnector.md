# ISourcedConnector Interface

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Provides basic functionality for reading raw data from an external source.

## Remarks

A Pansynchro [reader](Pansynchro.Core.IReader.html) is responsible for interpreting data from an external source.  In some cases, such as SQL databases, where the data storage and the data format are two inseparable parts of one whole system, the reader will also manage the data access.  When this is not the case, (ie. when dealing with data in a common format such as CSV, JSON, or Parquet,) the reader will also implement ISourcedConnector and will require a [Data Source](Pansynchro.Core.IDataSource) to retrieve the data.  This allows Pansynchro to treat data formats and data storage as two distinct problems to be solved independently of one another.  When a new Data Source is implemented, all sourced connectors should work with it automagically, and vice versa.

When a reader or [analyzer](Pansynchro.Core.ISchemaAnalyzer.html) implements ISourcedConnector, it is necessary to call the [SetDataSource](Pansynchro.Core.ISourcedConnector.SetDataSource.html) method to connect a valid data source before calling any other method on the reader or analyzer.  Failing to do so will raise an exception.

## Methods

| [SetDataSource(IDataSource)](Pansynchro.Core.ISourcedConnector.SetDataSource.html) | Attaches a Data Source to a sourced connector. |

## See Also

* [IDataSource interface](Pansynchro.Core.IDataSource.html)
* [IWriter interface](Pansynchro.Core.IWriter.html)
* [ISchemaAnalyzer interface](Pansynchro.Core.ISchemaAnalyzer.html)
