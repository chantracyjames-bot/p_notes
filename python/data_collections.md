
# Data Collections
- Definition:
	- Collections are used to store multiple values in a single variable.
	- Instead of declaring multiple variables to store value, collections like arrays makes the process easier.
- Note:
	- Lists are the commonly used as arrays in Python.

- Array-like list in Python
	- Declaration and initialization
		- Definition:
			- Arrays (lists) are declared using square brackets _[ ]_, values are separated by commas _,_.
	   - Syntax:
			```
			<array_name>: list = [<values>]
			#> or
			<array_name>: list[<data_type>] = [<values>]
			```
	   - Example:
			```
			my_array: list = []              #> empty array
			my_list: list = [1, "idk", True] #> non-empty array
			```
	- Access and modification
		- Accessing elements
			- Definition:
				- The elements inside an array is accessed through the use of indices.
				- In most languages, the index usually starts at 0.
				- i.e. the first element starts at index 0.
				- Trying to access an index that is greated than the size of the array will result in an _IndexError_.
		   - Syntax:
				```
				<array_name>[<index>]
				```
		   - Example:
				```
				my_array[0]
				```
		- Modifying elements
			- Definition:
				- The elements inside an array are able to be changed.
				- It is done through accessing their index and using the assignment operator to change the value.
		   - Syntax:
				```
				<array_name>[<index>] = <new_value>
				```
		   - Example:
				```
				my_array[0] = 3
				```
		- Querying the size
			- Definition:
				- The size of an array is obtained through the use of the _len()_ function.
		   - Syntax:
				```
				len(<array_name>)
				```
		   - Example:
				```
				len(my_array)
				```
		- Index pointers
			- Definition:
				- The index can either be a positive or negative number
				- Positive values incrementing starts from the first element, starts at 0 and ends at the last positive element.
				- Negative values decrementing starts from the last element, starts from the last element and ends at the first element.
		- Index slicing
			- Definition:
				- It is possible to "slice" the values of a list or a tuple.
		- Syntax:
			```
			<array_name>[<start_value>:<stop_value>:<step_value>]
			```
			- Where:
				- Start value:
					- Definition:
						- It is inclusive, or it includes the value.
						- Dictates which part of a list or tuple the index will start in.
						- If there are no stop value (present but empty), it will read the entire list from the starting index.
					- Example:
						```
						my_array[3]  #> reads index 3
						my_array[2:] #> starts fron index 2 and reads until the end of the array
						```
				- Stop value:
					- Definition:
						- It is exclusive, or it excludes the value.
						- Dictates which part of a list of tuple the index will end in.
						- If there are no start value (present but empty), it will read the entire list from the start of the array until the stop value - 1.
					- Example:
						```
						my_array[1:3] #> reads index 1 until index 3 - 1 (2)
						my_array[:6]  #> starts from the beginning and reads until the stop value
						```
				- Step value
					- Definition:
						- Dictates how much the index increments or decrements, the default value is 1
						- Can be a positive or negative number, with:
							- Positive numbers will move the index forward.
							- Negative numbers will move the index backward.
					- Example:
						```
						my_array[1:5:2]  #> reads index from 1 to 5 but skips 2 per read
											#> effectively being index 2 and 4
						my_array[5:1:-1] #> reads from index 5 to 1 buts skips -1 per read
											#> effectively being index 5, 4, 3
						```
		- Example:
			```
			my_array[2]     #> starts at index 2 (third element)
			my_array[3:6]   #> starts at index 3, ends at index 5
			my_array[1:5:2] #> starts at index 1, ends at index 4, skips 2 indices
			```
		- Value manipulation
			- Definition:
			   - It is possible to modify values inside a list using inedx slicing
			- Note:
				- When inserting values that is more that the values being replaced, the remaining values will get displaced.
				- The same thing happens when inserting values that is less than the values being replaced.
			- Syntax:
				```
				<list_name>[<start_value>:<stop_value>] = <new_values>
				```
			- Example:
				```
				my_list[1:4] = 1, 2, 3, 4 #> changes the values of index 1, 2, and 3
										      #> inserts a new value after index 3
				```
	- Multidimensional arrays
		- Definition:
			- Also called "nested arrays".
		- Declaration and initialization
			- Definition:
				- It is possible to insert arrays inside arrays.
				- The elements inside a nested array can either be:
					- Mixed arrays
						- Definition:
							- Contains both arrays and normal values.
						- Example:
							```
							my_nested_array: list = [1, "yes", [True, 0], "Hello World"]
							```
					- Pure arrays
						- Definition:
							- Contains only array elements.
						- Example:
							```
							my_nested_array: list[list[]] = [[1, 2], ["idk", "man"], [True, False]]
							```
		- Accessing and modofication
			- Accessing elements
				- Definition:
					- Accessing a nested array is done through the use of the index of the parent array and then the child array.
				- Syntax:
					```
					<array_name>[<parent_index>][child_index]
					```
				- Example:
					```
					my_nested_array[1][1]
					```
				- Note:
					- The leftmost index is the outermost array and the every succeesing index is the child array.
			- Modifying elements
				- Definition:
					- Modifying the vales is done through the same process as normal arrays.
				- Syntax:
					```
					<array_name>[parent_index][child_index] = <new_value>
					```
				- Example:
					```
					my_nested_array[1][0] = "maybe"
					```
			- Querying the size
				- Definition:
					- The size of an array inside a nested array is queried using the _len()_ function
				- Syntax:
					```
					len(<array_name>[parent_index])
					```
				- Example:
					```
					len(my_nested_array[1])
					```

- Types of collections in Python
	- lists
		- Definition:
			- Most commonly used array in Python.
			- Elements are ordered, mutable and allows duplicate values.
			- Ordered:
				- New items are appended at the end of the list.
				- Some methods are able to add items.
				- Generally, lists elements are ordered.
			- Mutable
				- Items are able to be added, removed and modified.
			- Duplicates
				- Duplicates or reocurring values are allowed.
		- Declaration and initialization
			- Definition:
				- Can be declared in two ways
			- Implicit declaration
				- Definition:
					- Uses square brackets _[ ]_.
				- Syntax:
					```
					<list_name> = [<values>]
					```
				- Example:
					```
					my_list: list = [1, "idk", True]
					```
			- Explicit declaration
				- Definition:
					- Uses the _list_ class
				- Syntax:
					```
					list([<values>])
					#> or
					list(<iterable>)
					```
				- Example:
					```
					list([1, "idk", True])
					```

		- Access and modification
			- Accessing elements
				- Definition:
					- _list_ values are able to be accessed through their index.
					- Do note that index values start at 0.
				- Syntax:
					```
					<list_name>[<index>]
					```
				- Example:
					```
					my_list[1]
					```
			- Modifying elements
				- Definition:
					- _list_ values are able to be modified using the same way they are accessed.
					- Values are assigned using the assignment = operator.
				- Syntax:
					```
					<list_name>[<index>] = <new_value>
					```
				- Example:
					```
					my_list[1] = "man"
					```
				- Note:
					- Adding new elements are done through the _.insert()_, _.append()_ and _.extend()_ methods.
					- Removing certain elements are done through the _.remove()_ and _.pop()_ methods.
					- Clearing the whole _list_ is done through the _.clear()_ method.
					- The _del_ keyword can do both tasks as well, removing and clearing the _list_.
					- Sorting can also be accomplished through the _.sort()_ methods, it sorts the list alphanumerically.
		- Collection unpacking
			- Definition:
				- It is possible to unpack lists and assign their values to individual variables.
			- Note:
				- If the amount of variable to store the new values are not sufficient, the last variable will store the remaining values.
			- example:
				```
				x, y, z = my_list
				```

		- List duplication
			- Definition:
				- Duplication is achieved through the use of the assignment _=_ operator.
			- Syntax:
				```
				<list_name1>: list = <list_name2>
				#> or
				<list_name1>: list[<data_type>] = <list_name2>
				```
			- Example:
				```
				my_list: list = my_other_list
				```
			- Note:
				- Using this method, both lists will become "linked".
					- Any changes to one will affect the other, this is due to them pointing to the same reference in memory.
				- To duplicate a list without dealing with linking, the _.copy()_ method solves this problem.
					- Syntax:
						```
						<list_name1>: list = <list_name2>.copy()
						#>
						<list_name1>: list[<data_type>] = <list_name2>.copy()
						```
					- Example:
						```
						my_list: list = my_other_list.copy()
						```
					- The slice operator can also be used to copy lists.
						- Syntax:
							```
							<list_name>: list = <list_name2>[:]
							#> or
							<list_name>: list[<data_type>] = <list_name2>[:]
							```

		- List concatenation
			- Definition:
				- Lists are able to be merged together or conjoined through the _+_ operator.
			- Syntax:
				```
				<list_name1> + <list_name2>
				```
			- Example:
				```
				my_new_list: list = my_list + my_other_list
				```
			- Using the _.extend()_ methods can also work to concatenate lists.
				- Example:
					```
					my_list.extend(my_other_list)
					```

		- List comprehension
			- Definition:
				- It is possible to create lists on the fly using list comprehension.
				- the expression is enclosed in square brackets _[ ]_.
			- Syntax: 
				```
				<list_name>: list = [<expression>]
				#>
				<list_name>: list[<data_type>] = [<expression>]
				```
			- Example:
				```
				my_list: list[int] = [x for x in range(5)] #> [0, 1, 2, 3, 4]
				```

	- tuples
		- Definition:
			- Elements are ordered, immutable and allows duplicate values.
			- Ordered:
				- Items have a fixed order.
			- Immutable:
				- Items cannot be added, removed or modified.
				- Modification is achieved by converting the tuple into a list, or by tuple by tuple operations.
			- Duplicates:
				- Duplicates or reocurring values are allowed.
		- Declaration and initialization
			- Definition:
				- Tuples are able to be declared in two ways.
			- Implicit declaration
				- Definition:
					- Uses parentheses _( )_.
				- Syntax:
					```
					<tuple_name>: tuple = (<values>)
					#>
					<tuple_name>: tuple[<data_type>] = (<values>)
					```
				- Example:
					```
					my_typle: tuple = (0, "man", False)
					```
			- Explicit declaration
				- Definition:
					- Uses the _tuple_ class.
				- Syntax:
					```
					tuple((<values>))
					#> or
					tuple(<iterable>)
					```

		- Access and modification
			- Accessing elements
				- Definition:
					- _tuple_ values are able ot be accessed through their index.
					- Index values start at 0.
				- Syntax:
					```
					<tuple_name>[<index>]
					```
				- Example:
					```
					my_tuple[1]
					```
			- Modifying elements
				- Definition:
					- While tuples are immutable, the one of few ways to modify the elements is to convert the tuple into a list.
					- After the modification, it can be returned to being a tuple.
				- Example:
					```
					my_tuple: tuple[int] = (1, 2, 3, 4)
					my_list: list[int] = list(my_tuple)
					my_list.append(5)
					my_tuple = tuple(my_list)
					```
				- Note:
					- The same workaround is able to be used to remove, modify and query items.
					- Tuples are able to be added to other tuples:
						- Syntax:
							```
							<tuple_name1> += <tuple_name2>
							```
						- Example:
							```
							my_tuple += my_other_tuple
							```
					- Tuples are also allowed to be multiplied with integers, effectively multiplying the elements.
						- Example:
							```
							my_tuple: tuple[int] = (1, 2, 3, 4)
							my_other_tuple: tuple[int] = my_tuple * 2 #> (1, 2, 3, 4, 1, 2, 3, 4)
							```
		- Collection unpacking
			- Definition:
				- It is possible to unpack tuples and assign their valuts to individual variables.
			- Note:
				- If the amount of variables to store the new values are not sufficient, the last variable will store the remaining values.
			- Example:
				```
				x, y, z = my_tuple
				```

	- sets
		- Definition:
			- Elements are unordered, immutable, and does not allow duplicate values.
			- Unordered:
				- The values are stored in random order, as sets do no have any fixed indices.
			- Immutable
				- Items cannot be modified, though there are certain methods to modify values. 
			- Duplicates
				- Sets discards any duplicate values.
		- Declaration and initialization
			- Definition:
				- Sets are able to be declared in two ways.
			- Implicit declaration
				- Definition:
					- Uses curly braces _{ }_.
				- Syntax:
					```
					<set_name>: set = {<values>}
					#> oe
					<set_name>: set[<data_type>] = {<values>}
					```
				- Example:
					```
					my_set: set[int] = {1, 2, 3, 4}
					```
			- Explicit declaration
				- Definition:
					- Uses the _set_ class.
				- Syntax:
					```
					set({<values>})
					#> or
					set(<iterable>)
					```
		- Access and modification
			- Accessing elements
				- Definition:
					- On sets, it is not possible to access values through indices.
					- The reason being the unorderedness and sets being unindexed.
					- The only way to view set elements is through the use of a loop.
				- Example:
					```
					for i in my_set:
					print(i)
					```
			- Modifying elements
				- Definition:
					- While being immutable, it is still possible to add and remove items from a set.				
					- Refer to set methods for more methods
				- Adding elements
					- Definition:
						- Adding values is done through the use of the _.add()_ method.
					- Example:
						```
						my_set.add("yes")
						```
				- Removing elements
					- Definition:
						- Removing values is done through the use of the _.remove()_ method.
					- Example:
						```
						my_set.remove("yes")
						```

		
		- Set duplication
			- Definition:
				- Duplication is achieved through the use of the assignment _=_ operator.
			- Syntax:
				```
				<set_name1>: set = <set_name2>
				#>
				<set_name1>: set[<data_type>] = <set_name2>
				```
			- Example:
				```
				my_set: set = my_other_set
				```
			- Note:
				- After using this solution to duplicate sets, both sets will become "linked".
					- Any changes to one will affect the other, this is due to them pointing at the same reference in memory
				- To duplicate a set with dealing with linking, the _.copy()_ method avoids this problem.
					- Syntax:
						```
						<set_name1>: set = <set_name2>.copy()
						#>
						<set_name1>: set[<data_type>] = <set_name2>.copy()
						```
					- Example:
						```
						my_set: set = my_other_set.copy()
						```

		- frozensets
			- Definition:
				- A fully immutable version of a set, items cannot be removed or added even through the use of set methods.
			- Declaration
				- Definition:
					- Can be declared using the _frozenset_ class.
				- Syntax:
					```
					frozenset({<values>})
					#> or 
					frozenset(<iterable>)
					```

	- dicts
		- Definition:
			- shortened name for dictionaries.
			- Elements are ordered, immutable and does not allow duplicates.
			- Ordered:
				- Items stored have a fixed order.
			- Immutable:
				- Items cannot be modified, though there are some methods to bypass this.
			- Duplicates:
				- Dictionary keys are not allowed to have duplicates.
				- Unlike keys, their value can be duplicates.
		- Declaration and initialization
			- Definition:
				- Dictionaries can be declared using curly braces _{ }_.
				- The entries must come in pairs, a key and its value separated by a colon _:_.
				- Dictionaries are able to be declared in two ways.
			- Implicit declaration
				- Syntax:
					```
					<dict_name>: dict = {<key>: <value>}
					```
				- Example:
					```
					my_dict: dict = {"yes": "no", "idk": "man"}
					```
				- Note:
					- If the key is a string, it must be enclosed in quotes.
			- Explicit declaration
				- Syntax:
					```
					<dict_name>: dict[<key_type>, <value_type>] = {<key_value>: <value>}
					#> or
					dict(<key_name>=<value>)
					#> or
					dict([(<>key_name1, <value1>), (<key_name2>, <value2>)])
					```
				- Example:
					```
					my_dict: dict[str, str] = {"yes": "no", "idk": "man"}
					```
		- Access and modification
			- Accessing elements
				- Definition:
					- Dictionary values are access by using their key.
				- Note:
					- Keys are case-sensitive.
				- Syntax:
					```
					<dict_name>[<key>]
					```
				- Example:
					```
					my_dict["yes"]
					```
				- Note:
					- Values can also be retrieved using the _.get()_ method.
						- Syntax:
							```
							<dict_name>.get(<key>)
							```
					- The _.keys()_ method returns all keys inside a dictionary.
					- The _.values()_ method returns all values inside a dictionary
			- Modifying elements
				- Definition:
					- Modifying values of keys are done by accessing their index.
				- Syntax:
					```
					<dict_name>[<key>] = <new_value>
					```
				- Example:
					```
					my_dict["idk"] = "lumbago"
					```
				- Note:
					- Modifying elements can also be done using the _.update()_ method.
						- If the key is not present, it will create a new entry
						- Syntax:
							```
							<dict_name>.update(<key>=<new_value>)
							```
						- Example:
							```
							my_dict.update(yes = "idkman")
							```
		- Dictionary duplication
			- Definition:
				- Dictionary duplication is done through the use of the assignment _=_ operator.
			- Syntax:
				```
				<dict_name1>: dict = <dict_name>
				#> or
				<dict_name1>: dict[<data_type>, <data_type>] = <dict_name>
				```
			- Example:
				```
				my_dict: dict = my_other_dict
				```
			- Note:
				- Using this method to duplicate dictionaries, both dictionaries will become "linked".
					- Any changes to one will affect the other, this is due to them pointing at the same reference in memory.
				- To duplicate a dictionary without dealing with memory linking, the _.copy()_ method avoids this problem.
					- Syntax:
						```
						<dict_name1>: dict = <dict_name2>.copy()
						#> or
						<dict_name1>: dict[<data_type>, <data_type>] = <dict_name2>.copy()
						```
					- Example:
						```
						my_dict: dict = my_other_dict.copy()
						```