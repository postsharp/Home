# PostSharp add-ins

## What are add-ins?

A PostSharp  add-in is a NuGet package that makes use of PostSharp and modifies your assembly during the compilation process. For example, the [StructuralEquality add-in](https://github.com/postsharp/PostSharp.Community.StructuralEquality) allows you to add an attribute to your classes and have `Equals` and `GetHashCode` methods automatically generated in IL so that they avoid cluttering your C# code.

Unlike aspects, add-ins use the low-level API that we call *PostSharp SDK* to directly manipulate the MSIL representation of the assembly.

## Community add-ins

* [StructuralEquality](https://github.com/postsharp/PostSharp.Community.StructuralEquality): Auto-implement Equals and GetHashCode
* [ToString](https://github.com/postsharp/PostSharp.Community.ToString): Auto-implement ToString based on fields and properties
* [Packer](https://github.com/postsharp/PostSharp.Community.Packer): Make your project into a single-file .exe
* [Virtuosity](https://github.com/postsharp/PostSharp.Community.Virtuosity): Make all your methods virtual
* [DeepSerializable](https://github.com/postsharp/PostSharp.Community.DeepSerializable): A [Serializable]-like attribute that applies recursively.
* [HelloWorld](https://github.com/postsharp/PostSharp.Community.HelloWorld): Base for creating your own add-in
* [UnsafeMemoryChecker](https://github.com/postsharp/PostSharp.Community.UnsafeMemoryChecker): Warn about memory access violation in unsafe code

## Quick start: How do I use a PostSharp add-in?

Just like you would start using an aspect:

1. Find an add-in that you want to use in your project and reference its NuGet package in your project.
2. Register for a free Community edition license of PostSharp at https://www.postsharp.net/get/free. You will be prompted to enter your license key when you first build the project.
3. Follow the instruction in the add-in README to add the effect of the add-in to your project. Most likely, you will need to add the add-in's attribute to your assembly or some of your classes.

## How can I choose what namespaces/classes are affected by the add-in?

For most add-ins, you can use multicasting. [How does multicasting work?](multicasting.md)

## How can I create my own add-ins?

Copy the contents of the repository https://github.com/postsharp/PostSharp.Community.HelloWorld and follow the README.md file there. 

Most of the PostSharp SDK has API-level documentation and is available at https://doc.postsharp.net/sdk/. This documentation is also embedded in the NuGet package `PostSharp.Compiler.Engine` so it will show up in IntelliSense. 

## How can I get help?

If you're planning to release your add-in as open source, you're welcome to  [join the add-in writers Slack](https://join.slack.com/t/postsharp-addins/shared_invite/zt-efilf9t1-voOs5FYteLEcKeHvXtu9xQ) to get answers to your questions. Please note we don’t have the capacity to provide support to PostSharp SDK to all users, and will focus our help on open-source contributors. Thank you for your understanding. *(Before May 19th, the Slack link was broken. Now it works.)*

