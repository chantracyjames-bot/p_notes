
# Arrays
- Definition:
	- Arrays are used to store multiple values in a single variable.
	- Instead of declaring multiple variables to store multiple values, arrays makes the process easier.
- Declaration and definition
	- Definition:
		- Arrays are declared using a data type and square brackers
	- Two ways to create arrays:
		- Explicit declartion
			- Definition:
				- It is possible to create arrays by directly assigning values to it.
				- Values are stored using curly braces _{ }_, and multiple values are declared using a comma-separated list.
			- Syntax:
				```
				<data_type> <array_name> = {<values>};
				```
			- Example:
				```
				int my_array = {1, 2, 3, 4, 5};
				```
		- Implicit declaration
			- Definition:
				- An empty array is automatically created when only the size is specified
			- Syntax:
				```
				<data_type> <array_name>[<size>]
				```
			- Example:
				```
				char my_string[10];
				```
- Access and modification
	- Accessing elements
		- Definition:
			- The elements inside an array is accessed through the use of indices.
			- In most languages, the index number usually starts at 0, i.e. the first element has an index of 0.
			- Trying to access an index that is greater than the size of the array will result in an error.
		- Syntax:
			```
			<array_name>[<index>];
			```
		- Example:
			```
			my_array[10]; // tries to access the 9th element
			```
	- Modifying elements
		- Definition:
			- Values of an array are able to be changed through accessing them via their index and using the _=_ assignment operator.
		- Syntax:
			```
			<array_name>[<index>] = <new_value>;
			```
		- Example:
			```
			my_array[1] = 10;
			```
	- Querying the size
		- Definition:
			- The size of an array is obtained through the _sizeof()_ operator.
		- Syntax:
			```
			sizeof(<array_name>);
			```
		- Note:
			- The _sizeof()_ operator returns the size in bytes and not the actual element count.
				- Element count is obtained through a mathematical operation.
				- Syntax:
					```
					sizeof(<array_name>) / sizeof(<array_name>[<index_value>]);
					```
- Multidimensional arrays
	- Definition:
		- Also called "nested arrays", as it is possible to insert array inside arrays.
	- Example:
		```
		int my_array[3][4] = {
			{1, 2, 3, 4},
			{5, 6, 7, 8},
			{9, 10, 11, 12}
		};
		```
	- Note:
		- The size of a multidimensional arrays must be declared unlike normal arrays.
		- Accessing a nested array is done through using the index of the parent array and then the child array.
			- Syntax:
				```
				<array_name>[<outer_index>][<inner_index>];
				```
			- Example:
				```
				my_array[1][2];
				```
			- The leftmost index is the parent array and every succeeding index is the child array.
			- Modifying the values if done through the same process as normal arrays only adding another index to represent the leaf values.
				- Syntax:
					```
					<array_name>[<outer_index>][<inner_index>] = <new_value>;
					```
				- Example:
					```
					my_array[1][3] = 100;
					```