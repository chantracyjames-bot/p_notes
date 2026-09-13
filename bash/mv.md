
# Move (mv)
- Definition:
	- Used to move files and directories from one location to another.
- Syntax:
```
mv <source> <destination>
#> or
mv <option> <source> <destination>
```
- Example:
```
mv my_file.txt my_folder/
```
- Note:
	- _mv_ can also be used to rename files.
		- Syntax:
			```
			mv <old_name> <new_name>
			```
		- Example:
			```
			mv my_file.txt renamed_file
			```
- Options:
	- -v
		- Definition:
			- Enables verbose mode, displays the progress of files being copied.
		- Syntax:
			```
			mv -v <source> <destination>
			```
	- -i
		- Definition:
			- Enables a prompt before overwriting, used to avoid replacing files when both share the same name.
		- Syntax:
			```
			mv -i <source> <destination>
			```
	- u
		- Definition:
			- Only copies the files if the source file is newer, i.e. overwrites the file with the same name if the source file if newer than the destination file.
		- Syntax:
			```
			mv -u <source> <destination>
			```