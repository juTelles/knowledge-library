# .NET environment and IDEs

## IDE
  Integrated Development Environment

## Visual Studio
* Main and most used IDE for .NET
* Supports C#, C++, Python, Node.js, Unity and mobile

#### Advantages
* Has a free version
* Rich and detailed Debugging tool
* Available for Windows and Mac
* Has several functionalities to help the development of .NET applications

#### Disadvantages
* Not available for Linux
* Bad performance, demands a lot of resources from the machine

## Visual Studio Code (VS Code)
  * Not the same tool as Visual Studio
  * It's not actually an IDE, is a code editor, where you can install extensions that make it behave as a IDE
  * Code editor used to facilitate development in several languages

#### Advantages
* Completely free and open-source
* Supports any languages, but will need specific extensions to have certain functionalities (for example, you are using python, you need to install a specific extension to have the auto-complete functionality)
* Possibility of installing and building several extensions
* Available for Windows, Linux and Mac
* Good performance, doesn’t not use much of the machine's resources

#### Disadvantages
* A initial configuration is needed
* Some functionalities are not very intuitive

## Rider
* An IDE for .NET
* Is even more complete than Visual Studio

#### Advantages
* Rich in functionalities
* Strong integration with .NET (Deploy, Build..)
* Easiness to work with Unity
* Has code refactoring recommendations
* Has shortcuts and commands that increase productivity

#### Disadvantages
* Not free
* Bad performance, demands a lot of resources from the machine

## Using .NET in VS Code

### Install .NET SDK
  Download and install the desired version of .NET SDK directly from the [official Microsoft Website](https://dotnet.microsoft.com/pt-br/download)

### Install VS Code
  Download and install the desired version of VS Code directly from the [official VS Code Website](https://code.visualstudio.com/)

### Necessary extensions to install on VS Code
* C# Dev Kit (Microsoft) - official C# extension

### Recommended extensions to install on VS Code
* C# Extensions (JosKreativ) - facilitates classes creation
* vscode-icons (vsCODE) - icon visual improver

### Making a new .NET project
With VS Code opened in the folder where you want to create the project, open a new terminal and use the command:

```dotnet new console```
