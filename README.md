# Serilog.Sinks.Loggr

[![Build status](https://ci.appveyor.com/api/projects/status/3k7h2rht9eyaqqg0/branch/master?svg=true)](https://ci.appveyor.com/project/serilog/serilog-sinks-loggr/branch/master)

A Serilog sink that writes events to Loggr.

[Loggr](http://www.loggr.net) is a cloud hosted solution to track users, events and other kinds of items. It provides analytics and notifications and more. Register for an account at their website and [find](http://docs.loggr.net/post#A Quick Example) your logkey and apikey. Pass those to the loggr sink using the extension.

**Package** - [Serilog.Sinks.Loggr](http://nuget.org/packages/serilog.sinks.loggr)
| **Platforms** - .NET 4.5

```csharp
var log = new LoggerConfiguration()
    .WriteTo.Loggr("<log key>", "<api key>")
    .CreateLogger();
```

As Loggr can track users, the sink will try to find a property called `UserName` and pass that to Loggr as a dedicated property. You can change the name of the property in one of the settings of the extension of the sink. The rest of the properties are being send as data elements to Loggr.
