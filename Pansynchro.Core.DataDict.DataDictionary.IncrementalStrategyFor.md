# [DataDictionary](Pansynchro.Core.DataDict.DataDictionary.html).IncrementalStrategyFor Method

## Definition

Namespace: Pansynchro.Core.DataDict<BR>
Assembly: Pansynchro.Core

Returns the incremental sync strategy for a given stream.

### Signature:
```
public IncrementalStrategy IncrementalStrategyFor(StreamDescription stream)
```

### Parameters:
`stream` [StreamDescription](Pansynchro.Core.StreamDescription.html)<BR>
The name of the stream.

### Returns:
[IncrementalStrategy](Pansynchro.Core.Incremental.IncrementalStrategy.html)<BR>
An IncrementalStrategy value representing the bookmarking method used for the stream in question.

### Remarks:
This method is preferred over accessing the [Incremental](Pansynchro.Core.DataDict.DataDictionary.Incremental.html) property directly, because it will safely return `IncrementalStrategy.None` for any stream that does not have a strategy listed.
