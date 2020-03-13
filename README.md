# PostSharp
[PostSharp](https://www.postsharp.net/) is an IL weaver for C#. 

## How does it work?
1. Add PostSharp to your project and annotate your code with [CustomAttributes].
2. The C# or VB.NET compiler builds your code into binaries.
3. PostSharp analyzes the binary and injects the implementation of aspects or add-ins.

## What are add-ins?
A PostSharp community add-in is a NuGet package that makes use of PostSharp and modifies your assembly during the compilation process. For example, the [StructuralEquality add-in](https://github.com/postsharp/PostSharp.Community.StructuralEquality) allows you to add an attribute to your classes and have `Equals` and `GetHashCode` methods automatically generated in IL so that they avoid cluttering your C# code.

This is a feature in development. Add-ins are not yet publicly available. 
