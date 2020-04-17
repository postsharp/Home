# PostSharp

## What is PostSharp?

PostSharp makes C# better so you can get back to the bright side of coding.

With PostSharp, you can eliminate the boilerplate that stems from the implementation of design patterns or features like logging or caching. The result: your code is more readable and maintainable; you can make better use of your time; and your deliverables are more reliable. 

PostSharp combines existing technologies such as aspect-oriented programming, meta-programming, IL weaving and static analysis, and takes them to the next level in a well-engineered approach.

## How does it work?

1. Instead of cluttering your source code with boilerplate, you add a few [CustomAttributes] telling the compiler what needs to be done. These custom attributes are called *aspects* and they describe how your target code should be enhanced. 

2. The C# or VB compiler builds your code into binaries as usually.

3. At build time, after the C# compiler finishes, PostSharp injects the repetitive code directly into your binaries.

PostSharp comes with a set of ready-made aspects for the most common patterns, and with a powerful toolkit so you can implement your own.

## Where can I learn more about it?

* Look at the [PostSharp.Samples](https://github.com/postsharp/PostSharp.Samples) repo. 

* Go to https://www.postsharp.net/documentation.

## What can I specifically do with PostSharp?

You can create your own aspects:
* [Method boundary aspect](https://doc.postsharp.net/method-decorator): Add code at the beginning and end of target methods
* [Method interception aspect](https://doc.postsharp.net/method-interception): Wrap target methods or replace method calls
* [Location interception aspect](https://doc.postsharp.net/location-interception): Replace accesses to fields and properties

You can use ready-made PostSharp Patterns aspects:
* [Logging](https://doc.postsharp.net/logging): Make all or target methods write traces to logs
* [NotifyPropertyChanged](https://doc.postsharp.net/inotifypropertychanged): Auto-implement smart properties
* [Contracts](https://doc.postsharp.net/contracts): Add runtime checks for arguments and return values
* [Caching](https://doc.postsharp.net/caching): Cache method return values
* *More patterns are documented at https://www.postsharp.net/.*

You can use community add-ins:
* [StructuralEquality](https://github.com/postsharp/PostSharp.Community.StructuralEquality): Auto-implement Equals and GetHashCode
* [ToString](https://github.com/postsharp/PostSharp.Community.ToString): Auto-implement ToString based on fields and properties
* [Packer](https://github.com/postsharp/PostSharp.Community.Packer): Make your project into a single-file .exe
* [Virtuosity](https://github.com/postsharp/PostSharp.Community.Virtuosity): Make all your methods virtual
* [DeepSerializable](https://github.com/postsharp/PostSharp.Community.DeepSerializable): A [Serializable]-like attribute that applies recursively.
* [HelloWorld](https://github.com/postsharp/PostSharp.Community.HelloWorld): Base for creating your own add-in
* [UnsafeMemoryChecker](https://github.com/postsharp/PostSharp.Community.UnsafeMemoryChecker): Warn about memory access violation in unsafe code

## Quick start: How can I use PostSharp in my project?

1. Find an aspect or add-in you want to use in your project and reference its NuGet package in your project. 

2. [Check out](https://www.postsharp.net/get/free) your free PostSharp Community license key. 
You will be prompted to enter your license key when you first build the project.

## How is PostSharp licensed?

There are three things: PostSharp as a product, PostSharp Community as a free product edition, and the `PostSharp.Community` namespace.

### PostSharp, the product

PostSharp is a commercial product. It includes both free and premium features, and the premium editions come with professional support. For an overview of the commercial editions, see https://www.postsharp.net/.

### PostSharp Community, the free edition of PostSharp

PostSharp Community allows for an unlimited use of all free features, plus the use of premium features on a limited number of lines of code. You can get your free license [here](https://www.postsharp.net/get/free).

### PostSharp.Community, the namespace

`PostSharp.Community` is a namespace used to herd open-source extensions to PostSharp, such as add-ins and aspect libraries. 

The extensions under the `PostSharp.Community` namespace are curated by PostSharp Technologies, but we don't necessarily own all intellectual rights on these extensions, nor do we guarantee the same level of quality or support as on PostSharp itself.

Some projects in the `PostSharp.Community` namespace were ported from [Fody](https://github.com/Fody),
an open-source IL weaver for .NET.

## How can I create my own aspect?

### Option 1. Use PostSharp Framework

By far the easiest and most powerful way to create an aspect is to use PostSharp Framework and create an aspect, for instance by deriving a new class from `OnMethodBoundaryAspect` or `MethodInterceptionAspect`. See https://doc.postsharp.net/custom-aspects for details.

PostSharp Framework is a supported product of commercial quality. Many of its features are included for free in PostSharp Community.

### Option 2. Build an add-in with PostSharp SDK

If what you need cannot be done with a PostSharp Framework, or if an aspect cannot reach your performance requirements, you can build a PostSharp add-in using the low-level APIs of PostSharp, called PostSharp SDK.

Unlike PostSharp Framework, PostSharp SDK is neither supported, documented, nor of commercial quality. But since it's the API we're using to build PostSharp Framework, we're pretty confident it works well.

It takes several months for a newly-hired PostSharp developer to become proficient in PostSharp SDK. If it does not sound scary to you, [go for it](addin.md).

[More about PostSharp add-ins](addin.md)

## How do I get my aspect or add-in listed here?

Contact us at hello@postsharp.net.
