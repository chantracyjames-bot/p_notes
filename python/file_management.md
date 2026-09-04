
# File Management
- File access
	- Definition:
		- Accessing files in python is done through the _open()_ function.
	- Syntax:
		```
		open(<filename>, <file_mode>)
		```
	- The function has four files modes:
		- _r_
			- Definition:
				- Read mode.
				- Opens a file for reading, the default value of the _open()_ function,.
			- Note:
				- The function throws an error if the file does not exist when accessing it through read mode.
			- Syntax:
				```
				open(<filename>, "r")
				```
			- Example:
				```
				open("my_file.txt", "r")
				```
		- _w_
			- Definition:
				- Write mode.
				- Opens a file for writing, creating a new file if it does not exist.
			- Note:
				- This flag overwrites the entire file when writing.
			- Syntax:
				```
				open(<filename>, "w")
				```
			- Example:
				```
				open("my_file.txt", "w")
				```
		- _a_
			- Definition:
				- Append mode.
				- Opens a file for appending, writing any changes to the end of the file.
				- creates a new file if it does not exist.
			- Note:
				- Unlike the write flag, this mode does not truncate or reset the file.
			- Syntax:
				```
				open(<filename>, "a")
				```
			- Example:
				```
				open("my_file.txt", "a")
				```
		- _x_
			- Definition:
				- Create mode.
				- Creates a file with the specified name.
			- Note:
				- The function throws an error if the file already exists.
			- Syntax:
				```
				open(<filename>, "x")
				```
			- Example:
				```
				open("my_file.txt", "x")
				```
	- Note:
		- The function also takes two more arguments, determining the mode that the content is displayed.
	- Access modes:
		- _t_
			- Definition:
				- Text mode.
				- Opens the file as a text, the default mode.
			- Syntax:
				```
				open(<filename>, "<file_mode>t")
				```
			- Example:
				```
				open("my_file.txt", "wt") # opens the file to write text
				```
		- _b_
			- Definition:
				- Binary mode.
				- Opens the file in binary, used for images and other file formats.
			- Syntax:
				```
				open(<filename>, "<file_mode>b")
				```
			- Example:
				```
				open("my_file.txt", "rb") #> opens the file to read binary
				```

- File location
	- Relative path
		- Definition:
			- It is the path that is relative to the current directory, where the program is currently at in the file system.
			- i.e. it is the folder where the program is currently running.
			- On Unix-like systems, it is commonly denoted by "./", or the current working directory (cwd).
		- Note:
			- If the file is in the same folder as the program, it is same to use just the file name.
				- Example:
					```
					// opening a file named "file"
					file = open(file)
					```
		- Example:
			```
			// a file is inside a folder named "folder" in the same cwd
			 cwd
			  |--> my_program.py // current program
			  \--> folder
			  \--> my_other_program.py // program trying to be accessed
			
			// the syntax to open the file would be:
			// Unix-like
			file = open("./folder/my_other_program.py")
			
			// Windows
			file = open(".\\folder\\my_other_program.py")
			```
		- Explanation
			- _./_
				- Is the current directory.
			- _./folder_ 
				- Is a folder inside the current directory.
			- _./folder/my_other_program.py_ 
				- Is the file trying to be accessed inside a folder inside the current directory.
	- Absolute path
		- Definition:
			- It is the path that starts from the root of the file system.
				- _C:_ for Windows, or any drive letter.
				- _/_ for Unix-like systems, like in Linux, macOS, etc.
		- example:
			```
			// in Linux, assuming program is at the default Docuements folder
			 / // root
			 |--> /home
			 | |--> /home/user
			 | | |--> /home/user/Documents
			 | | | |--> /home/user/Documents/my_program.py
			 | | | \--> /home/user/Documents/folder
			 | | | \--> /home/user/Documents/folder/my_other_program.py // file trying to be accessed
			
			// the syntax to open the file would be:
			// Linux
			file = open("/home/user/Documents/folder/my_other_program.py")
			
			// macOS equivalent
			file = open("/User/user/Documents/folder/my_other_program.py")
			
			// Windows equivalent
			file = open("C\\User\\user\\Documents\\folder\\my_other_program.py")
			```

- File manipulation
	- Creating new files
		- Definition:
			- It is done through the use of the create file mode of the _open()_ function.
		- Syntax:
			```
			open(<filename>, "x")
			```
		- Example:
			```
			open("my_file.txt", "x")
			```
		- Note:
			- If the file already exists, the function will throw an error.
			- Files can also be created using the write or append mode of the _open()_ function.
				- Syntax:
					```
					open(<filename>, "w")
					#> or
					open(<filename>, "a")
					```
				- Example:	
					```
					open("my_file.txt", "w")
					#> or
					open("my_file.txt", "a")
					```
	- Reading a file
		- Definition:
			- It is done through the use of the read file mode of the _open()_ function.
		- Syntax:
			```
			open(<filename>, "r")
			```
		- Example:
			```
			open("my_file.txt", "r")
			```
		- Reading contents:
			- Definition:
				- Reading part of a file is done through certain methods.
			- _.read()_
				- Definition:
					- Reads a certain number of characters.
				- Syntax:
					```
					<file_variable>.read(<number>)
					```
				- Example:
					```
					file.read(5) #> reads five characters inside the file
					```
			- _.readline()_
				- Definition:
					- Reads a whole line.
				- Syntax:
					```
					<file_variable>.readline()
					```
				- Example:	
					```
					file.readline()
					```
				- Note:
					- Each succeeding use of this function will read the next lines.
			- _.readlines()_
				- Definition:
					- Reads the every single line.
				- Syntax:
					```
					<file_variable>.readlines()
					```
				- Example:
					```
					file.readlines()
					```

	- Writing to a file
		- Definition:
			- Done through the use of the write file or append file mode of the _open()_ function.
		- Syntax:
			```
			open(<filename>, "w")
			#> or
			open(<filename>, "a")
			```
			- example:
			```
			open("my_file.txt", "w")
			#>
			open("my_file.txt", "a")
			```
		- Write mode:
			- Note:
				- Using this mode is destructive, as it overwrites the files contents before writing into it.
				- i.e. erases everything before writing new contents.
		- Append mode:
			- Note:
				- Unlike write mode, this mode does not erase the existing contents of a file, only appending the content it writes
				- i.e. add the new content to the end of the file
		- Writing contents:
			- Definition:
				- Writing to a file is done through certain methods.
			- _.write()_
				- Definition:
					- Writes a single string or entry.
				- Syntax:
					```
					<file_variable>.write(<string>)
					```
				- Example:
					```
					file.write("lumbago")
					```
			- _.writelines()_
				- Definition:
					- writes multiple lines or a list of strings.
				- Syntax:
					```
					<file_variable>.writelines(<string_list>)
					```
				- Example:
					```
					file.writelines(["idkman", "lumbago"]) #> adding newlines \n will write each entry to a separate line instead being on the same line
					```
			- _.flush()_
				- Definition:
					- Used to guarantee that the file is written without closing the file.
					- This method ensures that the internal buffer gets flushed out.
					- i.e. Python will tell the system to write the contents without closing the file first.
				- Syntax:
					```
					<file_variable>.flush()
					```
				- Example:
					```
					file.flush()
					```
				- Note:
					- This method is usually used after writing to a file without closing it yet.
			- _.truncate()_
				- Definition:
					- Used to truncate the file, or used to shrink it to a certain number of bytes.
					- It truncates the file to the set number of bytes that the argument takes.
				- Syntax:
					```
					<file_variable>.truncate()
					```
				- Example:
					```
					file.truncate(10) #> truncates the file to 10 bytes
										 #> any text after ten bytes is deleted
					```
				- Note:
					- The default number of bytes that this method take is the current pointer position.
					- i.e. if the pointer is at position 25, the _.truncate()_ method truncates the file to 25 bytes.
	- Closing the file
		- Definition:
			- After a file has been used or been tampered with, it is recommended to close the file to ensure any changes are made.
			- Sometimes, due to buffering, certain changes are not made until the file is closed.
			- Closing a file is done through the _.close() method.
		- Syntax:
			```
			<file_variable>.close()
			```
		- Example:
			```
			file.close()
			```
		- Note:
			- It is generally recommended to use the _with_ keyword in addition to the _open()_ function.
				- As this makes closing the file easier and is considered the _Pythonic_ way of handling files.
				- Syntax:
					```
					with open(<filename>, <mode>) as <variable_name>:
						<statements>
					```
				- Example:
					```
					with open("my_file.txt", "w") as file:
						file.write("idkman")
					```
	- Querying the file
		- Definition:
			- In order to know if the file is writable or readable, or even seekable, the _.writable()_ or _.readable()_, or _.seekable()_ methods are used.
			- These methods return a boolean corresponding to their purpose.
		- Syntax:
			```
			<file_variable>.writable()
			#> or
			<file_variable>.readable()
			#> or
			<file_variable>.seekable()
			```
		- Example:
			```
			file.writable() #> returns True if writable
			#> or
			file.readable() #> returns True if readable
			#>
			file.seekable() #> returns True if seekable
			```
	- Other Concepts:
		- Changing the pointer position
			- Definition:
				- To change the current pointer of the file, the .seek() method is used.
				- This method accepts a number as an argument and advances the pointer to that amount.
			- Syntax:
				```
				<file_variable>.seek(<number>)
				```
			- Example:
				```
				file.seek(5) #> advances the pointer by 5 bytes
							   #> "idkman" becomes "n"
				```
		- Querying the current pointer
			- Definition:
				- Done through the _.tell()_ method.
				- i.e. return the position it is current at after using the _.seek()_ method.
			- Syntax:
				```
				<file_variable>.tell()
				```
			- Example:
				```
				file.tell()
				```
		- Querying if the stream is interactible
			- Definition:
				- Done through the _.isatty()_ method.
			- Note:
				- If the current program is run using the terminal, the output of this method is _True_.
				- If the current program is being piped to another stream or session, the output of this method is _False_.
			- Syntax:
				```
				<file_variable>.isatty()
				```
			- Example:
				```
				file.isatty()
				```
		- Querying the current file descriptor
			- Definition:
				- Done through the _.fileno()_ method.
				- Usually, the output of this file is 3, or can be 4, 5 etc.
				- This is due to the first three descriptors being reserved to standard streams.
					- 0 being reserved for _sys.stdin_.
					- 1 being reserved for _sys.stdout_
					- 2 being reserved for _sys.stderr_
			- Syntax:
				```
				<file_variable>.fileno()
				```
			- Example:
				```
				file.fileno()
				```
			- Mote:
				- This method is commonly used inside the _os.fsync()_ (filesync) method to flush current buffer.
					- Example:
						```
						file.flush()            #> Python to System
						os.fsync(file.fileno()) #> System to Dish
						```
	- Deleting a file
		- Definition:
			- Python's native file handling does not have any file deletion methods, this problem is remedied using the _os_ module.
		- Syntax;
			```
			os.remove(<filename>)
			```
		- Example:
			```
			os.remove("my_file.txt") #> deletes the file at the cwd
			```
		- Note
			- This method is coupled with a file check to see if the file exists or not.
				- Syntax:
					```
					os.path.exists(<filename>)
					```
				- Example:
					```
					os.path.exists("my_file.txt") #> returns True if the file exists
					```
			- Folders and directories are able to be removed using a similar syntax.
				- Do note that this command only removes empty folders.
				- Syntax:
					```
					os.rmdir(<folder_name>)
					```
				- Example:
					```
					os.rmdir("my_folder")
					```