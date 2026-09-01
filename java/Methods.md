
# Methods
## Built-in Method~s
### main()
- the main method in Java
- it is the entry point of the program
    - this is where the statements are first read and executed

### System class methods
- .print()
    - Definition:
        - Prints text to the screen, using the stdout call.
    - Syntax:
        ```
        System.out.print(<value>);
        ```
    - Example:
        ```
        System.out.print("Hello World"); // Hello World
        ```
- .println()
    - Definition:
        - Prints text to the screen, and adds a new line after each statement.
    - Syntax:
        ```
        System.out.println(<value>);
        ```
    - Example:
        ```
        System.out.println("Hello World"); // Hello World\n
        ```
### String class methods
- .charAt()
    - Definition:
        - Queries the character at a specified index of a String, returning a char value corresponding to that index in the String.
    - Syntax:
        ```
        <string>.charAt(<index>);
        ```
    - Example:
        ```
        "idkman".charAt(1); // 'd'
        ```
- .codePointAt() 
    - Definition:
        - Queries the Unicode code of a character at a specified index of a String, returns an int value that is able to be casted as a char value.
    - Syntax:
        ```
        <string>.codePointAt(<index>);
        ```
    - Example:
        ```
        "idkman".codePointAt(1);    // 100
        ```
- .codePointBefore()
    - Definition:
        - Queries the Unicode code of a character before a specific index of a String, returns an int value that is able to be casted as a char value
    - Syntax:
        ```
        <string>.codePointBefore(<index>);
        ```
    - Example:
        ```
        "idkman".codePointBefore(1); // 106
        ```
- .codePointCout()
    - Definition:
        - Queries the numnber of Unicode characters found inside a String, requires an start index and end index.
        - Returns an int representing the amount of Unicode characters.
    - Note
        - The end index is exclusive and the start index is inclusive.
    - Syntax:
        ```
        <string>.codePointCount(<startIndex>, <endIndex>);
        ```
    - Example:
        ```
        "idkman".codePointBefore(0, 6); // 6
        ```
- .compareTo()
    - Definition:
        - Used to compare two String values by their lexicography, positive values indicate that the first String is greater that the second String
        - Uses either in Unicode value or number of Unicode characters.
    - Note
        - If the Unicode value is higher, the difference between it and the corresponding Unicode character at the same index in the second String is given.
            - Example: 'F' and 'A', 'F' is higher than 'A' by 4, so it returns 4
        - If the number of Unicode characters is higher, it will return the difference between the size of the first and second String if and only if the Strings are identical except the excess Unicode values.
            - Example: 'idkmmm' and 'idk', 'idkmmm' has 3 more values than 'idk', so it returns 3
        - Negative values indicate that the second String is greater than the first String, either in Unicode value or number of Unicode characters.
            - If the Unicode value is higher, the difference between it and the corresponding Unicode character at the same indec in the first String is given.
                - Example; 'A' and 'a', 'A' is lower than 'a' by 32, so it returns -32
            - If the number of Unicode characters is higher, it will return the difference between the size of the first and second String if and only if the Strings are identical except the excess Unicode values.
                - Example; 'lumbago' and 'lumbagooo', 'lumbago' has 2 less values than 'lumbagooo', so it returns -2
        - This method runs through the Strings from left to right, and any values String values after the first mismatch is discarded.
            - Example; 'lumbago' and 'idkman', the first letters are compared, 'l' and 'i' while the others are ignored
    - Syntax:
        ```
        <string1>.compareTo(<string2>);
        ```
    - Example:
        ```
        "lumbago".compareTo(idkman); // 3
        ```
- .compareToIgnoreCase()
    - Definition:
        - The same method as the .compareTo() method, comaparing two Strings lexicograpically, the only difference is that this method ignores case-sensitive differences.
        - i.e. does not take into consideration if both values differ in casing or not.
    - Syntax:
        ```
        <string1>.compareToIgnoreCase(<string2>);
        ```
    - Example:
        ```
        "Hello".compareToIgnoreCase("hello"); // 0
        ```
- .concat()
    - Definition:
        - Used to concatinate strings together, an alternative to the + operator returning a combined String value.
    - Syntax:
        ```
        <string1>.concat(<string2>);
        ```
    - Example:
        ```
        "idk".concat("man"); // "idkman"
        ```
- .contains()
    - Definition:
        - Queries if the String contains a specific sequence of characters.
        - returns a true if the value is present, returns a false if not.
    - Syntax:
        ```
        <string>.contains(<charSequence>);
        ```
    - Example:
        ```
        "lumbago".contains("bag"); // true
        ```
- .contentEquals()
    - Definition:
        - Compares a String to a StringBuffer or a CharSequence object, similar to the .equals() method.
    - Syntax:
        ```
        <string>.contentEquals(<stringBuffer>);
        // or
        <string>.contentEquals(<charSequence>);
        ```
    - Example:
        ```
        "Hello World".contentEquals("Hello World"); // true
        ```
- .copyValueOf()
    - Definition:
        - Returns a String from an array of characters.
        - i.e. turns a specific portion of a char[] into a String value.
    - Note:
        - This method requires a start index and a end index.
        - The end index is exclusive, and the start index is inclusive.
    - Syntax:
        ```
        <string>.copyValueOf(<char[]>), <startIndex>, <endIndex>;
        ```
    - Example:
        ```
        char[] charArray = {65, 66, 67, 68};                     // {'A', 'B', 'C', 'D'}
        String myString = myString.copyValueOf(charArray, 0, 4); // "ABCD"
        ```
- .endsWith()
    - Definition:
        - Queries if a given String ends with a certain sequence of characters.
        - Returning true if the String ends with the given characters. returns false if no.
    - Syntax:
        ```
        <string1>.endsWith(<string2>);
        ```
    - Example:
        ```
        "idkman".endsWith("man"); // true
        ```
- .equals()
    - Definition:
        - Compares two String values and returns true if both values are the same, returns false if otherwise.
    - Note:
        - Unlike the .contentEquals() method, this method strictly requires only Strings.
    - Syntax:
        ```
        <string1>.equals(<string2>);
        ```
    - Example:
        ```
        "idk".equals("idk"); // true
        ```
- .equalsIgnoreCase()
    - Definition:
        - Similar to the .equals() method, only that this method ignores case-sensitive strings.
        - i.e. does not consider UpperCase and lowercase characters.
    - Syntax:
        ```
        <string1>.equalsIgnoreCase(<string2>);
        ```
    - Example:
        ```
        "yippee".equalsIgnoreCase("YIPPEE"); // true
        ```
- .format()
    - Definition:
        - similar to the .printf() method, but instead of printing, it returns a String value.
        - Returns a formatted String value.
    - Note:
        - The first argument of this method must be a String of format specifiers.
    - Syntax:
        ```
        String.format(<formatSpecifier>, <string>);
        ```
    - Example:
        ```
        String.format("%d %s", 10, tem);
        ```
- .getBytes()
    - converts a String into an array of bytes
    - returns a bytes[] value
    - Syntax:
        ```
        <string>.getBytes()
        ```
    - Example:
        ```
        "ABCD".getBytes(); // {65, 66, 67, 68}
- .getChars()
    - Definition:
        - Copies a part of a String into a char array, returning a char[] value.
    - Note
        - This method requires a start and end index.
            - The end index is exclusive.
            - Start index is inclusive.
        - This method also requires a position index.
            - Dictates where to start to write the copied characters, and this value is inclusive.
    - Syntax:
        ```
        <string>.getChars(<startIndex>, <endIndex>, <charArray>, <position>);
        ```
    - Example:
        ```
        char[] maybe = {'l', 'u', 'm', 'b', 'a', 'g', 'o'};
        "idkman".getChars(3, 6, maybe, 4);                  // lumbman
        ```
- .hashCode()
    - Definition:
        - Returns the hash code of a string.
    - Formula:
        $ s[0]*31^(n-1) + s[1]*31^(n-2) + ... + s[n-1] $
        - Where:
            - s[i] is the ith character of the string.
            - n is the length of the string.
            - ^ indicates exponentiation.
    - Syntax:
        ```
        <string>.hashCode();
        ```
    - Example:
        ```
        "idkman".hashCode(); // -1193258838
        ```
- .intern()
    - Definition:
        - Returns a canonical representation of a String object
        - A reference of that String in the String Pool
    - Note:
        - If that String is not present, then it adds it and returns that address
        - If it is, then returns that address .
    - Syntax:
        ```
        <string>.intern()
        ```
    - Example:
        ```
        "idkman".intern(); // memory address of "idkman" from the String Pool
        ```
- .indexOf()
    - Definition:
        - Finds the index of the first occurence of a specified substring in a String, starting from the start of the String.
        - Returns an int value denoting the starting index of the located value
    - Note:
        - A substring is a required argument, which can be a String or char value.
        - It also takes an optional second argument, a starting index to for the method to start the search–this index is inclusive and in .indexOf(), the index moves to the right.
    - Syntax:
        ```
        <string>.indexOf(<substring>, <startIndex>);
        // or
        <string>.indxcOf(<substring>);
        ```
    - Example:
        ```
        "Hello World".indexOf('o'); // 4
        ```
- .isEmpty()
    - Definition:
        - Queries if the String is empty or not, due note that whirespace is not empty space.
    - Note:
        - This method returns a boolean value.
        - Returns a true if the String is empty, returns false if not.
    - Syntax:
        ```
        <string>.isEmpty();
        ```
    - Example:
        ```
        "idkman".isEmpty(); // false
        ```
- .join()
    - Definition:
        - Joins two or more CharSequence or String elements into one single String value, uses a separator to separate the joined Strings.
        - Returns a String value consisting of String values joined and separated by a separator.
    - Syntax:
        ```
        String.join(<separator>, <charSequence>);
        // or 
        String.join(<separator>, <iterable>);
        ```
    - Example:
        ```
        String.join(" ", "idkman", "lumbago"); // "idkman lumbago"
        111
- .lastIndexOf()
    - Definition:
        - Finds the index of the first occurence of a specified substring in a String, starting from the end of the String.
        - Returns an int value denoting the starting index of the located value.
    - Note:
        - A substring is a required argument, which can be a String or char value
        - It also takes an optional second argument, a starting index to for the method to start the search–this index is inclusive. In .lastIndexOf(), the index moves to the left.
    - Syntax:
        ```
        <string>.lastIndexOf(<substring>, <startIndex>);
        // or
        <string>.lastIndexOf(<substring>);
        ```
    - Example:
        ```
        "Hello World".lastIndexOf('o'); // 7
        ```
- .length()
    - Definition:
        - Queries the length of a string object.
        - Returns an int value, coninciding with the size of a String.
    - Syntax:
        ```
        <string>.length();
        ```
    - Example:
        ```
        "idkman".length(); // 6
        ```
- .matches()
    - Definition:
        - Compares a String to a regular expression, requiring a regex value as an arguement.
        - Results into a boolean which returns a true if the String matches the regex value, returns false if not.
        ```
    - Example:
        ```
        "idkman".matches("idkman|lumbago"); // true
        ```
- .offsetByCodePoints()
    - Definition:
        - Returns an index of a String which has bee offset byt a specified number of code points.
        - Emojis and other special characters require two characters in memory.
    - Note:
        - This method requires a starting index and an offset index.
        - The starting index dictates what index of a String to start reading.
        - The offset index dictates the number of charactes to offset by, skipping characters which take up two character slots.
        - Some code points require two characters in memory to store, needing to offset the index to read the correct index.
    - Syntax:
        ```
        <string>.offsetByCodePoints(<index>, <offset>);
        ```
    - Example:
        ```
        "idk😭man".offsetByCodePoints(2, 2); // 3
                                                // starts at index 2, 'k'
                                                // offset by 2 characters
                                                // since 😭 is an emoji, it takes two slots
                                                // 'm' is a normal character, taking one slot
                                                // 2 + 1 = 3
        ```
- .regionMatches()
    - Definition:
        - Compares two regions of two String values if they match, requiring the starting index of both regions of the two Strings.
        - the first index being the starting index of the first String, and the second being the starting index of the second String.
        - Results into a boolean value that returns a true if the specified regions match, returns false if not.
    - Note:
        - This method has an optional boolean value, toggling case-sensitive mode or not.
        - Requires a length value, indicating the length of the region to compare.
    - Syntax:
        ```
        <string1>.regionMathces(<boolean>, <string1Index>, <string2>, <string2Value>, <length>);
        // or
        <string1>.regionMatches(<string1Index>, <string2>, <string2Index>, <length>);
        ```
    - Example:
        ```
        "idkman".regionMatches(4, "lumbago", 4, 1); // true
                                                    // String region a = "a"
                                                    // String region b = "a"
        ```
- .replace()
    - Definition:
        - This method replaces all occurences of a specified char value in a String value, uses a char as a search value
        - Returns a String wherein the replaced characters are present
    - Note:
        - A char value for both a search and replacement value is required.
    - Syntax:
        ```
        <string>.replace(<search>, <replacement>);
        ```
    - Example:
        ```
        "idkman".replace('d', (char) 0); // "ikman"
        ```
- .replaceAll()
    - Definition:
        - Replaces all occurenhces of a specified substring in a String value, uses a regular expression as a search value.
        - Returns a String wherein the replaced substrings are present
    - Note:
        - A regex value and a replacement String value is required.
    - Syntax:
        ```
        <string>.replaceAll(<regex>, <replacement>);
        ```
    - Example:
        ```
        "idkman".replaceAll("i|a", "o"); / "odkman";
        ```
- .replaceFirst();
    - Definition:
        - Replaces the first occurence of a specified substring in a String value, using a regular expression as a search value.
        - Returns a String wherein the replaced substring is present
    - Note
        - A regex value and a replacement String value is required.
    - Syntax:
        ```
        <string>.replaceFirst(<regex>, <replacement>);
        ```
    - Example:
        ```
        "idkman".replaceFirst("idk", "ik"); // "ikman"
        ```
- .split()
    - Definition:
        - Splits the String value into an array of subtrings, using a regular expression as the separator.
        - Returns a String[] value.
    - Note:
        - A regex value is required. returning the remainder of the String into the end of the array.
        - This method has an optional second argument, an int value representing the limit to how many splits are done and the remaining string that is not split is stored at the end of the array.
    - Syntax:
        ```
        <string>.split(<regex>, <limit>);
        ```
    - Example:
        ```
        "idkman".split("k"); {"id", "man"}
        ```
- .startsWith()
    - Definition:
        - Queries if a given String starts with a certain sequence of characters.
        - Returns true if the String starts with the given characters, and returns false if not.
    - Syntax:
        ```
        <string1>.startsWith(<string2>)
        ```
    - Example:
        ```
        "idkman".startsWith("idk"); // true
        ```
- .subSequence()
    - Definition:
        - Returns a CharSequence object from a String value.
    - Note:
        - Requires both a start index and end index.
        - Do note that the end index is exclusive, start index is inclusive.
    - Syntax:
        ```
        <string>.subSequence(<startIndex>, <endIndex>);
        ```
    - Example:
        ```
        "idkman".subSequence(0, 3);
        ```
- .substring()
    - Definition:
        - Returns a subtring from a String value.
    - Note:
        - Requires a start index.
        - The end index is optional but if not present, returning a substring from the starting index until the end of the String.
        - The end index is exclusive, and start value if inclusive.
    - Syntax:
        ```
        <string>.substring(<startIndex>, <endIndex>);
        ```
    - Example:
        ```
        "idkman".substring(3, 6); // "man"
        ```
- .toCharArray()
    - Definition:
        - Converts a string value into a char array, returning a char[] value.
    - Syntax:
        ```
        <string>.toCharArray();
        ```
    - Example:
        ```
        "idkman".toCharArray(); // {'i', 'd', 'k', 'm', 'a', 'n'}
        ```
- .toLowerCase()
    - Definition:
        - Converts a String value into its lowercase variamts, Returns a String value of lowercase characters.
    - Syntax:
        ```
        <string>.toLowerCase();
        ```
    - Example:
        ```
        "LUMBAGO".toLowerCase(); // "lumbago"
        ```
- .toString()
    - Definition:
        - Used to allow code that is treating the String as a more generalized object, in order to know its string value without casting it to String type.
        - Returns a String value into itself.
    - Syntax:
        ```
        <string>.toString();
        ```
    - Example:
        ```
        "idkman".toString(); // "idkman"
        ```
- .toUpperCase()
    - Definition:
        - Converts a String value into its UpperCase variants, returns a String value of UpperCase characters.
    - Syntax:
        ```
        <string>.toUpperCase();
        ```
    - Example:
        ```
        "idkman".toUpperCase(); // "IDKMAN"
        ```
- .trim()
    - Definition
        - Removes whitespace from the start and end of a String, returning a String with the removed whitespace.
    - Syntax:
        ```
        <string>.trim()
        ```
    - Example:
        ```
        "   idkman   ".trim(); // "idkman"
        ```
- .valueOf()
    - Definition:
        - Converts non-String values into a String representation, returning a String value.
    - Syntax:
        ```
        String.valueOf(<value>);
        ```
    - Example:
        ```
        String.valueOf(100); // "100"
        ```
### Math class methods
- .abs()
    - Definition:
        - Finds the absolute value.
        - i.e. converts the number into a positive number.
        - Returns a positive double, float, int or long value.
    - Syntax:
        ```
        Math.abs(x);
        ```
    - Example:
        ```
        Math.abs(-10); // 10
        ```
- .addExact()
    - Definition:
        - Adds two value, returnng a long or an int value.
    - Note:
        - This method throws a ArithmeticException if the sum causes an overflow.
    - Syntax:
        ```
        Math.addExact(x, y);
        ```
    - Example:
        ```
        Math.addExact(1, 1); // 2
        ```
- .cbrt()
    - Definition:
        - Performs a cube root operatiom, returning a double value.
    - Syntax:
        ```
        Math.cbrt(x);
        ```
    - Example:
        ```
        Math.cbrt(27); // 3
        ```
- .ceil()
    - Definition:
        - Rounds a number to the nearest next integer, returning a double value.
    - Syntax:
        ```
        Math.ceil(x);
        ```
    - Example:
        ```
        Math.ceil(3.14); // 4.0
        ```
- .copySign()
    - Definition:
        - Copies the sign of the second argument and places it on the first, returning double or a float value.
    - Syntax:
        ```
        Math.copySign(x, y);
        ```
    - Example:
        ```
        Math.copySign(-1, 4); // 1
        ```
- decrementExact()
    - Definition:
        - Returns exactly one integer less than the argument
    - Note:
        - This method returns an long or an int value and throws an ArithmeticException if an overflow occurs.
    - Syntax:
        ```
        Math.decrementExact(x);
        ```
    - Example:
        ```
        Math.decrementExact(1); // 0
        ```
- .floor()
    - Definition:
        - Rounds a number to the nearest preceding integer.
    - Syntax:
        ```
        Math.floor(x);
        ```
    - Example:
        ```
        Math.floor(2.72); // 2.0
        ```
- .floorDiv()
    - Definitin:
        - Performs a division operation between two arguments, and then rounds the quotient down.
        - Thie method returns a long or an int value.
    - Syntax:
        ```
        Math.floorDiv(x, y);
        ```
    - Example:
        ```
        Math.floorDiv(10, 3); // 3
        ```
- .floorMod()
    - Defintion:
        - Performs a division operation between two arguements, and then returns the modulo of the remainder rounded up.
        - This method returns a long or an int value.
    - Syntax:
        ```
        Math.floorMod(x, y);
        ```
    - Example:
        ```
        Math.floorMod(10, 3); // 1
        ```
- .incrementExact()
    - Definition:
        - Returns exactly one integer more than the argument.
    - Note:
        - This method returns a long or an int value, throws an ArithmeticException if an overflow occurs.
    - Syntax:
        ```
        Math.incrementExact(x);
        ```
    - Example:
        ```
        Math.incrementExact(1); // 2 
        ```
- .max()
    - Definition:
        - Queries the highest value between two values, returning either a double, float, int, or long value.
    - Syntax:
        ```
        Math.max(x, y);
        ```
    - Example:
        ```
        Math.max(9, 5); // 9
        ```
- .min()
    - Definition:
        - Queries the lowest value between two values, returning either a double, float, int or long value.
    - Syntax:
        ```
        Math.min(x, y);
        ```
    - Example:
        ```
        Math.min(9, 5); // 5
        ```
- .multipleExact()
    - Definition:
        - Returns the exact product between two arguements.
    - Note:
        - This method returns a long or an int value, and throws an ArithmeticException if an overflow occurs.
    - Syntax:
        ```
        Math.multiplyExact(x, y);
        ```
    - Example:
        ```
        Math.multiplyExact(1, 1); // 1
        ```
- .negateExact()
    - Definition:
        - Returns the exact number but in the opposite sign (domain).
    - Note:
        - This method returns a long or an int value, and throws an ArithmeticException if an overflow occurs.
    - Syntax:
        ```
        Math.negateExact(x);
        ```
    - Example:
        ```
        Math.negateExact(Integer.MIN_VALUE); -> Error
        ```
- .nextAfter()
    - Definition:
        - Finds the next floating point number in the direction of the second argument, returns a double or float value.
    - Syntax:
        ```
        Math.nextAfter(x, y);
        ```
    - Example:
        ```
        Math.nextAfter(1f, 2f); // 1.0000001
        ```
- .nextDown()
    - Definition:
        - Finds the next floating point number in the negative direction, returns a double or float value.
    - Syntax:
        ```
        Math.nextDown(x);
        ```
    - Example:
        ```
        Math.nextDown(1); // 0.99999994
        ```
- .nextUp()
    - Definition:
        - Finds the next floating point number in the positive direction, returning a double or float number.
    - Syntax:
        ```
        Math.nextUp(x);
        ```
    - Example:
        ```
        Math.nextUp(1); // 1.0000001
        ```
- .pow()
    - Definition:
        - Raises a number to a power with the first argument being the base and the second argument being the exponent.
    - Syntax:
        ```
        Math.pow(x, y);
        ```
    - Example:
        ```
        Math.pow(3, 2); // 9
        ```
- .random()
    - Definition:
        - Returns a double ranging from 0.0 to 1.0.
    - Note:
        - 0.0 is inclusive, and 1.0 is exclusive.
    - Syntax
        Math.random();
        ```
    - Example:
        ```
        Math.random(); // 0.00 to 0.99 
        ```
- .rint()
    - Definition:
        - Rounds a number to the nearest integer, returning a double value.
    - Note
        - If the both integers are equally as far (0.5), the method returns the nearest even number.
    - Syntax:
        ```
        Math.rint(x);
        ```
    - Example:
        ```
        Math.rint(1.5); // 2   
        ```
- .round()
    - Definition:
        - Rounds a number to the nearest integer.
    - Syntax:
        ```
        Math.round(x);
        ```
    - Example:
        ```
        Math.round(0.6); // 1
        ```
- .scalb()
    - Definition:
        - Performs the mathemetical operation of x*2^y, with the first argument being the base and the second argument being the exponent of 2.
    - Note:
        - This method returns a double or a float value.
    - Syntax:
        ```
        Math.scalb(x, y);
        ```
    - Example:
        ```
        Math.scalb(3.0, 3.0); // 24.0
        ```
- .signum()
    - Definition:
        - Queries the sign of the number.
    - Note:
        - This method returns a double or a float only if:
            - -1 if the number is negative.
            - 1 if the number is positive.
            - 0 if the number is exactly zero.
    - Syntax:
        ```
        Math.signum(x);
        ```
    - Example:
        ```
        Math.signum(10); // 1.0
        ```
- .sqrt()
    - Definition:
        - Performs a square root operation.
    - Syntax:
        ```
        Math.sqrt(x);
        ```
    - Example:
        ```
        Math.sqrt(9); // 3
        ```
- .subtractExact()
    - Definition:
        - Subtracts two values.
    - Note:
        - This method returns a long or an int value, and throws a ArithmeticException if the difference causes an overflow.
    - Syntax:
        ```
        Math.subtractExact(x, y);
        ```
    - Example:
        ```
        Math.subtractExact(1, 1); // 0
        ```
- .toIntExact()
    - Definition:
        - Converts a long value to an int value.
    - Note:
        - This method returns an int value, and throws a ArithmeticException if the result causes an overflow.
    - Syntax:
        ```
        Math.toIntExact(x);
        ```
    - Example:
        ```
        Math.toIntExcat(10L); // 10
        ```
- .ulp()
    - Defintion:
        - Returns the unit of least precision of a number, with larger numbers having lower precision.
    - Note:
        - This method returns a double or long value, and doubles are more precise than floats.
    - Syntax:
        ```
        Math.ulp(x);
        ```
    - Example:
        ```
        Math.ulp(1); // 2.220446049250313E-16~
        ```

## User-defined methods
### Definition
- Paves the way for the creation of custom methods.
- User-defined methods are designed by the programmer.
### Declaration and definition
- Methods are made to either have a return type or not.
- No return type:
    - Syntax:
        ```
        <staticOrDefault> void <methodName>() {
            <statements>
        }
        ```
    - Example:
        ```
        static void greeterMethod() {
            System.out.print("Hello");
        }
        ```
- With return type:
    - Note:
        - When a return types is declared, the method must return a value, a compilation error occurs when there is no return value and the return value must be the same type as the return type declared.
        - The return type can be any of the primitive data types, including arrays .
        - Any code that is declared after the return value won't be run, once the program reaches a return value, it will jump back to the main program and ignoring any code after it.
    - Syntax:
        ```
        <staticOrDefault> <returnType> <methodName>() {
            <statements>
            return <value>;
        }
        ```
    - Example:
        ```
        static String idkman() {
            return "lumbago";
        }
        ```

### Methods with parameters
- Definition:
    - Methods that requires an input of data.
- Note:
    - The variable that is declared in the parameter is a temporary variable.
    - It disappears after the method is finished.
- Syntax:
    ```
    <staticOrDefault> <returnType> <methodName>(<parameters>) {
        <statements>
        <returnValueIfAny>
    }
    ```
- Example:
    ```
    void myMethod(int x) {
        return x;
    }
    ```
- Multiple parameters:
    - Definition:
        - It is possible to declare multiple parameters.
    - Syntax:
        ```
        void lumbago(float yes, char no) {
            System.out.print("maybe");
        }
        ```

### Access and method calls
- Definition:
    - Methods are accessed using the method name followed by parentheses ().
- Syntax:
    ```
    <methodName>();
    ```
- Example:
    ```
    // inside main()
    idkman();

### Method calls with arguments
- Definition:
    - Variables and values are able to be passed as arguments.
    - If a method needs certain parameters, that is called "argument".
    - Calling methods with parameters requires the corresponding arguments.
- Syntax:
    ```
    <methodName>(<arguments>);
    ```
- Example:
    ```
    myMethod(19);
- Multiple arguments
    - Definiion:
        - When there are multiple arguments needed. the order of parameters matter.
        - If the order of arguments doesn't match the order of parameters, an error occurs.
    - Example:
        ```
        // assuming myMethod(int x, float y)
        int a = 10;
        float b = .13;
        myMethod(a, b);
        meMethod(b, a); -> Error
        ```

### Method Overloading
- Definition:
    - Multiple methods can have the same name if they have different return types or paramenters.
    - It is also a form of Polymorphism.
- Syntax:
    ```
    <returnType1> <methodName>(<parametersIfAny>) {
        <arguments>
    }
    <returnType2> <methodName>(<parametersIfAny>) {
        <arguments>
    }
    ```
- Example:
    ```
    void idkman(String world) {
        System.out.print("Hello" + world);
    }    
    int idkmain(int man) {
        return mam;
    }
    // inside main()
    // calling the overloaded method
    idkman("Hello"); // valid
    idkman(10);      // valid
    111

### Recursions
- Definition:
- It is the act of a method calling upon itself.
- It is generally recommended to add a halting condition otherwise, it will go into an infinite loop or JVM will return recursion limit error.
- Example:
    ```
    static int factorial(int num) {
        if(num > 0) {
            return num * factorial(num -1);
        } else {
            return num;    
        }
    }
    ```