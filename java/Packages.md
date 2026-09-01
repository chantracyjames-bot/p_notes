
# Packages
## Definition:
- In Java, a package is a group of classes, they differ by name to avoid naming conflicts.
- built-in packages in java is part of the Java API, is a library of prewritten classes that are free of use, included in the Java Development Environment (JDE)

## Java has two types of packages
- Built-in Packages
    - Definition:
        - These are packages that are built-in to Java.
        - e.g. Scanner, InputMismatchException. etc.
        - To import packages in Java, it is done through the import keyword
    - Note:
        - Importing is usually declared before any classes.
    - Syntax:
        - Importing a single class.
            - Syntax:
                ```
                import <packageName>.<className>;
                ```
            - Example:
                ```
                import java.time.LocalTime;
                ```
        - Importing an entire package
            - Syntax:
                ```
                import <packageName>.*;
                ```
            - Example:
                ```
                import java.util.*;
                ```

- User-defined packages
    - Definition:
        - Java uses a file system to store packages, similar to folders on a computer
    - Declaration:
        - Definition:
            - To create a package, it is done using the package keyword.
            - It must be declared before any classes.
        - Note:
            - It is generally recommended to assign lowercase names to packages to avoid name conflicts.
        - Syntax:
            ```
            package <packageName>;
            ```
        - Example:
            ```
            package mypackage;
            ```
    - Access:
        - Definition:
            - To compile or export the package, a flag in the javac terminal command is specified.
        - Note:
            - The dots . represents the current folder /.
            - Compiling with a dot in the package name will let the compiler know to nest the package.
            - Example:
                ```
                my.package -> ./my/package
                ```
        - Syntax:
            ```
            java -d . <filename>
            ```
        - Example:
            ```
            java -d . idkman
            ```