
# Variables
- Definition:
	- Are used to act as containers and used for storing data.
- Declaration and initialization:
	- Definition:
		- To declare a variable in Python, the name of the variable is followed up by an equal sign = and then the value that it may hold.
		- Refer to "data_types.md" for more information.
	- Rules for variable declaration:
		- Variables must have a name.
			- They are also called as identifiers.
			- It is not possible to declare a variable without a name.
		- Variable names can use letters, numbers*, or underscores \_.
			- Do note that variable names cannot start with a number.
		- Variable names must start with a letter or an underscore.
		- Variable names must not contain any special characters.
			- Examples are @, #, %, etc.
		- Variable names cannot be reserved names.
			- Examples are int, float, class, etc.
	- Conventions in naming variables:
		- In Python, snake_case is the most preferred naming schene for variables and attributes.
			- Example: my_var, float_value, current_temp, etc.
		- Variable names must match their purpose.
			- It makes reading variables easier to understand.
			- Example: my_num, var_sum, etc.
	- Syntax:
		```
		<variable_name> = <value>
		```
	- Example:
		```
		idkman = 'yes'
		```
	- Note
		- Unlike in C/C++, Java and other similar programming languages, data types are assigned to variable automatically.
			- Example:
				```
				x = 10 #> x is auto-assigned as int
				
				y = 'yes' #> y is auto-assigned as str
				```
	
	- It is possible to declare a value alongside the variable.
		- Syntax:
			```
			<variable_name> = <value>
			```
		- Example:
			```
			my_num = 10
			```
	- It is possible to declare more than one variable in a single statement.
		- Note:
			- That each variable must come with their values.
		- Syntax:
			```
			<variable_name1>, <variable_name2>, <variable_name3> = <value1>, <value2>, <value3>
			```
		- Example:
			```
			my_num, my_float, my_bool = 10, 3.14, False
			```
	- It is possible to re-assign data types to variables.
		- Example:
			```
			x = 10 #> x is assigned as int
			
			y = 3.14 #> x is now assigned as float
			```
- Access and modification
	- Definition:
		- The values of variables are accessed by calling their name.
	- Syntax:
		```
		<variable_name>
		```
	- Example:
		```
		x = 10
		
		x #> returns the value of x
		```
	- It is possible to change the value of a variable.
		- Syntax:
			```
			<variable_name> = <new_value>
			```
		- Example:
			```
			x = 100
			```
	- It is possible to set (or declare) the value of a variable equal to another, they become "linked" and changes in one variable affects the other.
		- Syntax:
			```
			<variable_name1> = <variable_name2>
			```
		- Example:
			```
			x = y #> y becomes equal to x
			```
- Type casting
	- Definition:
		- It is possible to specify (or change) the data type of a variable, done through "casting" the variable into another type.
		- It uses the data type class to cast their data type.
		- Examples are int(), float(), str(), etc.
	- Syntax:
		```
		<data_type>(<value>)
		```
	- Example:
		```
		int("10") #> "10" becomes an int, or 10
		```