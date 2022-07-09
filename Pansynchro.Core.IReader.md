# IReader Interface

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Provides basic connector functionality for reading data from an external source into [DataStream](Pansynchro.Core.DataStream.html)s.

## Remarks

A Pansynchro reader is responsible for interpreting data from an external source.  In some cases, such as SQL databases, where the data storage and the data format are two inseparable parts of one whole system, the reader will also manage the data access.  When this is not the case, (ie. when dealing with data in a common format such as CSV, JSON, or Parquet,) the reader will also implement [ISourcedConnector](Pansynchro.Core.ISourcedConnector.html) and will require a [Data Source](Pansynchro.Core.IDataSource) to retrieve the data.  This allows Pansynchro to treat data formats and data storage as two distinct problems to be solved independently of one another.  When a new Data Source is implemented, all sourced connectors should work with it automagically, and vice versa.

## Methods

| [ReadFrom(DataDictionary)](Pansynchro.Core.IReader.ReadFrom.html) | Loads data into a sequence of [DataStream](Pansynchro.Core.DataStream.html)s. |
| [TestConnection()](Pansynchro.Core.IReader.TestConnection.html) | A tooling-friendly method for verifying that a reader is configured properly and able to retrieve data. |

## See Also

* [IDataSource interface](Pansynchro.Core.IDataSource.html)
* [IWriter interface](Pansynchro.Core.IWriter.html)
* [ISchemaAnalyzer interface](Pansynchro.Core.ISchemaAnalyzer.html)
