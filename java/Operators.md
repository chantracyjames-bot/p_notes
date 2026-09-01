
# Operators
## Definition:
- Operators are used to manipulate data or variables.
- Java has five main types of operators:
    1. Arithmetic
    2. Assigment
    3. Comparison
    4. Logical
    5. Precedence
## Arithmetic
- Definition:
    - The most commonly used operator for mathematical operations.
- Note:
    - To use any of the arithmetic operators, both values must be either numeric values or text values.
    - Adding a number to a string results in string concatenation.
- Types or arithmetic operators:
    - Addition (+)
        - Definition:
            - Used to add two values.
        - Example:
            ``` 
            int myNum = 10;
            myOtherNum = 15;
            sum = myNum + myOtherNum; // results to 25
            ```
    - Subtraction (-)
        - Definition:
            - Subtracts two values from one another.
        - Example:
            ``` 
            int myNum = 10;
            myOtherNum = 15;
            sum = myNum - myOtherNum; // results to -5
            ```
    - Multiplication (*)
        - Definition:
            - Multiplies two values with each other.
        - Example:
            ``` 
            int myNum = 10;
            myOtherNum = 15;
            sum = myNum * myOtherNum; // results to 150
            ```
    - Division (/)
        - Definition:
            - Divides one value by the another value.
        - Example:
            ``` 
            int myNum = 10;
            myOtherNum = 15;
            sum = myNum / myOtherNum; // results to 0 (due to it being with two integers, not float)
            ```
    - Modulus (%)
        - Definition:
            - Performs a division operation and returns the remainder.
        - Example:
            ``` 
            int myNum = 10;
            myOtherNum = 15;
            sum = myNum % myOtherNum; // results to 5
            ```
    - Increment (++)
        - Definition:
            - Increases the value by one.
        - Example:
            ``` 
            int myNum = 10;
            ++myNum;        // results to 11 or
            myNum++;        // results to 12
            ```
    - Decrement (--)
        - Definition:
            - Lowers the value by one
        - Example:
            ``` 
            int myNum = 10;
            --myNum;        // results to 9 or
            myNum--;        // results to 8
            ```

## Assigment
- Definition:
    - Used to assign values to variables.
- Types of assignment operators:
    - Assignment operator (=)
        - Definition:
            - Assigns values to variables, can also be used to initialize variables.
        - Example:
            ``` 
            int myNum = 10;
            ```
    - Addition assignment (+=)
        - Definition:
            ```
            - Used to increment (or add) a certain amount to variables.
        - Example:
            ```
            int myNum = 10;
            myNum += 10; // 20
            ```
    - Subtractiom assignment (-=)
        - Definition:
            ```
            - Used to decrement (or subtract) a certain amount to variables.
        - Example:
            ``` 
            int myNum = 10;
            myNum -= 10; // 0
            ```
    - Multiplication assignment (*=)
        - Definition:
            - Used to multiply a variables by a certain amount.
        - Example:
            ``` 
            int myNum = 10;
            myNum *= 10; // 100
            ```
    - Division assignment (/=)
        - Definition:
            - Used to divide variables by a certain amount.
        - Example:
            ``` 
            int myNum = 10;
            myNum /= 10; // 1
            ```
    - Modulo assignment (%=)
        - Definition:
            - Used to retrieve remainder values from variables.
        - Example:
            ``` 
            int myNum = 10;
            myNum %= 10; // 0
            ```
    - Bitwise AND assignment (&=)
        - Definition:
            - Used for bitwise operations, using the AND logic comparisons.
        - Example:
            ``` 
            int a = 60; // 0011 1100
            int b = 13; // 0000 1101
            a &= b;     // 0000 1100 - 12 in binary
            myNum %= 10 // 0
            ```
    - Bitwise OR assignment (|=)
        - Definition:
            - used for bitwise operations, using the OR logic comparisons.
        - Example:
            ``` 
            int a = 60;  // 0011 1100
            int b = 13;  // 0000 1101
            a &= b;      // 0011 1101 - 61 in binary
            myNum %= 10; // 0
            ```
    - Bitwise XOR assignment (^=)
        - Definition:
            - Used for bitwise operations, using the XOR logic comparisons
        - Example:
            ``` 
            int a = 60;  // 0011 1100
            int b = 13;  // 0000 1101
            a &= b;      // 0011 0001 - 49 in binary
            myNum %= 10; // 0
            ```
    - Left-shift assignment (<<=)
        - Definition:
            - Shifts the bit to the left, effectively multipling the value by 2^n.
        - Example:
            ``` 
            int myNum = 60; // 0011 1100
            myNum <<= 2;    // 1111 0000 - 240 in binary
            ```
    - Right-shift assignment (>>=)
        - Definition:
            - Shifts the bit to the right, effectively dividing the value by 2^n.
        - Example:
            ``` 
            int myNum = 60; // 0011 1100
            myNum >>= 2;    // 0000 1111 - 15 in binary
            ```

## Comparison
- Definition:
    - Used to compare two values logically.
    - returns a Boolean, either a true or a false.
- Types of comparison operators:
    - Equal To (==)
        - Definition:
            - Returns true if both values are equal, false otherwise.
        - Example:
            ``` 
            int a = 10;
            int b = 10;
            a == b; // true
            ```
    - Not Equal To (!=)
        - Definition:
            - Returns true if the values are not equal, false if they are equal.
        - Example:
            ``` 
            int a = 10;
            int b = 15;
            a != b; // true
            ```
    - Greater Than (>)
        - Definition:
            - Returns true if the value to the left if greater than the value in the right.
        - Example:
            ``` 
            int a = 10;
            int b = 5;
            a > b; // true
            ```
    - Less than (<)
            - Returns true if the value to the left if less than the value in the right.
        - Example:
            ``` 
            int a = 10;
            int b = 5;
            a < b; // false
            ```
    - Greater Than or Equal To (>=)
        - Definition
            - Returns true if the value to the left if greater than or equal to the value in the right.
        - Example:
            ``` 
            int a = 10;
            int b = 10;
            a >= b; // true
            ```
    - Less Than or Equal To (<=)
        - Definition:
            - Returns true if the value to the left if less than or equal to the value in the right.
        - Example:
            ``` 
            int a = 10;
            int b = 20;
            a <= b; // true
            ```

## Logical
- Definition:
    - Used to determine logic by combining one or more comparison operators, by chaining multiple conditions.
    - Based on the conditions, it returns either a true or false, 0 or 1, respectively.
- Types of logical operators:
            ```
    - Logical AND (&&)
        - Definition:
            - Returns true if both conditions are the true.
        - Example:
            ``` 
            15 > 10 && 25 < 30; // true
            ```
    - Logical OR (||)
        - Definition:
            - Returns true if at least one condition is true.
        - Example:
            ``` 
            10 > 15 || 25 < 30; // true
            ```
    - Logical NOT (!)
        - Definition:
            ```
            - Negates (or flips) the logical value, i.e. !(true) = false, vice versa.
        - Example:
            ``` 
            !(15 > 10 && 25 < 30); // false
            ```

## Precedence
- Definition:
    - It is the order of operations, or the PEMDAS in programming.
- Order from most important to least important:
            ```
    - Parentheses - ()
    - Multiplication, Division, Modulus - *, /, %
    - Addition, Subtraction - +, -
    - Comparison - >, <, >=, <= 
    - Equality - ==, != 
    - Logical AND - && 
    - Logical OR - ||
    - Assignment - = 

## Other Operators
- Ternary operator
    - Definition:
        - A Ternary operator is like an on the fly version of an if-else statement.
        - Mainly used to determine the value of a varible without declaring an if-else statement.
    - Syntax:
        ```
        <condition> ? <expressionIfTrue> : <expressionIfFalse>;
        ```
    - Example:
        ```
        boolean idkman = (1 == 1) ? true : false;
        ```
- Nested ternaries 
    - Definition:
        - An operator that acts like a if-else if-else statement.
    - Syntax:
        ```
        <condition> ? <expressionIfTrue> : <condition> ? <expressionIfTrue> : <expressionIfFalse>;
        ```
    - Example:
        ```
        double lumbago = (1 < 2) ? 2.13 : (3 < 2) ? 2.43 : 3.14;
        ```