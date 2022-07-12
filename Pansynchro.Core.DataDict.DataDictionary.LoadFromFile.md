# [DataDictionary](Pansynchro.Core.DataDict.DataDictionary.html).LoadFromFile Method

## Definition

Namespace: Pansynchro.Core.DataDict<BR>
Assembly: Pansynchro.Core

Reads a data dictionary saved to disc.

### Signature:
```
public static DataDictionary LoadFromFile(string filename)
```

### Parameters:
`filename` [string](https://docs.microsoft.com/en-us/dotnet/api/system.string)<BR>
The name of the file on disc.

### Returns:
[DataDictionary](Pansynchro.Core.DataDict.DataDictionary.html)<BR>
The dictionary loaded from the on-disc data.

### Remarks:
If the file does not exist, or if the file's contents do not represent a valid saved data dictionary, an exception will be thrown.
