# plotter-view-aspnet-core-angular2

> Eample project for creating view components and webapis based on aspnet core for the angular2 flavor of plotter

## Quickstart

### clone project using SourceTree

### run bash shell: cd /c/a/p/plotter-view-aspnet-core-angular2

```bash
dotnet restore
dotnet run
```

## Recipe (from scratch)

#### create project using yo aspnet

```bash
cd /c/a/p/plotter-view-aspnet-core-angular2
npm install -g yo generator-aspnet bower
yo aspnet webapi plotter-view-aspnet-core-angular2
dotnet restore
dotnet run
```

* copy contents of generated folder plotter-view-aspnet-core-angular2 up one level and delete the child folder 

![image](https://cloud.githubusercontent.com/assets/22680176/21083579/81df8fe8-bfb0-11e6-882c-bf7601d45640.png)

#### set port

In Program.cs, specify (via UseUrls) the port on which to listen

```csharp
public class Program
{
    public static void Main(string[] args)
    {
        var config = new ConfigurationBuilder()
            .AddCommandLine(args)
            .AddEnvironmentVariables(prefix: "ASPNETCORE_")
            .Build();

        var host = new WebHostBuilder()
            .UseConfiguration(config)
            .UseKestrel()
            .UseUrls("http://*:9050")
            .UseContentRoot(Directory.GetCurrentDirectory())
            .UseIISIntegration()
            .UseStartup<Startup>()
            .Build();

        host.Run();
    }
}
```

## TODO

#### enable cors

#### enable dotnet file watcher

#### install swagger tool chain

#### run swagger ui - generate swagger json

#### add swagger to web middleware to document webapi

#### run swagger ui - generate apiClient.ts

#### add component

#### call apiClient from component

## Generated Readme Content:

We've made some big updates in this release, so it’s **important** that you spend a few minutes to learn what’s new.

You've created a new ASP.NET Core project. [Learn what's new](https://go.microsoft.com/fwlink/?LinkId=518016)

## This application consists of:

*   Sample pages using ASP.NET Core MVC
*   [Bower](https://go.microsoft.com/fwlink/?LinkId=518004) for managing client-side libraries
*   Theming using [Bootstrap](https://go.microsoft.com/fwlink/?LinkID=398939)

## How to

*   [Add a Controller and View](https://go.microsoft.com/fwlink/?LinkID=398600)
*   [Add an appsetting in config and access it in app.](https://go.microsoft.com/fwlink/?LinkID=699562)
*   [Manage User Secrets using Secret Manager.](https://go.microsoft.com/fwlink/?LinkId=699315)
*   [Use logging to log a message.](https://go.microsoft.com/fwlink/?LinkId=699316)
*   [Add packages using NuGet.](https://go.microsoft.com/fwlink/?LinkId=699317)
*   [Add client packages using Bower.](https://go.microsoft.com/fwlink/?LinkId=699318)
*   [Target development, staging or production environment.](https://go.microsoft.com/fwlink/?LinkId=699319)

## Overview

*   [Conceptual overview of what is ASP.NET Core](https://go.microsoft.com/fwlink/?LinkId=518008)
*   [Fundamentals of ASP.NET Core such as Startup and middleware.](https://go.microsoft.com/fwlink/?LinkId=699320)
*   [Working with Data](https://go.microsoft.com/fwlink/?LinkId=398602)
*   [Security](https://go.microsoft.com/fwlink/?LinkId=398603)
*   [Client side development](https://go.microsoft.com/fwlink/?LinkID=699321)
*   [Develop on different platforms](https://go.microsoft.com/fwlink/?LinkID=699322)
*   [Read more on the documentation site](https://go.microsoft.com/fwlink/?LinkID=699323)

## Run & Deploy

*   [Run your app](https://go.microsoft.com/fwlink/?LinkID=517851)
*   [Run tools such as EF migrations and more](https://go.microsoft.com/fwlink/?LinkID=517853)
*   [Publish to Microsoft Azure Web Apps](https://go.microsoft.com/fwlink/?LinkID=398609)

We would love to hear your [feedback](https://go.microsoft.com/fwlink/?LinkId=518015)
