# PostSharp Add-Ins

## What are add-ins?

A PostSharp  add-in is a NuGet package that makes use of PostSharp and modifies your assembly during the compilation process. For example, the [StructuralEquality add-in](https://github.com/postsharp/PostSharp.Community.StructuralEquality) allows you to add an attribute to your classes and have `Equals` and `GetHashCode` methods automatically generated in IL so that they avoid cluttering your C# code.

Unlike aspects, add-ins use the low-level API that we call *PostSharp SDK* to directly manipulate the MSIL representation of the assembly.

## Quick start: How do I use a PostSharp add-in?

Just like you would start using an aspect:

1. Find an add-in that you want to use in your project and reference its NuGet package in your project.
2. Register for a free Community edition license of PostSharp at https://www.postsharp.net/get/free. You will be prompted to enter your license key when you first build the project.
3. Follow the instruction in the add-in README to add the effect of the add-in to your project. Most likely, you will need to add the add-in's attribute to your assembly or some of your classes.

## How can I choose what namespaces/classes are affected by the add-in?

For most add-ins, you can use multicasting. [How does multicasting work?](multicasting.md)

(TODO: This should move to the README of each add-in)

## How can I create my own add-ins?

Copy the contents of the repository [https://github.com/postsharp/PostSharp.Community.HelloWorld] and follow the README.md file there. 

