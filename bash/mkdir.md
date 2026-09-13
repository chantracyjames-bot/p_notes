
# Make Directory (mkdir)
- Definition:
	- Used to create new folders or directories.
- Syntax:
```
mkdir <new_directory>
#> or
mkdir <option> <new_directory>
```
- Example:
```
mkdir new_folder
```
- Options:
	- -p
		- Definition:
			- Creates a new parent directory, i.e. creates a new folder if the parent doesn't exist.
		- Syntax:
			```
			mkdir -p <parent_directory>/<new_directory>
			```
	- -v
		- Definition:
			- Enables verbose mode, displays the progress of folders being created.
		- Syntax:
			```
			mkdir -v <new_directory>
			```
	- -m
		- Definition:
			- Sets the file mode of the new directory, i.e. folder permissions.
		- Syntax:
			```
			mkdir -m <permissions> <new_directory>
			```