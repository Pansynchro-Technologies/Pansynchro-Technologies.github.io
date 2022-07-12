# [DataDictionary](Pansynchro.Core.DataDict.DataDictionary.html).SaveToFile Method

## Definition

Namespace: Pansynchro.Core.DataDict<BR>
Assembly: Pansynchro.Core

Saves a data dictionary to disc.

### Signature:
```
public void SaveToFile(string filename)
```

### Parameters:
`filename` [string](https://docs.microsoft.com/en-us/dotnet/api/system.string)<BR>
The name of the file on disc.

### Remarks:
The analysis process to produce an optimized dictionary can take a long time.  Once this is done, it can be a good idea to save it so that it won't need to be repeated.
