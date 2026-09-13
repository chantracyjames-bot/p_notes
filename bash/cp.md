
# Copy (cp)
- Definition:
	- Used to copy files and directories from one location to another
- Syntax:
```
cp <source> <destination>
#> or
cp <option> <source> <destination>
```
- Example:
```
cp my_file.txt my_folder/copy.txt
```
- Options:
	- -r
		- Definition:
			- Enables recursive copying, or copies all files from a directory.
		- Syntax:
			```
			cp -r <source> <destination>
			```
		- Example:
			```
			cp -r my_folder/ my_other_folder/
			```
	- -v
		- Definition:
			- Enables verbose mode, displays the progress of files being copied.
		- Syntax:
			```
			cp -v <source> <destination>
			```
		- Example:
			```
			cp -r my_file.txt my_folder
			```
	- -i
		- Definition:
			- Enables a prompt before overwriting, used to avoid replacing files when both share the same name.
		- Syntax:
			```
			cp -i <source> <destination>
			```
		- Example:
			```
			cp -r my_file.txt my_folder/
			```
	- -u
		- Definition:
			- Only copies the files if the source file is newer, i.e. overwrites the file with the same name if the source file if newer than the destination file.
		- Syntax:
			```
			cp -u <source> <destination>
			```
		- Example:
			```
			cp -r my_file.txt my_folder/
			```