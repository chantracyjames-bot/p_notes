
# File Management
## File access
- Definition:
    - Accessing files in Java requires the importing of the java.io.File class.
    - Syntax:
        ```
        import Java.io.File;
        ```
    - After importing the required class, files are now able to be assigned to variables–similar to declaraing an object of a class.
        - Syntax:
            ```
            File <variableName> = new File(<filename>);
            ```
        - Example:
            ```
            File myFile new File("General.java");
            ```
    - The File class has many methods to use when manipulating file variables.
- Methods:
    - .canRead()
        - Definition:
            - Checks whether the file is readable or not, returning a boolean value,
        - Syntax:
            ```
            <fileVariable>.canRead();
            ```
        - Example:
            ```
            myFile.canRead();
            ```
    - .canWrite()
        - Definition
            - Checks whether the file can be written to or not, returning a boolean value.
        - Syntax:
            ```
            <fileVariable>.canWrite();
            ```
        - Example:
            ```
            myFile.canWrite();
            ```
    - .createNewFile()
        - Definition:
            - Creates a new file and returns a boolean value.
            - Returns a true if the operation was successful or false if it is not.
        - Note:
            - Must be wrapped inside a try-catch block, due to it throwing a IOException if an error occurs during the file creation
        - Syntax:
            ```
            <fileVariable>.createNewFile();
            ```
        - Example:
            ```
            myFile.createNewFile();
            ```
    - .delete()
        - Definition:
            - Deletes the file, returns a boolean value if the operation was successful or not.
        - Syntax:
            ```
            <fileVariable>.delete();
            ```
        - Example:
            ```
            myFile.delete();
            ```
    - .exists()
        - Definition:
            - Checks if the file exists, returns a boolean value.
        - Syntax:
            ```
            <fileVariable>.exists()
        
            ```
        - Example:
            ```
            myFile.exists();
            ```
    - .getName()
        - Definition:
            - Retrieves the name of the file, returning a String value.
        - Syntax:
            ```
            <fileVariable>.getName();
            ```
        - Example:
            ```
            myFile.getName();
            ```
    - .getAbsolutePath()
        - Definition:
            - Retrieves the absolute path of the file, returning a String value.
        - Syntax:
            ```
            <fileVariable>.getAbsolutePath();
            ```
        - Example:
            ```
            myFile.getAbsolutePath();
            ```
    - .length()
        - Definition:
            - Queries the size of the file in bytes, returning a long value.
        - Syntax:
            ```
            <fileVariable>.length();
            ```
        - Example:
            ```
            myFile.length();
            ```
    - .list()
        - Definition:
            - Lists all files in the current directory, returns a String array.
        - Syntax:
            ```
            <dirVariable>.list();
            ```
        - Example:
            ```
            myDir.list();
            ```
    - .mkdir()
        - Definition:
            - Creates a new folder, returning a boolean value whether the operation succeded or not.
        - Syntax:
            ```
            <dirVariable>.mkdir();
            ```
        - Example:
            ```
            myDir.mkdir();
            ```

## File location
- Definition:
    - If the file is in the same folder as the program, it is same to use just the file.
    - example:
        ```
        // opening a file named "file"
        File myFile = new File("file");
        ```
    - If the file is not in the current folder. it can be accessed in two ways; either relative or absolute.
- Relative path
    - Definition:
        - It is the path that is relative to the current working directory.
        - It is the folder where the program is currently running.
        - On Unix-like systems, it is commonly denoted by "./", or the current working directory (cwd)
    - Example:
        ```
        // a file is inside a folder named "folder" in the same cwd 
        # cwd
        #  |--> MyProgram.java        // current program
        #  \--> folder
        #    \--> MyOtherProgram.java // program trying to be accessed
        // the syntax to open the file would be:
        // Unix-like
        File myFile = new File("./folder/MyOtherProgram.java");

        // Windows
        File myFile = new File(".\\folder\\MyOtherProgram.java");
        ```
    - Explanation
        ```
        -> ./                           // is the current directory
        -> ./folder                     // is a folder inside the current directory
        -> ./folder/MyOtherProgram.java // is the file trying to be accessed inside a folder inside the current directory
        ```
- Absolute path
    - Definition:
        - it is the path that starts from the root of the file system
        - C: for Windows, or any drive letter
        - / for Unix-like systems, used in Linux, macOS, etc.
    - Example:
        ```
        // in Linux, assuming program is at the default Docuemnts folder
        #  /                                                            // root
        #  |--> /home
        #  | |--> /home/user
        #  | | |--> /home/user/Documents
        #  | | | |--> /home/user/Documents/my_program.c
        #  | | | \--> /home/user/Documents/folder
        #  | | |   \--> /home/user/Documents/folder/MyOtherProgram.java // file trying to be accessed
        // the syntax to open the file would be:
        // Linux
        File myFile = new File("/home/user/Documents/folder/MyOtherProgram.java"); 

        // macOS equivalent
        FILE mac_file;
        File myFile = new File("/User/user/Documents/folder/MyOtherProgram.java"); 
        // Windows equivalent
        File myFile = new File("C\\User\\user\\Documents\\folder\\MyOtherProgram.java");
        ```
         
## File manipulation
- Creating new files
    - Definition:
        - It is done through the use of the createNewFile() method of the File class.
    - Note:
        - The method will return false if the file with the dame name is present.
    - Example:
        ```
        // inside main()
        try {                               // it must be inside a try-catch block
            File myFile = new File("file");
            myFile.createNewFile();         // creates a new file
                                            // with the name "file"
        } catch (IOException e) {
            System.out.println!("failed");  // prints an error message if the
                                            // file cannot be created 
        }
        ```
- Deleting files
    - Definition:
        - it is done through the use of the delete() method of the File class.
    - Note:
        - The delete() method can also be used to delete folders.
        - Do note that the folder (or directory) must be empty.
        - Example:
            ```
            // inside main()
            File myDir = new File("./folder");
            myDir.delete();
            ```
    - Example:
        ```
        // inside main()
        File myFile = new File("file");
        myFile.delete()
        ```

- Writing to a file
    - Definition:
        - File modification is able to be achieve through the use of the FileWriter class, which is imported from java.io.FileWriter and used for basic text file writing.
        - Syntax:
            ```
            import java.io.FileWriter;
            ```
        - after importing, it is now possible to write into files, through creating an object similar to the File class.
            - Syntax:
                ```
                FileWriter <writerVariable> = new FileWriter(<filename>);
                ```
            - Example:
                ```
                FileWriter myWriter = new FileWriter("file");
                ```
    - Note:
        - The FileWriter class takes in a second argument, dictating if it enters append mode or not.
            - Syntax:
                ```
                FileWriter <writerVariable> = new FileWriter(<filename>, <boolean>);
                ```
            - Example:
                ```
                FileWriter myWriter = new FileWriter("file", true); // turns on append mode
                ```
        - By default, without append mode, FileWriter overwrites the entire file with the .write() method is used but using append mode, FileWriter will only write to the end of the pre-existing file–instead of overwriting it, it adds on to it.
        - FileWriter can also take in a File object as an argument
            - Syntax:
                ```
                FileWriter <writerVariable> = new FileWriter(<fileVariable>, <boolean>);
                ```
            - Example:
                ```
                FileWriter myWriter = new FileWriter(myVariable, true);
                ```
    - Writing is done through the .write() method
        - Note:
            - After writing, it must be closed using the .close() method.
            - If FileWriter is not set to append mode, it will overwrite the contents of the file–deleting any previous entries.
        - Syntax:
            ```
            <writerVariable>.write(<string>);
            <writerVariable>.close();
            ```
        - Example:
            ```
            myWriter.write("idkman");
            myWriter.close();
            ```

- Reading a file
    - Definition:
        - Reading into a file is done through the Scanner class, imported from java.util.Scanner–used when only dealing with simple text files.
        - The File class must also be present in order for the Scanner class to read the file.
            - Syntax:
                ```
                import java.io.File;
                import java.util.Scanner;
                ```
        - After importing the prerequisite modules, it is now possible to read files but objects of both imported classes must be made.
            - Syntax:
                ```
                File <fileVariable> = new File(<filename>);
                Scanner <readerVariable> = new Scanner(<fileVariable>);
                // or
                File <fileVariable> = new File(<filename>);
                try (Scanner <readerVariable> = new Scanner(<fileVariable>)) {...} // try-with-resources
                ```
            - Example:
                ```
                File myFile = new File("file");
                Scanner myReader = new Scanner(myFile);            // note that Scanner must be closed after use
                // or
                File myFile = new File("file");
                try (Scanner myReader = new Scanner(myFile)) {...} // automatically closes Scanner object after use
                ```
        - The FileNotFoundException class is also imported to handle Exceptions when using the file, found in the java.io.FileNotFoundException package.
            - Syntax:
                ```
                import java.io.FileNotFoundException;
                ```
    - Example:
        ```
        import java.io.File;
        import java.io.FileNotFoundException
        import java.util.Scanner;

        // inside main()
        File myFile = new File("file");

        try (Scanner myReader = new Scanner(myFile)) {
            System.out.println(myReader.nextLine());
        } catch (FileNotFoundException e) {
            System.out.println("idkman"); 
        }
        ```

## I/O Streams
- Definition:
    - Unlike file management through the File class, it is unable to write or read files with out the FileWriter and Scanner class.
    - It can only query if the file exists, query the name or size, or create and delete files.
    - I/O Streams are move advanced than the File class due to it being able to handle both text and binary data, like images, audio, PDFs, etc.
    - Byte Streams; examples are FileInputStream and FileOutputStream.
    - Character Streams; examples are FileReader, FileWriter, BufferedReader and Bufferedriter.

- FileInputStream
    - Definition:
        - Used to read a file's contents byte by byte.
        - Using the FileInputStream class, it must first be imported, from the java.io.FileInputStream package.
            - Syntax:
                ```
                import java.io.FileInputStream;
                ```
        - Similar to the File class, an object must be created to use the class method.
            - Note:
                - The FileInputStream can also take a File object as an argument.
                - Syntax:
                    ```
                    FileInputStream <inputVariable> = new FileInputStream(<fileVariable>);
                    ```
                - Example:
                    ```
                    FIleInputStream myInput = new FileInputStream(myFile);
                    // or
                    try (FileInputStream myInput = new FileInputStream(myFile)) {...}
                    ```
            - Syntax:
                ```
                FileInputStream <inputVariable> = new FileInputStream(<file>);
                ```
            - Example:
                ```
                FIleInputStream myInput = new FileInputStream("file");
                // or
                try (FileInputStream myInput = new FileInputStream("file")) {...}
                ```
    - Reading data:
        - Definition:
            - Reading data from any file is done by storing each byte in a variable through the .read() method, and converting that byte into a character by type casting it through (char).
        - Note
            - A value of -1 indicates that the variable is at the end of file.
        - Example:
            ```
            try (FileInputStream myInput = new FileInputStream("file")) {
                int i;                                                    // used to store each raw bytes
                while((i = myInput.read()) != -1) {                       // runs it through a loop
                                                                            // storing each consequtive byte to the variable i
                    System.out.print((char) i);                           // prints each byte and casting them as a character                                    
                }
            } catch (IOExeption e) {
                System.out.println("idkman"); 
            }
            ```

- FileOutputStream
    - Definition:
        - Used to write to a file, byte by byte, using the FileOutputStream class, it must first be imported from the java.io.FileOutputStream package.
            - Syntax:
                ```
                import java.io.FileOutputStream;
                ```
        - Similar to the File class, an object must be created to use the class method
            - Syntax:
                ```
                FileOutputStream <outputVariable> = new FileOutputStream(<file>);
                ```
            - Example:
                ```
                FileOutputStream myOutput = new FileOutputStream("file");
                // or
                try (FileOutputStream myOutput = new FileOutputStream("file")) {...}
                ```

        - Note:
            - The FileOutputStream can also take a File object as an argument.
                - Syntax:
                    ```
                    FileOutputStream <outputStream> = new FileOutputStream(<fileVariable>);
                    ```
                - Example:
                    ```
                    FileOutputStream myOutput = new FileOutputStream(myFile);
                    // or
                    try (FileOutputStream myOutput = new FileOutputStream(myFile)) {...}
                    ```

            - Similar to the FileWriter class, FileOutputStream can also take in a second argument, dictating if it enters append mode or not.
            - By default, without append mode, FileOutputStream overwrites the entire file with the .write() method is used.
            - but using append mode, FileOutputStream will only write to the end of the pre-existing file, instead of overwriting it, it adds on to it.
                - Syntax:
                    ```
                    fileOutputStream <outputVariable> = new FileOutputStream(<file>, <boolean>);
                    ```
                - Example:
                    ```
                    FileOutputStream myOutput = new FileOutputStream("file", true); // turns on append mode
                    ```
    - Writing data:
        - Definition:
            - Writing data to a file is done through the .write() method.
        - Note:
            - That the output must be binary, as text is not allowed.
        - Example:
            ```
            // uses FileInputStream to copy a file
            try (FileInputStream myInput = new FileInputStream("file");           // uses the FileInputClass
                FileOutputStream myOutput = new FileOutputStream("otherFile")) { 
                int i;                                                            // used to store each raw bytes
                while ((i = myInput.read()) != -1) {                              // runs reading each byte into a loop
                myOutput.write(i);                                            // each loop, it writes the raw bytes from 
                                                                                // variable i into the output file
                                                                                // writing in binary format
                }     
            } catch (IOException) {
                System.out.println("idkman"); 
            }
            ```

- BufferedReader
    - Definition:
        - A faster version of the Scanner class. replacing it due to its faster speeds and less performance overheads.
        - Usually combined with the FileReader class. which handles the opening of files.
        - using the BuffedReader class, it must first imported, from the java.io.BufferecReader package.
            - Syntax:
                ```
                import java.io.BufferedReader;
                ```
        - using the FileWriter class as an argument
            - BufferedReade enables line by line reading at faster speeds than the Scanner class
            - syntax:
                ```
                BufferedReader <readerVariable> = new BufferedReader(new FileReader(<filename>));
                // or 
                BufferedReader <readerVariable> = new BufferedReader(new FileReader(<fileVariable>));
                ```
            - example:
                ```
                try (BufferedReader myReader = new BufferedReader(new FileReader("file"))) {...}
                ```
    - Reading data:
        - Definition:
            - Reading text line by line is done through the .readLine() method, with a similar syntax to the Scanner class.
        - Example:
            ```
            try (BufferedReader myReader = new BufferedReader(new FileReader("file"))) {
                String line;                                                             // used to store each line
                while((line = myReader.readLine()) != null) {                            // loops through each line in the file
                                                                                            // assigning each line to the line variable
                                                                                            // stops when the loop reaches the end of the file, indicated by null
                    System.out.println(line);                                            // prints each line
                }
            } catch (IOException e) {
                System.out.println("idkman"); 
            }
            ```

- BufferedWriter
    - Definition:
        - An advanced version of the FileWriter class, being able to handle large text at the same time.
        - Usually combimed with the FileWriter class, which handles the writing to files.
        - using the BufferedWriter class, it must first be imported, from the java.io.BufferedWriter package.
            - Syntax:
                ```
                import java.io.BufferedWriter;
                ```

        - Using the FileWriter class as an argument
            - Syntax:
                ```
                BufferedWriter <writerVariable> = new BufferedWriter(new FileWriter(<filename>));
                // or 
                BufferedWriter <writerVariable> = new BufferedWriter(new FileWriter(<fileVariable>));
                ```
            - Example:
                ```
                try (BufferedWriter myWriter = new BufferedWriter(new FileWriter("file"))) {...}
                ```
        - Note:
            - The FIleWriter can also take in a boolean as a second argument to toggle append mode.
    - Writing data                 
        - Writing text line by line is done though the .write() method, using the .newLine() to add a line break or new line.
        - Example:
            ```
            try (BufferedWriter myWriter = new BufferedWriter(new FileWriter("file"))) {
                myWriter.write("idkman");                                                // writes to the first line
                myWriter.newLine();                                                      // inserts a new line
                myWriter.write("idkman");                                                // writes to the second line 
            } catch (IOException e) {
                System.out.println("idkman"); 
            }
            ```