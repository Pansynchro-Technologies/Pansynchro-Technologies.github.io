# ITransformer Interface

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Provides functionality for modifying the names and contents of [data streams](Pansynchro.Core.DataStream.html).

## Remarks
One or more transformers can be inserted between the [reader](Pansynchro.Core.IReader.html) and the [writer](Pansynchro.Core.IWriter.html) in a sync job to modify the data.  Developers wishing to create their own transformers can inherit from the [StreamTransformerBase](Pansynchro.Core.StreamTransformerBase.html) class, which provides a skeleton of built-in functionality for modifying data streams.

## Methods

| [Transform(IAsyncEnumerable&lt;DataStream&gt;)](Pansynchro.Core.ITransformer.Transform.html) | Applies transformations to some or all of the data streams in a sequence. |

## See Also

* [IReader interface](Pansynchro.Core.Reader.html)
* [IWriter interface](Pansynchro.Core.IWriter.html)
