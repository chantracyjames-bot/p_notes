
# Touch (touch)
- Definition:
	- Used to change timestamps of files, or can be used to create new empty files only if the file does not exist.
- Syntax:
```
touch <file>
#> or
touch <option> <file>
```
- Example:
```
touch my_file
```
- Options:
	- -a
		- Definition:
			- Updates the access time of a file.
		- Syntax:
			```
			touch -a <file>
			```
		- Example:
			```
			touch -a my_file.txt
			```
	- -m
		- Definition:
			- Updates the modification time of a file
		- Syntax:
			```
			touch -m <file>
			```
		- Example:
			```
			touch -m my_file.txt
			```
	- -t
		- Definition:
			- Sets a specific timestamp to a file.
		- Syntax:
			```
			touch -t <timestamp> <file>
			```
		- Example:
			```
			touch -t 202607191200.00 my_file.txt
			```
	- -c
		- Definition:
			- Disables the create new files flag, does not create a new file when the file doesn't exist.
		- Syntax:
			```
			touch -c <file>
			```
		- Example:
			```
			touch -c my_file.txt
			```
	- -r
		- Definition:
			- Sets a specific timestamp to a file, uses another file as reference.
		- Syntax:
			```
			touch -r <reference_file> <file>
			```
		- Example:
			```
			touch -r reference.txt my_file.txt
			```