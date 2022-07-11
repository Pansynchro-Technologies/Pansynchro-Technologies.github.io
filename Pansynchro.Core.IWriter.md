# IWriter Interface

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Provides basic connector functionality for reading data to an external destination.

## Remarks

A Pansynchro writer is responsible for taking data from [DataStream](Pansynchro.Core.DataStream.html)s and encoding it into an existing data format.  In some cases, such as SQL databases, where the data storage and the data format are two inseparable parts of one whole system, the writer will also manage the work of saving the data.  When this is not the case, (ie. when dealing with data in a common format such as CSV, JSON, or Parquet,) the writer will also implement [ISinkConnector](Pansynchro.Core.ISinkConnector.html) and will require a [Data Sink](Pansynchro.Core.IDataSink.html) to save the data.  This allows Pansynchro to treat data formats and data storage as two distinct problems to be solved independently of one another.  When a new Data Sink is implemented, all sink connectors should work with it automagically, and vice versa.

## Methods

| [Sync(IAsyncEnumerable<DataStream>, DataDictionary)](Pansynchro.Core.IWriter.Sync.html) | Writes out the data from a sequence of [DataStream](Pansynchro.Core.DataStream.html)s. |

## See Also

* [IDataSink interface](Pansynchro.Core.IDataSink.html)
* [IReader interface](Pansynchro.Core.IReaderer.html)
* [ISchemaAnalyzer interface](Pansynchro.Core.ISchemaAnalyzer.html)
