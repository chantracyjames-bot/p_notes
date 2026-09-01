
# Conditionals
- Definition:
    - Conditional statements control the flow of the program.
    - It uses boolean as the logic with conditional operations controlling the result of the conditional statements.
    - All conditional operators must return a boolean value.
- Types of conditionl statements
    - if
        - Definition:
            - An _if_ statement only runs the code block if the condition is true.
        - Syntax:
            ```
            if (<condition>) {
                <statements> 
            }
            ```
        - Example:
            ```
            if (10 > 29) {
                System.out.print("no"); // runs since condition is true
            }
            ```
    - else if
        - Desctiption:
            - An _else if_ statement offers another condition other than the _if_ statement.
            - It has a similar syntax to the _if_ statement.
        - Syntax:
            ```
            else if (<condition>) {
                <statements>
            } 
            ```
        - Example:
            ```
            if (7 < 2) {
                System.out.print("no");  // does not run since condition is false
            }
            else if (9 > 2) {
                System.out.print("yes"); // runs since condition is true
            }
            ```
    - else
        - Definition:
            - An _else_ statement runs if all of the conditions return false.
            - If the _if_ and _else if_ statements did not run, the _else_ statement will run as a last resort.
        - Syntax:
            ```
            else {
                <statements>    
            }
            ```
        - Example:
            ``` 
            if (1 > 9) {
                System.out.print("no");    // does not run since condition is false
            }
            else {
                System.out.print("maybe"); // runs since all condition are false  
            }
            ```
    - if-else
        - Definition:
            - A combination of the _if_ and _else_ statements.
        - Example:
            ```
            if (90 == 12) {
                System.out.print("no");
            }
            else {
                System.out.print("maybe");    
            }
            ```
    - if-else if-else
        - Definition:
            - A combination of the _if_, _else if_ and _else_ statements.
        - Example:
            ```
            if (90 == 12) {
                System.out.print("no");
            }
            else if (75 != 89) {
                System.out.print("yes");
            }
            else {
                System.out.print("maybe");    
            }
            ```
    - switch-case
        - Definition:
            - An alternative approach to _if-else if-else_ statements, as it offers a clean and organized approach to conditional operations.
        - Syntax:
            ```
            switch (<expression>) {
                case <condition>:
                    <statements>
                    break;
                case <condition>:
                    <statements>
                    break;
                default:
                    <statements>
            }
            ```
        - Example:
            ```
            int num = 10;
            switch (num) {
                case num <= 9:
                    System.out.print("no");
                    break;
                case num >= 11:
                    System.out.print("yes");
                    break;
                default:
                    System.out.print("maybe");
            }
            ```
        - Note:
            - The _case_ condition is similar to the _if_ and _else if_ statements, being a conditional statement in and of itself—only running the code block if is true.
            - The _break_ statement is required to end the case statements as if it not present, it will run other case conditions instead of stopping when reaching the first true condition.
            - The _default_ condition is similar to the _else_ statement, only running if all case conditions are false.
- Nested Conditional Statements
    - Definition:
        - It is possible to nest condition statements inside of each other.
        - An _if_ statement is able to be inserted to another _if_ statement, or even in a _switch-case_.
    - Example:
        ```
        if (100 = 1) {
            if (32 < 1) {
                System.out.println("idkman");
            }
        }
        ```
- Ternary Operators
    - Description:
        - It is possible to declare a short form _if_, _else if_, and _else_ statements using a special syntax.
        - A ternary operator is like an on the fly version of an _if-else_ statement.
        - Do note that it is generally unadvised to use ternary operators when dealing with complex operations as it can lead to the code base being unreadable.
    - Short-hand if-else
        - Definition:
            - Mainly used to determine the value of a varible without declaring an if-else statement
        - Syntax:
            ```
            <condition> ? <expressionIfTrue> : <expressionIfFalse>;
            ```
        - Example:
            ```
            boolean idkman = (1 == 1) ? true : false;
            ```
    - Short-hand nested if-else
        - Definition:
            - A nested ternary operator that acts like a _if-else if-else_ statement.
        - Syntax:
            ```
            <condition> ? <expressionIfTrue> : <condition> ? <expressionIfTrue> : <expressionIfFalse>;
            ```
        - Example:
            ```
            double lumbago = (1 < 2) ? 2.13 : (3 < 2) ? 2.43 : 3.14;
            ```