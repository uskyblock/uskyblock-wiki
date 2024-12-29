The following coding guidelines must be followed for any contributions to uSkyBlock.

## Syntax
* Whitespace: Always use spaces, not tabs (tab-stops/indentation may wary from IDE to IDE, spaces wont)
* Scopes: Always use curly-braces in `if-then-else` or similar constructs.
* Curly-braces: Belong to the line of the keyword, not on a separate line. We want lines to carry meaning, a curly carries no meaning on it's own.
* Naming: Use the Java-naming-conventions, not the C# ones, meaning
  * CAPITALS: Denote **constants** (`static final` or `enum`).
  * UpperCamelCase: Denote **classes** (never variables)
  * lowerCamelCase: Denote **variables**, **fields** or **methods**. All IDEs can distinguish between the three, and methods will always have paranthesis at the end.
* Don't use * imports - it makes merging much harder

### Examples
```java
public class MyClass {
  String myField;

  public MyClass() {
  }

  public myMethodWithCamelCase(String myArg) {
    boolean myVariable = true;
    if (myVariable) {
      doSomething();
    } else {
      doSomethingElse();
      myVariable = false;    // Any decent IDE will color this assignment different
      myField = "Something"; // From this one, so no need for this.myField or _myField or m_myField.
    }
  }
}
```
