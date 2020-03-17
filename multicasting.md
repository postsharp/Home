# Attribute Multicasting

This is an explanation of how [attribute multicasting](https://doc.postsharp.net/attribute-multicasting) works with respect to add-ins.

Often, PostSharp add-ins have an attribute that inherits from [MulticastAttribute](https://doc.postsharp.net/t_postsharp_extensibility_multicastattribute) like this:

```csharp
[AttributeUsage(AttributeTargets.Assembly | AttributeTargets.Class | AttributeTargets.Method)]
[MulticastAttributeUsage(MulticastTargets.Method)]
public class VirtualAttribute : MulticastAttribute
{
}
```

This means the `[Virtual]` is an attribute that applies to methods, but 
that you can annotate methods, classes or assemblies with this attribute.

If you annotate a method, it applies to that method.

If you annotate a class, it applies to all methods in that class.

If you annotate an assembly, it applies to all methods in all types in that assembly.

And then, you can also use the properties of [MulticastAttribute](https://doc.postsharp.net/t_postsharp_extensibility_multicastattribute)
to narrow down your targets more precisely. See that documentation page for the list of properties and their meaning.

Some examples:

`[assembly:Virtual(AttributeTargetTypes="regex:.*Virt.*")]` applies to all methods in classes which have "Virt" in their fully qualified name.

`[assembly:Virtual(AttributeTargetMemberAttributes = MulticastAttributes.Public)]` applies to all public methods.
