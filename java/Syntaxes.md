
# Syntax
## Statements
- Definition:
    - A statement is a single line (or many) that performs a single operation, i.e. calling a function or method, initialiazing a variable, declaring a loop, etc.
    - Every statement in java must end with a semicolon ;.
- Syntax:
    ```
    <statetemt>;
    ```
- Example:
    ```
    String myString = "Hello World"; // semicolon ends the statement
    int myNum = 28;
    ```
## Case-sensitivity
- Definition:
    - Java is case-sensitive when it comes to naming.
    - myClass and MyClass are not the same thing.
- Example:
    ```
    int myNum;
    System.out.println(MyNum); -> error
                                // MyNum does not exist
    ```
## File naming
- Definition:
    - Java is class-oriented programm this extends to how it handles its file name, the class name must match it.
    - Since this file is named General, the class name must match it.
- Syntax:
    ```
    public class <filename> {...}
    ```
- Example:
    ```
    public class Syntaxes {...}
    ```
## Numbers and Text
- Text or Strings
    - Definition
        - Text in Java must be wrapped in double quotes " ".
        - While a single character is usually wrapped in single quotes ' '.
    - Example:
        ```
        String myString = "string";
        char myChar = 'A';
        ```
- Numbers and Floating points
    - Definition:
        - Unlike strings, numbers don't need to be inside double qoutes, doing so will convert the number into a string.
        - Floating points also do not need any quotations.
    - Example:
        ```
        int myInt = 100;
        float myFloat = 27.9;
        ```
## Code Blocks
- Definition:
    - Blocks or groups of code are often encased in curly braces { }.
    - It is recommended to encase blocks of code in curly braces to group them.
    - For instance, code blocks are used in an if, else-if, else statements, and possible even in iterative statements.
    - Without a code block, only the first line will get executed as part of the statement, and the succeding lines will get ignored or get executed outside of the statements.
- Example:
    ```
    if (dayIsSunny)
        sunnyDayCount++;                            // runs if the if statement is true
        System.out.println("Today is a sunny day"); // runs regradless if the if statement if true or false
    ```
## Scope
- Definition:
    - By default, the compiler compiles code from the top to bottom, first line unitl the last line.
    - Xalling a variable that is not defined until later in the code will throu an error.
- Example:
    ```
    int sum = x + 10; -> Error
    int x = 10;       // x is declared later in the code
    ```
- Block scope
    - Definition:
        - Are statements inside a block of code, variables inside a block scope only exists inside that code block.
        - Trying to access a variable inside a block scope from the outside will through an error.
    - Example:
        ```
        void myFunc() {
            int x;      // variable only exists inside of myFunc
        }
        x = 10;         -> Error
                        // trying to access an element that is not in scope
        ```
- Loop scope
    - Definition
        - Similar to block scope, variables declared inside a loop will only exist inside that loop block.
        - Calling the variable from the outside will result in an error.
    - Example:
        ```
        while(true) {
            int x = 10; // variable only exists inside the code block
            break;
        }
        x = 100;        -> Error
        ```
## Naming Conventions
- Definition:
    - There are industry conventions when naming certain elements in java
- Attributes and Variables:
    - Usually declared in camelCase.
    - example:
        ```
        int myNum;
        String myString;
        ```
- Methods and Functions:
    - Usually declared in camelCase.
    - example:
        ```
        myMethod();
        myFunction();
        ```
- Filenames:
    - usually declared in PascalCase.
    - example:
        ```
        ./MyJavaProgram.java
        ./GeneralBasics.java
        ```
- Classes, Interfaces, and Enumerations:
    - Since classes must match the filename, it follows PascalCase.
    - Interfaces and enumerations are a type of class, following the PascalCase naming scheme.
    - example:
        ```
        class MyClass {...}
        interface MyAbstract {...}
        enum MyEnum {...}
        ```
- Constants (final) and Enum Values:
    - Since enum values are similar to final variables, both follow the SCREAMING_SNAKE_CASE.
    - example:
        ```
        final String MY_MESSAGE = "hi";
        enum MyEnum {
            IDKMAN;                     // enum value
        }
        ```