﻿
Moving https://bitbucket.org/DimaStefantsov/unidecodesharpfork project to GitHub (Dima no longer works with .NET).
Also the goal is to port it to .net core

# Overview

**Unidecode.NET** is .NET library dll, written in C#.
It provides string or char extension method Unidecode() that returns transliterated string. It supports huge amount of languages.
And it's very easy to add your language if it's not supported already!

#Example code

Take a look at the list of assertions:
```cs
Assert.AreEqual("Bei Jing ", "\u5317\u4EB0".Unidecode());
Assert.AreEqual("Rabota s kirillitsey", "Работа с кириллицей".Unidecode());
Assert.AreEqual("aouoAOUO", "äöűőÄÖŨŐ".Unidecode());
Assert.AreEqual("Hello, World!", "Hello, World!".Unidecode());
Assert.AreEqual("'\"\r\n", "'\"\r\n".Unidecode());
Assert.AreEqual("CZSczs", "ČŽŠčžš".Unidecode());
Assert.AreEqual("a", "ア".Unidecode());
Assert.AreEqual("a", "α".Unidecode());
Assert.AreEqual("a", "а".Unidecode());
Assert.AreEqual("chateau", "ch\u00e2teau".Unidecode());
Assert.AreEqual("vinedos", "vi\u00f1edos".Unidecode());
```