# [DataStream](Pansynchro.Core.DataStream.html) Constructor (StreamDescription, StreamSettings, IDataReader)

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Initializes a new DataStream with a stream name object, settings metadata, and a data reader.

### Signature:
```
public DataStream(StreamDescription Name, StreamSettings Settings, IDataReader Reader)
```

### Parameters:
`Name` [StreamDescription](Pansynchro.Core.StreamDescription.html)<BR>
The name of the stream.

`Settings` [StreamSettings](Pansynchro.Core.StreamSettings.html)<BR>
Metadata flags containing stream settings information.

`Reader` [IDataReader](https://docs.microsoft.com/en-us/dotnet/api/system.data.idatareader?view=net-6.0)<BR>
A data reader that provides the data for the stream.
