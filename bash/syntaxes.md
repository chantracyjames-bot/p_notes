
# Syntaxes
## Comments:
- Definition:
	- Comments in Bash is done through the pound _\#_ symbol.
- Example:
```
# this is a comment
```
## Scope:
- Definition:
	- Commands are run from top to bottom though, there are special cases wherein this is ignored like in function calls.
	- Multiple commands on the same line are able to be separated, using a semicolon _;_.
	- scripts usually start with a special declaration, called a shebang _#!_ which signifies that the file is a Bash script.
## Operations 
- Concatenation
	- Definition:
		- This operation concatenates (or combines) two string variables or string literals to a variable.
	- Syntax:
	```
	$<variable1>$<variable2>
	```
	- Example:
	```
	"$my_variable$my_variable"
	```
- Arithmetic
	- Definition:
		- This operation combines two numbers to one another using the addition + operator.
	- Syntax:
		```
		$((<value1> + <value2>))
		```
	- Example:
		```
		$((10 + 10))
		```