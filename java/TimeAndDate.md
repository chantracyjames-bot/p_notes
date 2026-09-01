
# Time and Date
## Definition
- While java does not have a built-in class for date and time, it is available through the java.time package, imported either as a single class or the whole package.
- It is used to work with the date and time.
    - java.time classes
        - LocalDate
            - represents a date
            - year, month, day
            - yyyy-MM-dd
        - LocalTime
            - represents a time
            - hour, minute, second, nanoseconds
            - HH-mm-ss-ns
        - LocatDateTime
            - represents both a date a time
            - yyyy-MM-dd-HH-mm-ss-ns
        - DateTimeFormatter
            - formatter for displaying and parsing date-time objets
### LocalDate
- Definition
    - To display the current date, it is done by importing the LocalDate class from the java.time package, using the .now() method will return the current date.
- Example:
    ```
    // inside main()
    LocalDate myObj = LocalDate.now();
    myObj;                             // current date
    ```
### LocalTime
- Definition:
    - To display the current time, it is done by importing the LocalTime class from the java.time package, using the .now() method will return the current date.
- Example:
    ```
    // inside main()
    LocalTime myObj = LocalTime.now();
    myObj                              // current time
    ```
### LocalDataTime
- Definition:
    - To display both the current date and time, it is done by importing the LocalDateTime class from the javaa.time package, using the .now() method will retrun the current data and time.
- Example:
    ```
    // inside main()
    LocalDateTime myObj = LocalDateTime.now();
    myObj;                                     // current date and time
    ```
### DateTimeFormatter
- Definition:
    - To format date and time, it is done by importing the DateTimeFormatter class from java.time package, using the .ofPattern() method will format the given date and time into a format.
    - Sample formats:
        - yyyy-MM-dd
        - dd/MM/yyyy
        - dd-MMM-yyyy
        - E, MMMM dd yyyy
- Example:
    ```
    LocalDateTime myObj = LocalDateTime.now();                                       // returns the current date time
    DateTimeFormatter myFormat = DateTimeFormatter.ofPattern("dd-MM-yyyy HH:mm:ss"); // calls the ofPatter() method
                                                                                    // uses the dd-MM-yyyy date format
                                                                                            // uses the HH:mm:ss time format
                                                                                        
                                                                                            // removes the T and nanoseconds from the original forma
            String formmattedStuff = myObj.format(formatObj);                                // uses the LocalDateTime to convert the date time to a readable format
            formattedStuff;                                                                  // 16-06-2026 12:57:39
    ```