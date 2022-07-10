# [StreamDescription](Pansynchro.Core.StreamDescription.html).Parse(string) Method

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Reads a string representation of a stream name into a [StreamDescription](Pansynchro.Core.StreamDescription.html).

### Signature:
```
public static StreamDescription Parse(string name)
```

### Parameters:
`name` [string](https://docs.microsoft.com/en-us/dotnet/api/system.string) <BR>
The name of the stream.

### Returns:
[StreamDescription](Pansynchro.Core.StreamDescription.html)<BR>
A new StreamDescription representing this name.

## Remarks:
This method creates a StreamDescription from a name string, correctly handling namespace setup when one or more dots appear in the name.
