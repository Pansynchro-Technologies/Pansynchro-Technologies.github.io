# ISinkConnector Interface

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Provides basic functionality for writing raw data to an external source.

## Remarks

A Pansynchro [writer](Pansynchro.Core.IWriter.html) is responsible for taking data from [DataStream](Pansynchro.Core.DataStream.html)s and encoding it into an existing data format.  In some cases, such as SQL databases, where the data storage and the data format are two inseparable parts of one whole system, the writer will also manage the work of saving the data.  When this is not the case, (ie. when dealing with data in a common format such as CSV, JSON, or Parquet,) the writer will also implement ISinkConnector and will require a [Data Sink](Pansynchro.Core.IDataSink) to save the data.  This allows Pansynchro to treat data formats and data storage as two distinct problems to be solved independently of one another.  When a new Data Sink is implemented, all sink connectors should work with it automagically, and vice versa.

When a writer implements ISinkConnector, it is necessary to call the [SetDataSink](Pansynchro.Core.ISinkConnector.SetDataSink.html) method to connect a valid data sink before calling any other method on the writer.  Failing to do so will raise an exception.

## Methods

| [SetDataSink(IDataSink)](Pansynchro.Core.ISinkConnector.SetDataSink.html) | Attaches a data sink to a sink connector. |

## See Also

* [IDataSink interface](Pansynchro.Core.IDataSink.html)
* [IWriter interface](Pansynchro.Core.IWriter.html)
