
# Algorithms
- Definition:
    - Are used to solve problems related to sorting, searching, or manipulating data strutures.
- Types of Algorithms:
    - Searching Algorithms
        - These types of algorithms are used to find certain elements inside a collection.
        - A well-known searching algorithm is called "Binary Search".
    - Sorting Algoriths
        - These types of algorithms are uses to sort collections.
        - It depends on what order the resulting collection becomes, a common order type is natural order.
    - Iteration
        - Is also another type of algorithm, used to loop through elements.
        - refer to Iteratives.md for more information about Iteratives.
## Java Algorithms
- Definition:
    - Java has various built-in helper methods for searching and sorting through collections.
    - It requires the Collections class to be import first before using any of its methods.
    - Syntax:
        ```
        import java.util.Collections;
        ```
### Searching
- Binary Search
    - Definition:
        - A commonly used searching algorithm.
        - It is used through the .binarySearch() method inside the Collections class, returning the index of the element if found.
    - Note:
        - The collection must be sorted first.
    - Syntax:
        ```
        Collections.binarySearch(<collection.Object>, <element>) 
        ```
- Maximum and Minimum Search
    - Definition:
        - It is used to find the maximum and minimum values of a collection.
        - Used through the .max() and .min() methods of the Collections class, respectively.
    - Syntax:
        ```
        Collections.min(<collectionObject>);
        // or
        Collections.max(<collectionObject>);
        ```
- Frequency Search
    - Definition:
        - It is used to query a collection about the number of times an element appears.
        - Used through the .frequency() method of the Collections class.
    - Syntax
        ```
        Collections.frequency(<collectionObject>, <element>);
        ```
- Disjoint Search
    - Definiition:
        - It compares two collections is they have no elements in common, returning a boolean value.
        - Returns true if there are no common elements between the two collections, and returns false if there are.
    - Syntax:
        ```
        Collections.disjoint(<collectionObject1>, <collectionObject2>);
        ```

### Sorting
- Natural Order
    - Definition:
        - It a common type of sorting algorithm, it sorts items alphanumerically.
        - Sorting order:
            - 0-9, then
            - A-Z, and
            - a-z
        - It can be used through the .sort() method inside the Collections class, sorting the items through natural order.
    - syntax:
        ```
        Collections.sort(<collectionObject>);
        ```
- Reverse Order
    - Definition:
        - Reverses the current order of a collecti, used through the .reverse() method inside the Collections class.
    - Note:        
        - There is another method, .reverseOrder() that is able to be used inside the .sort() method, reversing the order of the data structure.
    - Syntax:
        ```
        Collections.reverse(<collectionObject>);
        // or
        Collections.sort(<collectionObject>, Collections.reverseOrder());
        ```
- Random Order
    - Definition:
        - Randomly shuffles the elements around in a collection, used through the .shuffle() method from the Collections class.
    - Syntax:
        ```
        Collections.shuffle(<collectionObject>);
        ```
- Swap Order
    - Definition:
        - Swaps two elements inside a collection, used through the .swap() method from the Collections class.
    - Syntax:
        ```
        Collections.swap(<collectionObject>, <index1>, <index2>);
        ```
