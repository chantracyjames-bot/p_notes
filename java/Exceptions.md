
# Exceptions
## Java Errors
- Definition:
    - When Java encounters an error, it immediately stops the program.
    - Unlike Exceptions, it cannot be circumvented unless it's fixed.
- three types of errors
    - Compile-Time Errors
        - occurs duing compilation time
            - preventing the file from compiling properly
            - mainly due to syntax and type errors
        - common examples are:
            - missing semilcolons
                int x = 5
            - incompatible types
                boolean yes = "Hello";
            - undeclared variables
                System.out.print(myValue);
    - Runtime Errors
        - occurs after the program compiles
            - but encounters sudden crashes or unintended behaviors
        - common examples are:
            - division by zero
                int x = 10 / 0;
            - index out of bounds
                String arr[] = new String[1];
                arr[10] = "yes";
    - Logical Errors
        - occurs no Compilation Errors or Runtime Errors occur
            - the output is not accurate to what was supposed to happen
        - common examples are
            - expecting a sum but the results is a difference
                int x = 10;
                int y = 8;
                System.out.print("Sum: ", x - y);

    - how to avoid errors?
        - use meaningful variable names
            - avoid typos and spellings
        - check for missing semicolons and braces
        - read the error messages carefully
            - gives valuable information in debugging

    - debugging
        - the process of identifying and fixing errors or bugs present in a program
        - it often includes:
            - reading error messages
            - tracing program flow step by step
            - testing small pieces of code independently
        - common debugging steps:
            - printing values for each step
                - mainly used when encountering Logical Errors
                - can reveal which part of the program is failing
                - example:
                    int x = 10;
                    System.out.print(x);
                    int y = 8;
                    System.out.print(y);
            - using IDEs for debugging
                - modern Java IDEs comes with debugging tools
                    - examples: IntelliJ IDEA, Eclipse, Netbeans, etc.
                    - these are able to:
                        - add breakpoints
                            - dictates where the program ends for testing
                        - inspect variables in real time
                            - being able to see their values step by step
            - commenting 
                - using the comment // syntax to rule out problematic lines of code
                - example:
                    int x = 10;
                    // float y = "Hello"; -> Error
                    String yes = "no";
            - looking for typos
                - calling for elements can sometimes yield in mispellings ot typos
                - example:
                    int myValue = 10;
                    System.out.print(MyValue); // typo

- Java Exception
    - different types of problems and errors can occur while a program is running
        - yielding different error messages depending on the type
    - when the program encounters a roadblock or an error, Java immediately stops the program
        - it then throws an error describing the reason for stopping the program
    - unlike Errors, these types of errors are able to be circumvented
        - commonly called as Exceptions 
    - these types of errors are "predicted" and have code that runs when the program runs into that error

- Exception handling
    - Java has four keywords for Exception Handling
        - try
            - runs a block of code and "tests" it while being executed
            - any error messages will be "caught" by the catch statement
            - syntax:
                try {...}
            - example:
                try {
                    int x = 100;
                    int y = 0;
                    System.out.print(x / y); -> Error
                }
        - catch
            - runs a block of code after the Exception it is "expecting" is caught
            - can catch any Exceptions, from broad to specific
            - sidenote:
                - the catch statement can also catch Error, but is genereally unadvised
                    - Errors are a underlying problem with the program
                    - it is better to solve it to prevent futher problems
            - syntax:
                catch(<exception> <identifier>) {...}
            - example:
                catch(Exception e) {
                    System.out.print("Error encountered"); // prints when an Exception is triggered
                }
        - finally 
            - runs regardless of the result of a try-catch statement
            - runs after a try-catch
            - syntax:
                finally {...}
            - example:
                finally {
                    System.out.print("try-catch is finished");
                }
        - throw
            - used to throw Exceptions
                - can also throw Errors but is ill-adviced
            - typically used together with an exception type
            - can be used outside a try-catch statement
                - note that the program will be stopped after an Exception is thrown
            - syntax:
                throw <objectName> <exceptionClass>;
            - example:
                throw new Exception;

    - the try and catch keywords usually come in as pairs
        - with the finally statement being optional
        - syntax:
            try {...}
            catch(<exeption> <identifier>) {...}
            // optional
            finally {...}
        - example:
            try {
                int i = 10 / 0;                       // triggers the ArithmeticException error
            } catch (ArithmethicException e) {
                System.out.print(e);                  // prints after the Exception is triggered
            } finally {
                System.out.print("Program finished"); // runs after the try-catch statement is done
            }

    - multiple catch blocks are able to be declared in a try-catch statement
        - it can help in handling multiple Exceptions through custom statements
        - note that catch order matters
            - exceptins closer to the try statement runs first when triggered
            - it is by convention to declare exceptions from specific to general Exceptions
        - example:
                try {
                int arr[] = {1, 2, 3};
                arr[10] = 10;                                       // ArrayIndexOutOfBoundException
                int yes = 10 / 0;                                   // ArithmeticException
            } catch (ArithmeticException e) {
                System.out.print("arithmethic error"); 
            } catch (ArrayIndexOutOfBoundException e) {
                System.out.print("arrayindexourofbound error"); 
            } catch (Exception e) {
                System.out.print("broad exception");            // runs when previous exceptions are not triggered
            }
        - it is also possible to catch multiple exceptions in a single statement
            - it is through using the or | operator
            - it saves space by avoiding repetition
            - syntax:
                catch(<exception1> | <exception2> e) {...}
            - example:
                catch (ArithmeticException | ArrayIndexOutOfBoundsException e) {...}

    - try-with-resources
        - a special implementation of the try-catch block
            - with added support for streams
            - which it closes automatically after the end of the try block
        - syntax:
            try (<stream>) {...}
        - example:
            try (FileWriter myWriter = new FileWriter("file")) {...}
        - the catch statement is used the same way as a regular catch statement
            - for Exception handling and Error debugging
        - sample code:
            try (FileWriter myWriter = new FileWriter("file")) {
                myWriter.write("idkman");
            } catch (IOException e) {
                System.out.println("idkman"); 
            }