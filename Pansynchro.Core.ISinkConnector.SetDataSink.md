# [ISinkConnector](Pansynchro.Core.ISinkConnector.html).SetDataSink(IDataSink) Method

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Connects an ISinkConnector to a [data sink](Pansynchro.Core.IDataSink.html).

### Signature:
```
void SetDataSink(IDataSink sink);
```

### Parameters:
`sink` [IDataSink](Pansynchro.Core.IDataSink.html)<BR>
A Data Sink to save data from the connector to an external data store.

## Remarks:
When a [writer](Pansynchro.Core.IWriter.html) implements [ISinkConnector](Pansynchro.Core.ISinkConnector.html), it is necessary to supply a [Data Sink](Pansynchro.Core.IDataSink.html) before calling any other method on the writer.  Failing to do so will raise an exception.
