# PostSharp
[PostSharp](https://www.postsharp.net/) is an IL weaver for C#. This readme file is about PostSharp add-ins. For general information on PostSharp, see the main website.

## How does it work?
1. Add PostSharp to your project and annotate your code with [CustomAttributes].
2. The C# or VB.NET compiler builds your code into binaries.
3. PostSharp analyzes the binary and injects the implementation of aspects or add-ins.

## What are add-ins?
A PostSharp community add-in is a NuGet package that makes use of PostSharp and modifies your assembly during the compilation process. For example, the [StructuralEquality add-in](https://github.com/postsharp/PostSharp.Community.StructuralEquality) allows you to add an attribute to your classes and have `Equals` and `GetHashCode` methods automatically generated in IL so that they avoid cluttering your C# code.

This is a feature in development. Add-ins are not yet publicly available. 

## Quick start: How do I use a PostSharp add-in?
1. Find an add-in that you want to use in your project and reference its NuGet package in your project.
2. Register for a free Community edition license of PostSharp at https://postsharp.net/essentials. 
    * You will be prompted to enter your license key when you first build the project.
3. Follow the instruction in the add-in README to add the effect of the add-in to your project. 
    * Most likely, you will need to add the add-in's attribute to your assembly or some of your classes.
    * Most attributes in add-ins are multicast attributes. [How does multicasting work?](multicasting.md)

## How can I choose what namespaces/classes are affected by the add-in?
For most add-ins, you can use multicasting. [How does multicasting work?](multicasting.md)

## How can I create my own add-ins?
Copy the contents of the repository [https://github.com/postsharp/PostSharp.Community.HelloWorld] and follow the README.md file there. 

## Are add-ins maintained or supported by PostSharp Technologies?
The add-ins under [this organization](https://github.com/postsharp) are maintained by PostSharp Technologies. You can report bugs in these add-ins against their GitHub repositories and we will look into those issues. 

However, we don't offer commercial support for these add-ins. We offer commercial support for the PostSharp Aspect Framework and other PostSharp Patterns libraries. 
