
# Global Regular Expression Print (grep)
- Definition
	- Used to query and search for text patterns in files.
- Syntax:
```
grep <pattern> <file>
# or
grep <option> <pattern> <file>
```
- Example:
```
grep 'text here' my_file.txt
```
- Options:
	- -i
		- Definition:
			- Ignores case-sensitivity, i.e. searches both uppercase and lowercase patterns.
		- Syntax:
			```
			grep -r <pattern> <file>
			```
		- Example:
			```
			grep -r 'tExt HeRE' my_file.txt
			```
	- -r
		- Definition:
			- Searches through files inside a specific directory.
		- Syntax:
			```
			grep -r <pattern> <directory>
			```
		- Example:
			```
			grep -r 'text here' my_file.txt
			```
	- -v
		- Definition:
			- Finds files that do not match the pattern.
		- Syntax:
			```
			grep -v <pattern> <file>
			```
		- Example:
			```
			grep -v 'text here' my_file.txt
			```