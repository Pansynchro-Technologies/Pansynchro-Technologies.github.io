# [DataDictionary](Pansynchro.Core.DataDict.DataDictionary.html).CustomTypes Property

## Definition

Namespace: Pansynchro.Core.DataDict<BR>
Assembly: Pansynchro.Core

Lists any custom types defined by the source data.

## Signature
```
public Dictionary<string, FieldType> CustomTypes Streams { get; }
```

## Remarks

This is used to keep track of type aliases, enums, and specially constrained types defined in a database, so that the information contained in those types is preserved in transmission.
