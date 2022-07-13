# Discord.OAuth2
[![NuGet](https://img.shields.io/nuget/vpre/Discord.OAuth2.svg?maxAge=2592000?style=plastic)](https://www.nuget.org/packages/Discord.OAuth2)
[![MyGet](https://img.shields.io/myget/rogueexception/vpre/Discord.OAuth2.svg)](https://www.myget.org/feed/rogueexception/package/nuget/Discord.OAuth2) 
[![Build status](https://ci.appveyor.com/api/projects/status/axedfea3b7j1l2ua?svg=true)](https://ci.appveyor.com/project/RogueException/discord-oauth2)

Middleware ASP.Net Core que permite que um aplicativo dê suporte ao fluxo de trabalho de autenticação OAuth 2.0 do Discord.

Based on [ASP.Net Core Facebook OAuth](https://github.com/aspnet/Security/tree/master/src/Microsoft.AspNetCore.Authentication.Facebook)

### Usage
```cs
services.AddAuthentication()
    .AddDiscord(x =>
    {
        x.AppId = Configuration["Discord:AppId"];
        x.AppSecret = Configuration["Discord:AppSecret"];
        x.Scope.Add("guilds");
    });
```
