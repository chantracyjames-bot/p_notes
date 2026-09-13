
# Data Types
- Definition:
	- BASH natively supports strings, integers and arrays, but it does not have native support for floating points.
	- Decimals are automatically evaluated as integers when operating on them.
- Strings
	- Definition:
		- These are values that are enclosed in double quotes.
	- Example:
		```
		"idkman"
		```
- Numbers
	- Definition:
		- These are integers or values that are not envoloped in double quotes
	- Example:
		```
		1, 2, 3
		```
- Arrays
	- Definition:
		- These type holds multiple values and they are able to hold both numbers and strings at the same time.
	- Example:
		```
		("idkman", 100, "yes, 3.14")
		```
- Associative arrays
	- Definition:
		- These are variables that associate with arrays, adding values for each element of the array similar to dictionaries or maps.
	- Syntax:
		```
		declare -A <associative_name>
		```
	- Example:
		```
		declare -A lumbago
		lumbago[idkman]="maybe"
		```
