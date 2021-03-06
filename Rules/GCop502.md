﻿# GCop502

> *"The parameter '{ParameterName}' doesn't seem to be used in this method. Consider removing it. If the argument must be declared for compiling reasons, rename it to contain only underscore character."*


## Rule description
Unused parameters just increase code length and reduce readability of code, so it is better to avoid using them.

There are cases where the argument must remain for the method signature to comply with an interface or an overriden base method. In those cases, to make it clear that the argument is not used, name it as _ or __ or ___ depending on how many such unused arguments exist.

## Example 1
```csharp
public void MyMethod(MyClassObject myProperty)
{
    ...
    //myProperty is Not used in the method body
}
```
*should be* 🡻

```csharp
public void MyMethod()
{
    ...
}
```

*Or if the parameter must remain* 🡻

```csharp
public void MyMethod(MyClassObject _)
{
    ...
}
```
