
# Itertives
## Definition
- Commonly called as loops, running a code block until a certain condition is met.
- May it be until the loop counter reaches a certain number, the condition becomes false, etc.
- Uses a boolean value to dictate if the loop runs or stops, using loop counter values other than whole numbers will cause errors.
## Loop keywords
- break
    - The break keyword is used to stop loops, breaking a loop means ending it prematurely.
- continue 
    - The continue keyword is used to skip the current iteration, using it will end the current iteration and move on to the next
## Types of loops:
- while loop
    - Definition:
        - Runs a loop while the condition is true.
    - Note:
        - If the initial condition is false, the loop never runs.
    - Syntax:
        ```
        while (<condition>) {
            <statements>
        }
        ```
    - Example:
        ```
        while (10 > 11) {
            System.out.print("lumbago");
        }
        ```
- do-while loops
    - It is a variant of the while loop, unlike while loop, this loop runs the block of code first before checking the condition.
    - Stops when the condition becomes false.
    - Note:
        - It always runs the statements once 
    - Syntax:
        ```
        do {
            <statements>
        } while (<condition>)
        ```
    - Example:
        ```
        do {
            System.out.print("idkman");
        } while (29 < 1);
        ```
- for loops
    - Definition:
        - It is an extensive type of loop, running a loop while the condition is true.
        - Takes in three statements:
            - Statement 1:
                - Executed before the code block.
                - Usually is reserved for initializing the loop counter (or variable).
            - Statement 2:
                - Represents the condition of the loop.
                - Usually is reserve for conditional operations.
            - Statement 3:
                - Executed after the code block.
                - Usually is reserved to increment or decrement the loop counter (or variable).
    - Note:
        - If the initial condition is false, the loop never runs
    - Syntax:
        ```
        for(<statement1>; <statement2>; <ststement3>) {
            <statement>
        }
        ```
    - Example:
        ```
        for(int i = 0; i < 10; i++) {
            System.out.print("yes");
        }
- for each loop
    - Definition:
        - A variant of the for loop, used to loop through iterables.
        - i.e. iterating through arrays.
    - Note:
        - The loop variable type must match the iterable type.
    - Syntax:
        ```
        for(<dataType> <loopVariableName> : <iterable>) {
            <statement>
        }
        ```
    - Example:
        ```
        float myFloat[] = {3.13, 4.19, 5.15, 6.18};
        for(float myNum : myFloat) {
            System.out.print("no");
        }

## Iterators
- Definition:
    - Are objects that can be used to toop through collections, mainly Collection type objects like ArryaLists, HashSets, etc.
    - The term comes from "iterating" which is a technical from of looping.

- Declaration and Initialization
    - Before an Iterator object is declared, it must first be imported, it is imported from the java.util package.
        - Syntax:
            ```
            import java.util.Iterator;
            ```
    - After being imported an iterator object must be tied to a collection, calling that collection's iterator method.
        - Syntax:
            ```
            Iterator<object> <iteratorObject> = <colletionObject>.iterator();
            ````
        - Example:
            ```
            Iterator<String> myIterator = myArrayList.iterator();
            ```
        - It is possible to declare an Iterator variable using the var keyword.
            - Syntax:
                ```
                var <mapObject> = <collectionObject>.iterator();
                ```
            - Example:
                ```
                var myIterator = myArrayList.iterator();
                ```

- Access and Iteration
    - Definition:
        - An iterator can be "advanced" using a few methods.
        - The .hasNext() method returns a boolean if the object being iterated has a succeeding value, indicating whether or not the object's elements are exhausted or not.
        - Syntax:
            ```
            <iteratorObject>.hasNext();
            ```
        - Example:
            ```
            myIterator.hasNext();
            ```
    - Advacning the iterator is done through the .next() method.
        - Note:
            - An Excepttion will be thrown if the iterator goes out of bounds, similar to the Index Out Of Bounds Exception.
        - Syntax:
            ```
            <iteratorObject>.next();
            ```
        - Example:
            ```
            myIterator.next();
            ```
    - An Iterator can remove elements form a collection, it is done through the .remove() method which is typically done while inside a loop.
        - Note:
            - It is recommended to remove items using a while loop with the .next() method.
            - Removing items when in a for loop or a for-each loop will not work correctly, due to the size of the collection changing when removing items.
        - Syntax:
            ```
            <iteratorObject>.remove();
            ```
        - Example:
            ```
            myIterator.remove();
            ```