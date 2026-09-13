
# Remove (rm)
- Definition:
	- Used to remove files or folders
- Note:
	- This command is extremely powerful, any removed files are not easily recovered.
- Syntax:
```
rm <file>
#> or
rm <option> <file>
```
- Example:
```
rm my_file
#> or
rm my_folder
```
- Options:
	- -v
		- Definition:
			- Enables verbose mode, displays progress of removal.
		- Syntax:
			```
			rm -v <file>
			```
		- Example:
			```
			rm -v my_file.txt
			```
	- -i
		- Definition:
			- Enables prompt before removing, used to avoid making accidental deletions.
		- Syntax:
			```
			rm -i <file>
			```
		- Example:
			```
			rm -i my_file.txt
			```
	- -r
		- Definition:
			- Enables recursive removal, removes files and folders inside of folders.
		- Syntax:
			```
			rm -r <folder>
			```
		- Example:
			```
			rm -r my_file.txt
			```
	- -f
		- Definition:
			- Enables force removal, removes files without any warning
		- Syntax:
			```
			rm -f <file>
			```
		- Example:
			```
			rm -f my_file.txt
			```