# [DataDictionary](Pansynchro.Core.DataDict.DataDictionary.html).DependencyOrder Property

## Definition

Namespace: Pansynchro.Core.DataDict<BR>
Assembly: Pansynchro.Core

A representation of the order in which streams need to be read.

## Signature
```
public StreamDescription[][] Streams { get; }
```

## Remarks

This is used by the Pansynchro framework when syncing to a SQL database with foreign key constraints that must be maintained.  The DependencyOrder property is how [readers](Pansynchro.Core.IReader.html) know in which order streams should be retrieved.
