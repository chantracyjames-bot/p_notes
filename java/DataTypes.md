
# Java Data Types
- Definition:
    - Java has two types of data types: Primitive and Non-primitive.
    - Primitive data types:
        - byte
            - Stores whole numbers ranging from -128 to 127.
            - Example:
                ```
                byte myByte = 127;
                ```
        - short
            - Stores whole numbers ranging from -32,768 to 32,767.
            - Example:
                ```
                short myShort = -32768;
                ```
        - int
            - Stores whole numbers ranging from -2,147,483,648 to 2,147,483,647.
            - Example:
                ```
                int myInt = 2147483647;
                ```
        - long 
            - Stores whole numbers ranging from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807.
            - Note:
                - Using this data type requires the l or L suffix to be a valid long value.
            - Example:
                ```
                long myLong = -9223372036854775808L;
                ```
        - float
            - Stores 4 bytes of decimals ranging from 6-7 decimal places.
            - Note:
                - Using this data type requires the f or F suffic to be a valid float value.
            - Example:
                ```
                float myFloat = 3.141592f;
                ```
        - double
            - Stores 8 bytes of decimals ranging from 15-16 decimal places, decimals are automatically declared as double unless type casted.
            - Note:
                - It is optional to use the d or D suffix unless type casting from a float
            - Example:
                ```
                double myDouble = 1.23456789101112;
                ```
        - boolean
            - Stores a truth value, either a true ot false value.
            - Example:
                ```
                boolean myBool = true;
                ```
        - char
            - Stores a single character or a Unicode escape sequence.
            - Using this data type requires to be declared in single quotes ' '.
            - Example:
                ```
                char myChar = 'Y';
                ```

    - Non-primitive data types:
        - String
            - Stores an array of characters, and has methods to manipulate text values.
            - Note:
                - Using this data type requires to be declared in double quotes " ".
            - Example:
                ```
                String myString = "Hello World";
                ```
        - Classes
            - Are blueprints for objects, having their own attributes and methods.
            - String is a class, so is Scanner, LocalDate, System, etc.
            - Example:
                ```
                class MyClass {...}
                ```
        - Interfaces
            - Are blueprints for classes, part of the concept of Abstraction.
            - Example:
                ```
                interface MyInterface {...}
                ```
        - Enums
            - Stores constant (final) attributes and values.
            - Example:
                ```
                enum MyEnum {...}
                ```

    - Other data type concepts:
        - Automatic data type declaration
            - Definition:
                - Leaves it to the compiler to determince the data types or an attribute or variable, uses the _var_ keyword.
                - _var_ only works if the value the variable holds is assigned alongside it.
            - Note:
                - The data type cannot be changed after the compiler determines its type, i.e. float cannot become int after compilation.
            - Example:
                ```
                var myVar = "value"; // becomes a String
                ```
        - Scientific notation (e)
            - Definition:
                - Used to write very large or very small numbers, uses the letter e or E.
            - Example:
                ```
                double largeNum = 10e10; // same as 10 x 10^10
                // or
                float smallNum = 10e-10f; // same as 10 x 10^-10
                ```
        - Type casting
            - Definition:
                - Data types are able to be converted into another type, either widening casting or narrowing casting.
            - Widening casting
                - Definition:
                - From a smaller type to a larger type, done automatically without data loss
                - byte -> short -> char -> int -> long -> float -> double
                - Example:
                    ```
                    byte smallToLargeType = 100;
                    int largerType = smallToLargeType;
                    ```
            - Narrowing casting
                - Definition:
                    - From a larger type to a smaller type, done manually due to possible data loss.
                    - double -> float -> long -> int -> char -> short -> byte
                - Example:
                    ```
                    float largeToSmallType = 903.54f;
                    short smallerType = (short) largeToSmallType; // has to be manually type casted using (<dataType>)
                    ```