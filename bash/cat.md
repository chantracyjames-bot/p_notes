
# Concatenation (cat)
- Definition:
	- Shows the content of files in the terminal.
- Syntax:
```
cat <file>
#> or
cat <option> <file>
```
- Example:
```
cat my_file.txt
```
- Note:
	- It can also be used to concatenate files.
		- Syntax:
			```
			cat <file1> <file2> > <output_file>
			```
		- Example:
			```
			cat my_file.txt my_other_file.txt > result.txt
			```
- Options
	- -n
		- Definition:
			- Adds numbers to each line, including blank lines.
		- Syntax:
			```
			cat -n <file>
			```
		- Example:
			```
			cat -n my_file.txt
			```
	- -b
		- Definition:
			- Adds number to each line, excluding blank lines.
		- Syntax:
			```
			cat -b <file>
			```
		- Example:
			```
			cat -b my_file.txt
			```
	- -s
		- Definition:
			- Suppresses empty lines, i.e. does not show any empty lines.
		- Syntax:
			```
			cat -s <file>
			```
		- Example:
			```
			cat -s my_file.txt
			```
	- -v
		- Definition:
			- Used to show non-printing characters, used for debugging.
		- Syntax:
			```
			cat -v <file>
			```
		- Example:
			```
			cat -v my_file.txt
			```