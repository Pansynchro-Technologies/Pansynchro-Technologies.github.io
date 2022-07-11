# IDataSink Interface

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Provides basic functionality for saving raw data to an external data store.

## Remarks

A Pansynchro [writer](Pansynchro.Core.IWriter.html) is responsible for taking data from [DataStream](Pansynchro.Core.DataStream.html)s and encoding it into an existing data format.  In some cases, such as SQL databases, where the data storage and the data format are two inseparable parts of one whole system, the writer will also manage the work of saving the data.  When this is not the case, (ie. when dealing with data in a common format such as CSV, JSON, or Parquet,) the writer will also implement [ISinkConnector](Pansynchro.Core.ISinkConnector.html) and will require a Data Sink to save the data.  This allows Pansynchro to treat data formats and data storage as two distinct problems to be solved independently of one another.  When a new Data Sink is implemented, all sink connectors should work with it automagically, and vice versa.

## Methods

| [WriteData(string)](Pansynchro.Core.IDataSink.WriteData.html) | Produces a [Stream](https://docs.microsoft.com/en-us/dotnet/api/system.io.stream) to write binary data to. |
| [WriteText(string)](Pansynchro.Core.IDataSource.WriteText.html) | Produces a [TextWriter](https://docs.microsoft.com/en-us/dotnet/api/system.io.textwriter) to write textual data to. |

## See Also

* [ISinkConnector interface](Pansynchro.Core.ISinkConnector.html)
* [IWriter interface](Pansynchro.Core.IWriter.html)
