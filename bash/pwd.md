
# Print Working Directory (cwd)
- Definition:
	- Used to print the current working directory.
- Syntax:
```
pwd
#> or
pwd <options>
```
- Options:
	- -L
		- Definition:
			- Prints the logical path, including any symbolic links.
		- Syntax:
			```
			pwd -L
			```
	- -P
		- Definition:
			- Prints the physical path, does not include symbolic links.
		- Syntax:
			```
			pwd -P
			```