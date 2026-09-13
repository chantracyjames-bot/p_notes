
# Print (echo)
- Definition:
	- Used to display a line of text to the terminal.
- Syntax:
```
echo <message>

#> or

echo <options> <message>
```
- Example:
```
echo "Hello World"
```
- Options:
	- -n
		- Definition:
			- Prevents echo from adding a newline "\n" at the end, any succeeding echo calls appends to the end of the current line.
		- Syntax:
			```
			echo -n <message>
			```
		- Example:
			```
			echo -n "my_message"
			```
	- -e
		- Definition:
			- Allows special characters to manipulate output, like newlines and horizontal tabs spaces.
		- Syntax:
			```
			echo -e <message>
			```
		- Example:
			```
			echo -e "my_message\n"
			```
	- -E
		- Definition:
			- Disables special characters or escape sequences, default mode of echo.
		- Syntax:
			```
			echo -E <message>
			```
		- Example:
			```
			echo -E "my_message"
			```
