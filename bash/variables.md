
# variables
- Declaration and definition
	- Definition:
		- Variables are declared using a variable name and then assigning it a value.
		- Values are assigned using the assignment operator _=_.
	- Syntax:
		```
		<variable_name>=<value>
		```
	- Example:
		```
		my_variable="idkman"
		```
- Access and variable calls
	- Definition:
		- Once variables are declared and defined, they are called using a dollar sign $.
	- Syntax:
		```
		$<variable_name>
		```
	- Example:
		```
		$my_variable
		```
- Local variables
	- Definition:
		- These are variables that are only a variable in the block of code they reside in.
		- They are not able to be accessed from the outside, unlike global variables which are able to be accessed from anywhere in the script only if that variable is declared before it is called.
	- Example:
		```
		test_func() {
		    VAR=100
		}
		```