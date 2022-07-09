# ISchemaAnalyzer Interface

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Provides functionality for analyzing a source of data to produce a [DataDictionary](Pansynchro.Core.DataDict.DataDictionary.html).

## Remarks

A Pansynchro analyzer is responsible for gathering metadata about an external source.  In some cases, such as SQL databases, where the data storage and the data format are two inseparable parts of one whole system, the analyzer will also manage the data access.  When this is not the case, (ie. when dealing with data in a common format such as CSV, JSON, or Parquet,) the analyzer will also implement [ISourcedConnector](Pansynchro.Core.ISourcedConnector.html) and will require a [Data Source](Pansynchro.Core.IDataSource) to analyze the data.  This allows Pansynchro to treat data formats and data storage as two distinct problems to be solved independently of one another.  When a new Data Source is implemented, all sourced connectors should work with it automagically, and vice versa.

## Methods

| [AnalyzeAsync(string)](Pansynchro.Core.ISchemaAnalyzer.AnalyzeAsync.html) | Analyzes the data to produce a [DataDictionary](Pansynchro.Core.DataDict.DataDictionary.html). |
| [Optimize(DataDictionary, Action&lt;string&gt;)](Pansynchro.Core.ISchemaAnalyzer.Optimize.html) | Attempt a more in-depth analysis to determine metadata that can improve on-the-wire sync performance. |

## See Also

* [IDataSource interface](Pansynchro.Core.IDataSource.html)
* [IReader interface](Pansynchro.Core.Reader.html)
* [IWriter interface](Pansynchro.Core.IWriter.html)
