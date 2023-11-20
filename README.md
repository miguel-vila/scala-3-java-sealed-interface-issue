## Scala 3 - Java sealed interface issue

In a codebase with both scala 3 and a java sealed interface, the scala 3 compiler will fail to compile with errors:

```
[error] 3 |public sealed interface TestInterface permits TestFoo {
[error]   |              ^^^^^^^^^
[error]   |              illegal start of type declaration
```

and

```
[error] 3 |record TestFoo() implements TestInterface {
[error]   |                            ^^^^^^^^^^^^^
[error]   |                            Not found: type TestInterface
```
