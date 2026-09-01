
# Arrays
- Definition:
    - Arrays are used to store multiple values in a single variable, instead of declaring multiple variables to store multiple values—arrays makes the process easier.
- Declaration and Initialization:
    - Arrays are declared using a data type and square brackets [].
    - Two ways to create arrays:
        - Explicit declaration
            - Definition:
                - It is possible to create arrays by directly assigning values into it.
                - Values are stored using curly braces { }, with multiple values declared using a comma-separated list.
            - Syntax:
                ```
                <dataType> <arrayName>[] = {<values>};
                // or
                <dataType> <arrayName>[] = new <dataType>[] {<values>};
                ```
            - Example:
                ```
                char myArray[] = {'i', 'd', 'k', 'm', 'a', 'n'};
                // or
                char myArray[]  new char[] {'i', 'd', 'k', 'm', 'a', 'n'};
                ```
        - Implicit declaration
            - Definition:
                - An empty array is automatically created when only the size is specified.
            - Syntax:
                ```
                <dataType>[] <arrayName> = new <dataType>[5];
                ```
            - Example:
                ```
                float myArray = new float[]; // an array with a size of 5 is created
                ```

- Access and Modification:
    - Accessing elements in the array
        - Definition:
            - The elements inside an array is accessed through the use of indices.
            - In most languages, the index number usually starts at 0—i.e. the first element has an index of 0.
            - Trying to access an index that is greater than the size of the array will result in an error.
        - Syntax:
            ```
            <arrayName>[<index>];
            ```
        - Example:
            ```
            myArray[1]; // false
            ```
    - Modifying elements in the array
        - Definition:
            - Values of an array are able to be changed, through accessing them via their index and using the = assignment operator.
        - Syntax:
            ```
            <arrayName>[<index>] = <newValue>;
            ```
        - Example:
            ```
            myArray[1] = false;
            ```
    - Querying the size of the Array
        - Definition:
            - The size of an array is obtained through the use of the .length property.
        - Syntax:
            ```
            <arrayName>.length;
            ```
        - Example:
            ```
            myArray.length; // return an integer
            ```

- Multidimensional Arrays
    - Definition:
        - Also called "nested arrays", containing arrays inside an array.
        - The elements inside a nested array can either be:
            - Mixed arrays
                - Containing both array elements and normal values.
                - example:
                    ```
                    { {1, 2, 3}, 4, 5, 6, {7, 8} }
                    ```
            - Purely arrays
                - Conatains only array elements.
                - Example:
                    ```
                    {{'a', 'b', 'c'}, {'d', 'e', 'f'}, {'q'}}
                    ```
    
    - Declaration and Initialization
        - Arrays are declared using a data type and multiple square brackets [].
        - Two ways to create arrays:
            - Explicit declaration
                - Definition:
                    - It is possible to create arrays by directly assigning values into it.
                    - Values are stored using curly braces { }, with multiple values declared using a comma-separated list.
                - Syntax:
                    ```
                    // 2D arrays
                    <dataType> <arrayName>[][] = {<values>};
                    // or
                    // 3D arrays
                    <dataType> <arrayName>[][][] = {<values>};
                    ```
                - Example:
                    ```
                    // 2D arrays
                    int myArray[][] = {{1, 2}, {3, 4}, {5, 6}};
                    // or
                    // 3D arrays
                    int myArray[][][] = {{{1, 2}, {3, 4}}, {{5, 6}}, {{7, 8}, {9, 0}}};
                    ```
            - Implicit declaration
                - Definition:
                    - An empty array is automatically created when only the size is specified.
                - Syntax:
                    ```
                    // 2D arrays
                    <dataType>[][] <arrayName> = new <dataType>[<rowSize>][<columnSize>];
                    // or
                    // 3D arrays
                    <dataType>[][][] <arrayName> = new <dataType>[<rowSize>][<columnSize>][<blockSize>];
                    ```
                - Example:
                    ```
                    // 2D arrays
                    float[][] myArray = new float[4][5]; // an array with a row size of 4 and column size of 5 is created
                    // or
                    // 3D arrays
                    float[][][] myArray = new float[4][5][6]; // an array with a row size of 4, column size of 5, and block size of 6 is created
                    ```
    
    - Access and Modification
        - Accessing elements in the array
            - Definition:
                - Accessing a nested array is done through using the index of the parent array and then the child array
                - The leftmost index is the parent array and every succeeding index is the child array
            - Syntax:
                ```
                <arrayName>[<parentIndex>][<childIndex>];
                ```
            - Example:
                ```
                // 2D array
                myArray[1][2];
                // or
                // 3D array
                myArray[1][2][3];
        - Modifying elements in the array
            - Definition:
                - The process of modifying an element in a nested array is similar to accessing normal arrays, only adding another index to represent the leaf values;
            - Syntax:
                ```
                <arrayName>[<parentIndex>][<childIndex>] = <newValue>;
                ```
            - Example:
                ```
                // 2D arrays
                myArray[1][3] = "lumbago";
                // or
                // 3D arrays
                myArray[1][2][4] = "idkman";
        - Querying the size of the array
            - Definition:
                - The size of an array inside another array can also be queried using the .length property.
            - syntax:
                '''
                <arrayName>[<parentIndex>].length;
                ```
            - Example:
                ```
                // 2D arrays
                myArray[1].length;
                // or
                // 3D arrays
                myArray[1][2].length;
                ```