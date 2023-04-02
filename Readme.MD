## Goals

The goal of this repository is to provide feature-rich but less boiler plate starting point for any .Net project to kick start their Blazor MAUI application.


## Features

- [x] Built on .NET 6.0
- [x] Code sepereation for Web and MAUI

## Projects

- [x] Web 
    - All Web application related files are added in this project. Built on Blazor Server architecture 
    - When Web application is started, the flow goes as below
        - Program.cs &rarr; BlazorLibrary/Pages/_Host.cshtml &rarr; BlazorLibrary/Pages/_Layout.cshtml <i>(this file refers the css in Maui/wwwroot and also Blazorlibrary/wwwroot)</i>
        - BlazorLibrary/App.Razor -> This loads BlazorLibrary.Shared.MainLayout

- [x] MAUI
    - All MAUI application related files are added in this project
    - When MAUI application is started, the flow goes as below
        - MauiProgram.cs &rarr; MainPage.xaml.cs &rarr; wwwroot/index.html <i>(this file refers the css in Maui/wwwroot/css and also Blazorlibrary/wwwroot)</i>
        - Main.razor -> This loads BlazorLibrary.Shared.MainLayout

- [x] BlazorLibrary
    - SitePages - All custom Razor Pages must be added in this folder
    - wwwroot - All custom files here that are common for web and maui; <font color=red>make sure to update the references in _Layout.cshtml and index.html </font>

- [x] ClassLibrary
    - Controller - Controllers and logic classes must goto this folder
    - Model - All Model classes must goto this folder
    - Service - All external interacting service classes must goto this folder

## License

This project is licensed with the [MIT license](LICENSE).
