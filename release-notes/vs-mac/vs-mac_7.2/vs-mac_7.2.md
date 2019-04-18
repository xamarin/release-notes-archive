---
id: 4FC92ADD-2453-4AEC-BBA2-E0851376BE2D
title: "Visual Studio for Mac 7.2 (Preview) Release Notes"
---


> ⚠️  
> View the latest Visual Studio for Mac release notes on [docs.microsoft.com](https://docs.microsoft.com/visualstudio/releasenotes/vs2017-mac-relnotes).
> 





**This is a preview of the upcoming Visual Studio for Mac 7.2 release. These previews are unsupported builds to allow developers to test the new features, and to gather feedback and bug reports. Your help is very appreciated!**

Visual Studio for Mac 7.2 primarily focuses on bug fixes and performance improvements and includes the following features.

## Docker Support

You can now publish Asp.Net Core apps to docker containers and run them from an App Service.

To enable docker support to your project, right click on your Asp.Net Core web app and `Add > Add Docker Support`.

To publish your web app to a docker container, use the `Publish > Publish to Azure` workflow introduced in Visual Studio for Mac (right click on the web app project in the `Solution Pad`). 

During publishing the following resources are created on Azure

- a container registry is created tha the Docker image is published to. Container registry requires Azure storage which will also be created.
- an App Service is created that will download the image from the container registry and run it.

During publication:

- a new docker image is created, tagged and pushed to the Azure container registry.
- the App Service downloads the new image and runs it.

Note:
* If you use an existing Resource Group, it must be in the same region as the App Service Plan you are creating.
* If you are creating a new Resource Group, you must set the Container Registry and the App Service plan to be in the same region (e.g. both must be in “West US”).
* The VM size of the App Service Plan must be `S1` or larger.

[![](images/docker-publish.png)](images/docker-publish.png)

## Xamarin Live Player (Preview)

Xamarin Live Player enables developers to continuously deploy and debug their app, straight to an iOS or Android device..

For more information visit https://xamarin.com/live.


### Known Issues

- Azure Functions: Debugging Azure Functions does not work when the project is first created. Close and reopen the project to be able to debug.

### Bugs Fixed

* Improved: Added syntax highlighting for markdown files.
* Improved: Add complication custom run configuration support.
* Fixed: Copy and pasting multi line statements into F# interactive is broken.
* Fixed: Accessibility: MAS40B: Empty "Label" for edit fields in 'Solution Options' window.
* Fixed: Unlocalized strings in Preferences dialog.
* Fixed: Failure to install blocks the IDE from closing the solution.
* Fixed: Page up/down doesn't work in code completion.
* Fixed: Dirty file interferes with creating new project.
* Fixed: Many workspace errors logged while coding.
* Fixed: VS for Mac constantly prompting for myGet credentials.
* Fixed: "Hung" tool tip causes inability to use IDE.
* Fixed: When typing a description in NuGet package Metadata the UI keeps on growing.
* Fixed: Toggling "unsafe" now requires a complete project reload to take effect.
* Fixed: [F#] Hovering a namespace results in a tooltip displayed in the wrong location.
* Fixed: Tuples tooltip has completely broken syntax.
* Fixed: Tuple tooltip uses no colours.
* Fixed: Watch window does not update tuple information on change.
* Fixed: Parentheses closing is broken when you do an if statement.
* Fixed: "ctor" code snippet is producing an nameless constructor.
* Fixed: Remove WCF 'Add a Reference' dialog when unsupported.
* Fixed: Duplicate key binding not shown in tooltip.
* Fixed: Adding package source url with extra spaces should be trimmed.
* Fixed: Numbers syntax highlighted in namespace names, method names and property names.
* Fixed: Code completion item shown with white text.
* Fixed: Triple line comments text syntax highlighted with black text.
* Fixed: Language not shown for all recently used projects in New Project dialog.
* Fixed: Searching for Microsoft.AspNet.WebApi.Client in the Add Packages dialog terminates IDE.
* Fixed: Getting build errors when first character is numeric value in android app name field with F# project.
* Fixed: Accessibility: Accessibility Inspector: MAS40B: "Label" property is empty for 'Andriod' & 'Phone' image icon in 'New Project' window.
* Fixed: Dialogs "ghost" after switching away from XS and back again.
* Fixed: UINavigationController rendering as black box in storyboard designer.
* Fixed: Designer placing labels behind image - not happening on Xcode.
* Fixed: Cannot resize Xamarin Forms Previewer window.
* Fixed: On changing the Horizontal spacing values in property panel, value of Vertical spacing in property panel also changed.
* Fixed: Projects which begin with a number produce an incorrect package name.
* Fixed: Some project templates are using the legacy _Category element.
* Fixed: Xamarin.Mac project templates not shown until Xcode installed.
* Fixed: Forms and Android project template wizards can create invalid Android package names.

## Visual Studio for Mac 7.2.0.540

* Fixed: In the Info.plist dialog the Japan, Chinese and Korea translations are shown vertically.
* Fixed: Spaces converted to tabs on paste with C# source code option to "Use default settings from 'Text file'".
* Fixed: Writing " inserts two of " characters, but delete only deletes 1 leaving one behind.
* Fixed: Duplicate "ASP.NET Core Web App" show in "New Project" template.
* Fixed: F# Forms Android project does not include FSharp.Core package.
* Fixed: Xamarin.Mac Classic API projects do not compile until solution reloaded.

## Visual Studio for Mac 7.2 Preview (7.2.0.583)

* Fixed: Closing quote missing in XAML when autocompleting.
* Fixed: Paste corrupts inserted text.
* Fixed: Device/Simulator list is disabled upon creation of new iOS project.
* Fixed: MSBuild Condition parsing has issues with function calls.
* Fixed: Default keybindings re-appear if they are removed.
* Fixed: Unable to start a .exe as an External Tool or in code via ProcessInfo.
* Fixed: Imported PackageReferences are not supported.
* Fixed: Visual Studio for Mac just shows "Execution failed" when starting Android emulator with Docker running.
* Fixed: Provisioning profiles not shown on iOS Bundle Signing page if Team is selected.
* Fixed: Debugger disconnects from Live Player after a short period of time.

