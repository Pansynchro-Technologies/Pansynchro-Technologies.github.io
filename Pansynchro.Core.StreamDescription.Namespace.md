# [StreamDescription](Pansynchro.Core.StreamDescription.html).Namespace Property

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Represents the optional namespace of a stream.

## Signature
```
public string? Namespace { get; }
```

## Remarks

Some data sources place a namespace before the name of their data, like a namespace on a SQL table or an Avro schema.  This property represents the namespace of the stream.  If there is no namespace, it can be left null.
