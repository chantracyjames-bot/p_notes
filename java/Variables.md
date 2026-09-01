
# Java Variables
- Definition:
    - Variables are containers for storing data (or values).
- Declaration and Initialization:
    - Definition:
        - To declare a variable, the data type and the name of the variable is required. Refer to DataTypes.md for more information about data types in Java.
        - Rules for variable declaration:
            - Variables must have a name
                - It is not possible to declare a variable without a name, trying to do so results in an error.
                - Example:
                    ```
                    String = "test"; -> Error
                    ```
            - Variable names can use letters, numbers*, underscores _ or dollar signs $.
                - *Do note that variable names cannot start with a number.
                - Example:
                    ```
                    float 123myNum; -> Error
                    ```
            - Variable names must not contain any special characters.
                - Examples are @, #, %, ~, etc.
            - Variable names must start with either a letter, an underscore _ or a dollar sign $.
            - Variable names cannot use reserved names.
                - Examples are int, float, classes, String, etc.
            - Variable must be declared with a type, as declaring a variable without a data type results in an error.
                - Example:
                    ```
                    myVar = "idk"; -> Error
                    ```
        - Conventions in naming variables
            - In Java, camelCase is the preferred method of naming variables adn attribues
                - Example: myVar, floatValue, currentTemperature, etc.
            - Variable names must match their purpose, as it makes reading variable easy to understand.
                - Example: myNum, varSum, etc.
    - Syntax:
        ```
        <dataType> <variableName>;
        ```
    - Example:
        ```
        int myNum;
        float yes;
        String HelloWorld;
        ```

    - It is possible to declare a value alongside the variable.
        - Note that the value to assign to a variable must match the variable type
        - Syntax:
            ```
            <dataType> <variableName> = <value>;
            ```
        - Example:
            ```
            char myChar = 'I';
            ```

    - It is possible to declare more than one variable in a single statement.
        - Note that the it is only possible to declare multiple variables with the same data type.,
        - Syntax:
            ```
            <dataType> <variable1Name>, <variable2Name>, <variable3Name>;
            ```
        - Example:
            ```
            String testString, tryString, yesString;
            ```

    - It is also possible to declare values alongside the variables in a multi-variable declaration.
        - Syntax:
            ```
            <dataType> <variable1Name> = <variable1Value>, <variable2Name> = <variable2Value>;
            ```
        - Example:
            ```
            String myString = "Hello World", myString = "idkman", kjakyuih = "lumbago";
            ```

- Access and Modification
    - Definition:
        - The values of a variable are accessible through calling their name.
        - Syntax:
            ```
            <variableName>;
            ```
        - Example:
            ```
            myFloat; // 3.14
            ```
    - Using the same concept, it is possible to change the values of a variable.
        - Syntax:
            ```
            <variableName> = <newValue>;
            ```
        - Example:
            ```
            myFloat = 1.11;
            ```
        - Note:
            - Changing the value of a variable to a value that does not match the declared type is not allowed, doing so result in an error
                - Example: 
                    ```
                    myFloat = "idkman"; -> Error
                    ```
            - It is not possible to change the type of a variable once it have been assigned to one, doing so resuls in an error.
                - Example
                    ```
                    int myNum;
                    float myNum; -> Error
                    ```

    - It is possible to set (or declare) the value of variable equal to another, only if they are the same data type.
        - syntax:
            ```
            <dataType> <variable1Name> = <variable2Name>;
            ```
        - example:
            ```
            String myString = myText;
            ```

- Constants (final)
    - Definition:
        - These are variables that is unmodifiable, i.e. the values are stuck or cannot be changed.
        - The variable effectively becomes read-only, similar to the const keyword in C/C++.
        - Uses the final keyword to be declared.
        - Convention:
            - When naming constant (final) variables, it is recommended to be in SCREAMING_SNAKE_CASE
            - Example:
                ```
                final int NUM1 = 1, NUM2 = 2;
                ```
    - Syntax:
        ```
        final <dataType> <variableName> = <value>;
        ```
    - Example:
        ```
        final char CHAR = 'A';
        ```
    - Note:
        - A value must be declared alongside the final variable.
        - If a final variable is declared without a value, an error occurs
        - example:
            ```
            final int NUM; -> Error
            ```

- Wrapper Classes
    - Definition:
        - Certain classes in Java requires an input of object, where primitive data types are not allowed here.
            - Example:
            ArrayList<int> myInt = new ArrayList<int>();         -> Error
            // instead
            ArrayList<Integer> myInt = new ArrayList<Integer>(); // valid
        - Java has wrapper classes, converting from a primitive data type to a class object.
        - It also has object methods converts the wrapper object into its primiive counterpart.
    - Types of Wrapper Classes:
        ```
        Type        Wrapper Class   Object Methods
        byte        Byte            .byteValue()
        short       Short           .shortValue()
        int         Integer         .intValue()
        long        Long            .longValue()
        float       Float           .floatValue()
        double      Double          .doubleValue()
        boolean     Boolean         .booleanValue()
        char        Character       .charValue()
        ```

    - Note:
        - To create wrapper objects of primitive data types, they are declared the same way but instead of the primitive type decalration—the wrapper class is used instead.
            - Syntax:
                ```
                <wrapperClass> <objectName> = <value>;
                ```
            - Example:
                ```
                Integer myInt = 100;
                Double myDouble = 3.14;
                Character myChar = 'Y';
                ```
        - It is possible to convert wrapper objects to primitive types, it is through using their respective object methods.
            - Syntax:
                ```
                <objectName>.<objectMethod>();
                ```
            - Wxample:
                ```
                myInt.intValue();
                myDouble.doubleValue();
                myChar.charValue();
                ```
        - It is also possible to convert a wrapper object into a string, it is through the .toString() method—useful for using String methods on wrapper objects
            - Syntax:
                ```
                <objectName>.toString();
                ```
            - Example:
                ```
                myInt.toString();
                myDouble.toString();
                myChar.toString();
                ```