# NickBuhro.Translit

C# library for cyrillic-latin transliteration.

The current version of the library is also [available on NuGet](https://www.nuget.org/packages/NickBuhro.Translit).

## Features

It implements transliteration by 
[ISO 9](https://en.wikipedia.org/wiki/ISO_9) 
([ГОСТ 7.79—2000](https://ru.wikipedia.org/wiki/ISO_9#.D0.93.D0.9E.D0.A1.D0.A2_7.79.E2.80.942000)) 
on System B (only for slavik languages).

Both direction transliteration is supported:
* cyrillyc to latin
* latin to cyrillyc

It could be specified concrete language from list:
* Russian
* Belorussian
* Ukrainian
* Bulgarian
* Makedonian

## Usage

``` C#

// Cyrillic to latin example

var latin = Transliteration.CyrillicToLatin("Предками данная мудрость народная!", Language.Russian);
Console.WriteLine(latin);	// Output: Predkami dannaya mudrost` narodnaya!

// Latin to cyrillic example

var cyrillic = Transliteration.LatinToCyrillic("Predkami dannaya mudrost` narodnaya!", Language.Russian);
Console.WriteLine(cyrillic);	// Output: Предками данная мудрость народная!

```

## Compatibility

The library uses no references except for `System` - it has no external dependencies.
It is cross compiled to:

* .NET Framework 3.5 Client Profile
* .NET Framework 4.0 Client Profile
* .NET Framework 4.5
* .NET Platform 5.4