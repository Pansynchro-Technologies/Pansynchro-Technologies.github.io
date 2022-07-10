# StreamDescription Class

## Definition

Namespace: Pansynchro.Core<BR>
Assembly: Pansynchro.Core

Represents the name of a stream, with an optional namespace.

## Remarks

Every stream has a name.  Some data sources also place a namespace before the name.  The StreamDescription class helps to manage the name and optional namespace of the stream.

## Constructors

| [StreamDescription(string?, string)](Pansynchro.Core.StreamDescription.ctor.html) | Initializes a new StreamDescription with an optional namespace and a name. |

## Methods

| [Parse(string)](Pansynchro.Core.StreamDescription.Parse.html) | Reads a string representation of a stream name into a StreamDescription. |

## Properties

| [Namespace](Pansynchro.Core.StreamDescription.Namespace.html) | [string?](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The namespace of the stream's name, or null. |
| [Name](Pansynchro.Core.StreamDescription.Name.html) | [string](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The name of the stream. |