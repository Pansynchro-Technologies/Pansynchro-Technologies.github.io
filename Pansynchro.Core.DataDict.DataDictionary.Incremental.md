# [DataDictionary](Pansynchro.Core.DataDict.DataDictionary.html).Incremental Property

## Definition

Namespace: Pansynchro.Core.DataDict<BR>
Assembly: Pansynchro.Core

Stores information on which streams support incremental sync and the method by which their bookmarking is kept track of.

## Signature
```
public Dictionary<StreamDescription, IncrementalStrategy> Incremental { get; }
```

## Remarks

This is used to keep track of type aliases, enums, and specially constrained types defined in a database, so that the information contained in those types is preserved in transmission.
