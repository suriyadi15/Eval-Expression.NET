
Evaluate, Compile and Execute code and expression at runtime.

*From simple expression*
```csharp
int result = Eval.Execute<int>("x + y", new { x = 1, y = 2})
```
*To complex code*
```csharp
var sum = Eval.Execute(@"var list = new List<int>(x, y, z);
return list.Where(x => x > 2).Sum(x);", new { x = 1, y = 2, z = 3 });
```

![NuGet Version](https://img.shields.io/nuget/v/Z.Compiler.svg?style=flat-square)
![NuGet Version](https://img.shields.io/nuget/dt/Z.Compiler.svg?link=http%3A%2F%2Fabc.xyz&link=http%3A%2F%2Fabc.xyz)

```
PM> Install-Package Z.Compiler
```

## Eval.Execute
Evaluate and execute a code or expression and return the results.

Use Execute if you need to evaluate the expression only once.
- To execute a code once...

*Using Anonymous Class*
```csharp
int result = Eval.Execute<int>("x + y", new { x = 1, y = 2})
```

*Using Ordinal Value*
```csharp
int result = Eval.Execute<int>("{0} + {1}", x, y)
```

*Using Extension Methods*
```csharp
string s = "x + y";
int result = s.Eval<int>(new { x = 1, y = 2 });
```

## Eval.Compile
Compile the code or expression and return a delegate of type Func or Action to execute.

Use Compile if you need to evaluate the same expression more then once.
- To Evaluate property path
- To Evaluate the same expression with different parameter

```csharp
int result = Eval.Compile<Func<int>>("x + y", new { x = 1, y = 2})
```
```csharp
string code = "x + y";
var compiled = code.Compile<Func<int, int>>("x", "y");
foreach(var item in list)
{
}
```

## Free VS Pro
Limited to 50 caracters...
Limited to 2 variables...


## Support
- [Documentation](https://zzzprojects.uservoice.com/forums/327759-eval-expression-net)
- [Forum](https://zzzprojects.uservoice.com/forums/327759-eval-expression-net)
- Email: [sales@zzzprojects.com](sales@zzzprojects.com)

### More Projects

