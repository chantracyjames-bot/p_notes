
# Functions
- Built-in methods
	- Universal functions
		- _print()_
			- Definition:
				- Used to print text to the screen.
			- Syntax:
				```
				print(<value>)
				```
			- Note:
				- Multiple values can be printed, but must be separated by commas _,_.
					- Syntax:
						```
						print(<value1>, <value2>, <value3>)
						```
				- This method has an end= parameter, used to replace the newline ('\n') after each default print() call.
					- Syntax:
						```
						print(<value>, end = <value>)
						```
		- _input()_
			- Definition:
				- Used for gathering user input.
			- Syntax:
				```
				input(<prompt>)
				```
				- Where:
					- prompt
						- Definition:
							- The prompt parameter is used to display text when the input function is ran.
						- Example:
							```
							input('lumbago? ') #> prints and then asks for user input
							```
			- Note:
				- The input() function returns a string, using it in as another data type is done via type casting.
		- _type()_
			- Definition:
				- Used to query the data type of a variable.
			- Syntax:
				```
				type(<value or variable name>)
				```
			- Example:
				```
				x: int = 10
				type(x) #> `<class 'int'>`
				```
		- _len()_
			- Definition:
				- Queries the size of a list and by extension, strings also/
			- Syntax:
				```
				len(<list>)
				```
			- Example:
				```
				a: str = "idkman"
				
				len(a) #> 6
				```
		- _isinstance()_
			- Definition:
				- Determines if the value is the same type as the first parameter.
			- Syntax:
				```
				isinstance>(<variable>, <data_type>)
				```
			- Example:
				```
				x: float = 3.14
				
				isinstance(x, float) #> True
				```
		- _range()_
			- Definition:
				- Returns a range of integers, starts at 0.
			- Syntax:
				```
				range(<integer>)
				```
			- Example:
				```
				range(6) #> 0, 1, 2, 3, 4, 5
				```
			- Note:
				- Similar to slicing, there are start, stop and step values.
					- Syntax:
						```
						range(<start>, <stop>, <step>)
						```
					- Example:
						```
						range(3, 6, 2) #> 3, 5
						```
				- Range values are able to be displayed when transform into a list() object.
		- _map()_
			- Definition:
				- Applies a function to every iterable, mostly used in lambda functions.
			- Syntax:
				```
				map(<lambda_function>, <container>)
				```
		- _filter()_
			- Definition:
				- Creates a list of items when the condition is _True_.
			- Syntax:
				```
				filter(<lambda_function>, <container>)
				```
		- _sorted()_
			- Definition:
				- Sorts item alphanumerically.
			- Syntax:
				```
				sorted(<values>)
				```
		- _next()_
			- Definition:
				- Manually advances a generator object iterable, used when dealing with generator functions.
			- Syntax:
				```
				<variable> = <generator_function>
				next(<variable>)
				```
		- _random()_
			- Definition:
				- Requires the _random_ module, used to generate random numbers.
			- Example:
				```
				#> random number generator with a range
				random.randrange(1, 10) #> 1 - 9
				#> 1 is inclusice, 10 is exclusive
				```
	- String methods
		- _.lower()_
			- Definition:
				- Converts the characters inside a string into their lowercase forms.
			- Syntax:
				```
				<string>.lower()
				```
			- Example:
				```
				my_string: str = 'IDKMAN'
				my_string.lower() #> 'idkman'
				```
		- _.upper()_
			- Definition:
				- Converts the characters inside a string into their uppercase forms.
			- Syntax:
				```
				<string>.upper()
				```
			- Example:
				```
				my_string: str = 'idkman'
				my_string.lower() #> 'IDKMAN'
				```
		- _.strip()_
			- Definition:
				- Removes the whitespace present before or after the text.
			- Syntax:
				```
				<string>.strip()
				```
			- Example:
				```
				my_string: str = " Hello World "
				my_string.strip() #> "Hello World"
				```
		- _.replace()_
			- Definition:
				- Replaces a keyword (or a character) in a string.
			- Syntax:
				```
				<string>.replace(<string_to_be_replaced>, <replacement_string>)
				```
			- Example:
				```
				my_string: str = 'lumbago'
				my_string.replace('l', 'd') #> 'dumbago'
				```
		- _.split()_
			- Definition:
				- Splits the string into a list dictated by the split parameter, typically used to transform list values from comma separators.
			- Syntax:
				```
				<string>.split(<string_separator>)
				```
			- Example:
				```
				my_string: str = "Hello,World"
				my_list: list[str] = my_string.split(',') #> ['Hello', 'World']
				```
		- _.format()_
			- Definition:
				- Presents a way to format strings, replaced by the f-string in python 3.6.
				- Different syntax to f-strings, but still uses curly braces _{ }_ as placeholder.
			- Syntax:
				```
				<string>.format(<placeholder>)
				```
			- Example:
				```
				"yes{}".format("no")
				```
			- Note:
				- Multiple placeholders are possible.
					- Example:
						```
						my_text: str = "my number is {} and adding {} equals {}"
						my_text.format(10, 20, 30)
						```
				- It is common to use index numbers to mark the number and order of placeholders.
					- Example:
						```
						test: str = "one {0}, yes {1}, idkman {2}"
						```
				- It is also common to use names as indexes.
					- Example:
						```
						test = "{one}, {two}, {three}"
						```
	- math methods
		- _abs()_
			- Definition:
				- Returns the absolute value on a number, i.e. returns it as a positive.
			- Syntax:
				```
				abs(<number>)
				```
			- Example:
				```
				abs(-9.23) #> 9.23
				```
		- _min()_
			- Definition:
				- Returns the minimum value of an iterable.
			- Syntax:
				```
				min(<iterable>)
				```
			- Example:
			```
			min(1, 78, 10, 29, 199) #> 199
			```
		- _max()_
			- Definition:
				- Returns the maximum value of an iterable.
			- Syntax:
				```
				max(<iterable>)
				```
			- Example:
				```
				max(9, 34, 23, 22, 31) #> 34
				```
		- _pow()_
			- Definition:
				- Returns the value an value raised to a power.
			- Syntax:
				```
				pow(<num1>, <num2>)
				```
				- Where:
					- num1
						- Is the base number.
					- num2
						- Is the exponent.
			- Example:
				```
				pow(2, 4) #> 16
				```
	- list methods
		- adding elements
			- _.insert()_
				- Definition:
					- Inserts values at a specified index/
				- Syntax:
					```
					<list_name>.insert(<index>, <value>)
					```
				- Example:
					```
					my_list: list[int] = [1, 2, 3]
					my_list.insert(1, 10) #> [1, 10, 2, 3]
					```
			- _.append()_
				- Definition:
					- Adds items at the end of the list.
				- Syntax:
					```
					<list_name>.append(<value>)
					```
				- Example:
					```
					my_list: list[int] = [1, 2, 3]
					my_list.append(4) #> [1, 2, 3, 4]
					```
			- _.extend()_
				- Definition:
					- Used to extend (or append) elements from another list to the current list.
					- It is possible to extend from other containers, like tuples, sets and dictionaries.
				- Syntax:
					```
					<list_name1>.extend(<list_name2>)
					```
				- Example:
					```
					my_list: list[int] = [1, 2, 3]
					my_other_list: list[int] = [4, 5, 6]
					my_list.extend(my_other_list) #> [1, 2, 3, 4, 5, 6]
					```
		- removing elements
			- _.remove()_
				- Definition:
					- Removes the first occurrence of a value.
				- Syntax:
					```
					<list_name>.remove(value)
					```
				- Example:
					```
					my_list: list[int] = [1, 2, 3]
					my_list.remove(1) #> [2, 3]
					```
			- _.pop()_
				- Definition:
					- Removes a value specified by its index value, similar to the _del_ keyword.
				- Syntax:
					```
					<list_name>.pop(<index>)
					```
				- Example:
					```
					my_list: list[int] = [1, 2, 3]
					my_list.pop(2) #> [1, 2]
					```
			- _.clear()_
				- Definition:
					- Clears the whole list, leaving an empty list.
				- Syntax:
					```
					<list_name>.clear()
					```
				- Example:
					```
					my_list: list[int] = [1, 2, 3]
					my_list.clear() #> []
					```
		- organiizng elements
			- _.sort()_
				- Definition:
					- Sorts the list alphanumerically.
					- Sorts uppercase strings first then lowercase.
				- Syntax:
					```
					<list_name>.sort
					```
				- Example:
					```
					my_list: list[int] = [2, 3, 1]
					my_list.sort() #> [1, 2, 3]
					```
				- Note:
					- Can be reversed through the reverse argument.
						- Syntax:
							```
							<list_name>.sort(reverse = True)
							```
						- Example:
							```
							my_list: list[int] = [2, 3, 1]
							my_list.sort(reverse = True) #> [3, 2, 1]
							```
			- _.reverse()_
				- Definition:
					- Returns a reverse order of elements in a list.
				- Syntax:
					```
					<list_name>.reverse()
					```
				- Example:
					```
					my_list: list[int] = [2, 3, 1]
					my_list.reverse() #> [1, 3, 2]
					```
		- duplicating lists
			- _.copy()_
				- Definition:
					- Copies lists data collections
					- Instead of sharing the same reference in memory, _.copy()_ changes that.
				- Syntax:
					```
					<list_name1> = <list_name2>.copy()
					```
				- Example:
					```
					my_list: list[int] = [1, 2, 3]
					my_other_list = my_list.copy() #> [1, 2, 3]
					```
		- querying values
			- _.count()_
				- Definition:
					- Used to count the number of occurrences of the specified value.
				- Syntax:
					```
					<list_name>.count(<value>)
					```
				- Example:
					```
					my_list: list[int] = [1, 2, 3]
					my_list.count(1) #> 1
					```
			- _.index()_
				- Definition:
					- Returns the index of specified value in a list.
				- Syntax:
					```
					<list_name>.index(<value>)
					```
				- Example:
					```
					my_list: list[int] = [1, 2, 3]
					my_list.index(2) #> 1
					```

	- tuple methods
		- querying values
			- _.count()_
				- Definition:
					- Used to count the number of occurrences of the specified value.
				- Syntax:
					```
					<tuple_name>.count(<value>)
					```
				- Example:
					```
					my_tuple: tuple[int] = (1, 2, 3)
					my_tuple.count(1) #> 1
					```
			- _.index()_
				- Definition:
					- Returns the index of specified value in a list.
				- Syntax:
					```
					<list_name>.index(<value>)
					```
				- Example:
					```
					my_tuple: tuple[int] = (1, 2, 3)
					my_tuple.index(2) #> 1
					```

	- set methods
		- adding elements
			- _.add()_
				- Definition:
					- Adds elements into a set.
				- Syntax:
					```
					<set_name>.add(<value>)
					```
			- _.update()_
				- Definition:
					- Adds items from another set to the current set.
					- Its not restricted to sets only, it is possible to add lists, tuples or dictionaries.
				- Note:
					- This method updates the original set.
				- Syntax:
					```
					<set_name1>.add(<set_name2>)
					```
		- removing elements
			- _.remove()_
				- Definition:
					- Removes an element in a setd
				- Note:
					- This method will raise an error if the element to be removed is not present.
				- Syntax:
					```
					<set_name>.remove(<value>)
					```
			- _.discard()_
				- Definition:
					- Removes an element in a setd
				- Note:
					- This method will not raise an error is the element to be removed is not present.
				- Syntax:
					```
					<set_name>.discard(<value>)
					```
			- _.pop()_
				- Definition:
					- Removes an element in a setd
				- Note:
					- The item removed is random.
				- Syntax:
					```
					<set_name>.pop()
					```
			- _.clear()_
				- Definition:
					- Clears the set.
				- Syntax:
					```
					<set_name>.clear()
					```
		- duplicating lists
			- _.copy()_
				- Definition:
					- Copies sets.
					- Instead of sharing the same reference in memory, _.copy()_ changes that.
				- Syntax:
					```
					<set_name1> = <set_name2>.copy()
					```
				- Example:
					```
					my_set: set[int] = {1, 2, 3}
					my_other_set: set[int] = my_set.copy() #> {1, 2, 3}
					```
		- joint sets
			- _.union()_
				- Definition:
					- Adds the elements from two sets.
					- It is possible to unionize a set and a tuple, alternative to the | set operator.
				- Note:
					- This method discards any duplicates and must be declared as a new set.
				- Syntax:
					```
					<new_set_name> = <set_name1>.union(<set_name2>)
					```
			- _.intersection()_
				- Definition:
					- Keeps only the duplicates from two sets, alternative to the & set operator.
				- Note:
					- This method discards non-duplicates, must be declared as a new set.
				- Syntax:
					```
					<new_set_name> = <set_name1>.intersection(<set_name2>)
					```
			- _.intersection_update()_
				- Definition:
					- Keeps only duplicates.
					- Updates the original set, instead of requiring a new set.
				- Syntax:
					```
					<set_name1>.intersection_update(<set_name2>)
					```
			- _.difference()_
				- Definition:
					- Keeps only the unique items from the first set, alternative to the - set operator.
				- Note:
					- This method discards duplicates and items from the second set, must be declares as a new set.
				- Syntax:
					```
					<new_set_name> = <set_name1>.difference(<set_name2>)
					```
			- _.difference_update()_
				- Definition:
					- Keeps unique items from the first set.
					- Updates the original set, instead of requiring a new set.
				- Syntax:
					```
					<set_name1>.difference_update(<set_name2>)
					```
			- _.symmetric_difference()_
				- Definition:
					- Keeps items present in both sets, alternative to the ^ set operator.
				- Note:
					- Discards any items that are possible duplicates.
				- Syntax:
					```
					<set_name1>.symmetric_difference(<set_name2>)
					```
			- _.symmetric_difference_update()_
				- Definition:
					- Keeps items present in both sets.
					- Updates the original set, instead of requiring a new set.
				- Syntax:
					```
					<set_name1>.symmetric_difference_update(<set_name2>)
					```
			
	- dictionary methods
		- adding values
			- _.update()_
				- Definition:
					- Updates the value of a key in a dictionary.
				- Note:
					- If the key doesn't exist, adds a new entry.
					- The argument must be a dictionary.
				- Syntax:
					```
					<dict_name>.update({<key>:<value>})
					```
				- Example:
					```
					my_dictionary: dict[str, str] = { "idk" : "Hello" }
					my_dictionary.update({"idk" : "man"}) #> { "idk" : "man" }
					```
		- removing values
			- _.pop()_
				- Definition:
					- Removes items through their key in a dictionary.
				- Syntax:
					```
					<dict_name>.pop(<key>)
					```
				- Example:
					```
					my_dictionary: dict[str, str] = { "idk" : "man" }
					my_dictionary.pop("idk") #> {}
					```
			- _.popitem()_
				- Definition:
					- Removes the last item added in a dictionary.
				- Syntax:
					```
					<dict_name>.popitem()
					```
				- Note:
					- On Python versions before 3.7, _.popitem()_ removes random items.
			- _.clear()_
				- Definition:
					- Clears the items inside a dictionary/
				- Syntax:
					```
					<dict_name>.clear()
					```
		- duplicating dictionaries
			- _.copy()_
				- Definition:
					- Copies dictionaries.
					- Instead of sharing the same reference in memory, _.copy()_ changes that.
				- Syntax:
					```
					<dict name1> = <dict name2>.copy()
					```
				- Example:
					```
					my_dictionary: dict[str, str] = { "idk" : "man" }
					my_other_dictionary = my_dictionary.copy() #> { "idk" : "man" }
					```
		- querying values
			- _.get()_
				- Definition:
					- Returns a the value a key holds inside a dictionary.
				- Syntax:
					```
					<dict_name>.get(<key>)
					```
				- Example:
					```
					my_dictionary: dict[str, str] = { "idk" : "man" }
					my_dictionary.get("idk") #> "man"
					```
			- _.keys()_
				- Definition:
					- Returns all keys inside a dictionary, returning a list.
					- Any changes in the dictionary are reflected on the list.
				- Syntax:
					```
					<dict_name>.keys()
					```
				- Example:
					```
					my_dictionary: dict[str, str] = { "idk : "man" }
					my_dictionary.keys() #> ["idk"]
					```
			- _.values()_
				- Definition:
					- Returns all values inside a dictionary, returning a list.
					- Any changes in the dictionary are reflected on the list.
				- Syntax:
					```
					<dict_name>.values()
					```
				- Example:
					```
					my_dictionary: dict[str, str] = { "idk" : "man" }
					my_dictionary.values() #> ["man"]
					```
			- _.items()_
				- Definition:
					- Returns all items inside a dictionary, returning tuples in a list.
					- Any changes in the dictionary are reflected on the list.
				- Syntax:
					```
					<dict_name>.items()
					```
				- Example:
					```
					my_dictionary: dict[str, str] = { "idk" : "man" }
					my_dictionary.items() #> [("idk", "man")]
					```
			
	- generator methods
		- _.send()_
			- Definition:
				- Allows sending values to a generator.
			- Note:
				- The generator object must first prime the generator using _next()_.
			- Syntax:
				```
				#> assuming <generator_name> is a generator object
				<generator_name>.send(<values>)
				```
			- Example:
				```
				def my_generator() -> str:
					while True:
						my_value = yield
						print(my_value)

				my_generator = my_generator()
				next(my_generator) #> priming the generator object
				my_generator.send("hello") #> "hello"
				my_generator.send("idkman") #> "idkman"
				```
		- _.close()_
			- Definition:
				- Closes the generator object or function.
			- Syntax:
				```
				<generator_name>.close()
				```
			- Example:
				```
				def my_generator() -> str:
					try:
						yield 'yes'
					finally:
						print('no') #> runs when the try block finishes

				my_var = my_generator()
				my_var.close #> runs the finally statement
				```

- User-defined functions
	- Definition:
		- Enables the creation of user-defined functions or methods, these are defined by the programmer.
	- Rules when naming functions:
		- Can contain letters, numbers and underscores \_.
			- But must start with a letter or an underscore.
		- Names are case-sensitive
			- my_function and my_Function are not the same.
		- Functions are used for code repeatability.
			- functions are reusable, removes the hassle of typing the same code over and over again.
		- The name must match the purpose of the function.
		
	- Declaration and definition
		- Definition:
			- Custom methods can either have a return statement or not.
		- Without return statement
			- Syntax:
				```
				def <function_name>() -> <return_type>:
					<statament>
				```
			- Example:
				```
				def my_function() -> None:
					print("idkman")
				```
		- With return statement
			- Syntax:
				```
				def <function_name>() -> <return_type>:
					<statament>
					return <value>
				```
			- Example:
				```
				def my_function() -> int:
					x = 10
					return x
				```
		- Note:
			- The return value can be any value, it can be a collection, a variable, etc.
				- Any code declared after the return statement is considered as useless.
			- After the custom method runs the return statement, it jumps back to the main program, ignoring the code after it.
	
	- functions with parameters
		- Definition:
			- Methods and functions that require an input of data.
			- When declaring a function that requires an input, it is called as a parameter.
			- Multiple inputs are called parameters
		- Syntax:
			```
			def <function_name>(<parameter>) -> <return_type>:
				<stataments>
			```
		- Example:
			```
			def yes(idk) -> None:
				print(idk)
			```
		- Note:
			- Parameters are strictly temporary, it disappears after the function ends.
			- Functions that requires multiple inputs can also have multiple parameters.
				- Example:
					```
					def sum_of_num(x, y, z) -> int:
					return x + y + z
					```
	- access and function calls
		- Definition:
			- Functions are accessed using the method name followed by parentheses _()_.
		- Syntax:
			```
			<function_name>()
			```
		- Example:
			```
			my_function()
			```
	- functions calls with arguments
		- Definition:
			- If a function requires certain parameters, that is called an "argument", or arguments if there are multiple parameters.
			- Calling functions with parameters requires the corresponding arguments.
			- Variables and values are able to be passed as arguments.
		- Syntax:
			```
			<function_name>(<arguments>)
			```
		- Example:
			```
			my_function("yes")
			```
		- Note:
			- When there are multiple arguments needed, the order of the parameters matter.
			- If the order of arguments doesn't match the order of parameters, an error occurs.
				- Example:
					```
					my_function(a, b, c)
					```
			- Arguments can be in the form of keyword arguments (or kwargs)
				- Example:
					```
					my_function(a = 1, b = 2, c = 3)
					```
	- function or method overloading
		- Definition:
			- Multiple functions or methods can have the same name, only if they have different parameters.
			- It is a form of polymorphism.
		- Syntax:
			```
			def <function_name>(<parameters1>) -> <return_type>:
				<stataments>
			def <function_name>(<parameters2>) -> <return_type>:
				<stataments>
			```
		- Example:
			```
			def print_stuff(yes: int) -> None:
				print(yes)
			def print_stuff(no: str) -> None:
				print(no)
			```
	- \*args and \*\*kwargs
		- Definition:
			- Allows a function to accept multiple arguments as input.
		- Arbitraty arguments (\*args):
			- Definition:
				- Allows multiple arguments and stores it in a tuple.
			- Syntax:
				```
				def <function_name>(*<args>) -> <return_type>: #> note that *args can be any name
				#> the single star * is what defines the *args
					<stataments>
				```
			- Example:
				```
				def idkman(*lumbago: int) -> None:
					for i in lumbago:
					print(i)
				```
			- Note:
				- Positional arguments are able to be combined with arbitrary arguments.
				- Do note that positional arguments must be declared first.
					- Syntax:
						```
						def <function_name>(<parameters>, *<args>) -> <return_type>:
							<statements>
						```
					- Example:
						```
						def my_function(my_string: str, *my_num: int) -> None:
							for i in my_num:
								for n in range(i):
									print(my_string)
						```
				- The positional arguments must be satisfied when calling the function.
		- Arbitrary keyword arguments (\*\*kwargs):
			- Definition:
				- Allows passing of multiple keyword arguments, i.e. variables that are defined while calling the function.
				- Stores the received values in a dictionary.
			- Syntax:
				```
				def <function_name>(**<kwargs>) #> note that **kwargs can be any name
				#> the double star ** is what defines the **kwargs
					<statements>
				```
			- Example:
				```
				def my_function(**idkman):
					print(idkman.values())
				```
			- Note:
				- Positional arguments are able to be combined with keyword arguments.
				- Do note that positional arguments must be declared first.
			- Syntax:
				```
				def <function_name>(<parameters>, **<kwargs>) -> <return_type>:
					<stataments>
				```
			- Example:
				```
				def my_function(yes: str, **maybe) -> str:
					print(str)
					return maybe
				```
		- Note:
			- \*args and \*\*kwargs are able to be declared simultaneously.
				- But do note that \*args must come before \*\*kwargs.
				- Syntax:
					```
					def <function_name>(*<args>, **<kwargs>) -> <return_type>:
					<stataments>
					```
				- Example:
					```
					def idkman(*yes, **no) -> None:
					pass
					```
			- It is possible to unpack lists and tuples, or dictionaries when calling \*args and \*\*kwargs functions or methods.
				- \*args
					- Example:
						```
						def idkman(a, b, c) -> None:
							print(b)
							
						my_list: list = [2, 3, 4]
						idkman(*my_list)
						```
					- Note:
						- A star * must be present.
				- \*\*kwargs
					- Example:
						```
						def lumbago(a, b) -> None:
						print(a)
						print(b)
						my_dict = { "a" : "idk", "b": "man" }
						lumbago(**mydict)
						```
					- Note:
						- Double stars ** must be present
			- It is possible to combine positional arguments, \*args, and \*\*kwargs.
				- Do that positional arguments must come first, then \*args, and then \*\*kwargs.
				- Syntax:
					```
					def <function_name>(<parameters>, *<args>, **<kwargs>) -> <return_type>:
						<stataments>
					```
				- Example:
					```
					def my_function(yes, *no, **maybe) -> None:
						pass
					```

	- Decorator functions
		- Definition:
			- Adds more functionality to a function or a method.
			- Does this without altering the code of the original function or method.
			- Takes a function as an input and returns a new function, returns an altered form of the original function and are able to be called multiple times.
		- Declaration and definition
			- Without parameters
				- Syntax:
					```
					def <decorator_name>(func):
						def <function_name>(): #> can be any other name
							<statements>
							return <expression>
						return <function_name>
					```
				- Example:
					```
					def change_to_uppercase(func):
						def to_upper():
							return func().upper()
						retrun to_upper
					```
			- With parameters
				- Definition:
					- It is possible to modify or "decorate" function parameters.
				- Syntax:
					```
					def <decorator_name>(func):
						def <function_name>(<parameters>):
							<statements>
							return <expression>
						return <function_name>
					```
				- Example:
					```
					def my_decorator(func):
						def my_function(*args, **kwargs):
							retrun my_function(*args, **kwargs).lower()
						return my_function
					```
			- Note:
				- Decorators have no control over \*args and \*\*kwargs arguments.
				- To solve this, add \*args and \*\*kwargs to the decorator function.
					- With parameters
						- Definition:
							- Decorators can accept their own arguments, done by adding another wrapper level.
						- Syntax:
							```
							def <decorator_name>(<parameters>):
								def <decorator_name>(func):
									def <function_name>():
										<statements>
										return <expression>
									return <function_name>
								return <decorator_name>
							```
		- Access and calls
			- Definition:
				- Uses the at @ symbol to call the function.
			- Without arguments
				- Syntax:
					```
					@<decorator_name>
					```
				- Example:
					```
					@change_to_upper
					def my_function():
						print("change this to upper")
					```
				- Sample Code:
					```
					def to_lower(func):
						def function_stuff(*idk, **man):
							return function_stuf(*idk, **man).lower()
						return function_stuff

					@to_lower
					def print_stuff(stuff):
						print(stuff)

					print_stuff("IDKMAN")
					```
			- With arguments
				- Syntax:
					```
					@<decorator_name>(<arguments>)
					```
		- Multiple decorators
			- Definition:
				- It is possible to call more than one decorator to work on a single function.
			- Example:
				```
				@my_decorator1
				@my_decorator2
				def my_function():
					pass
				```
		- Preserving metadata
			- Definition:
				- When a function is decorated, metadata is lost.
			- Example:
				```
				def my_decorator(func):
					def my_method():
						return func()
					return my_method

				@my_decorator
				def my_function():
					print('yes')

				print(my_function().__name__) #> my_method
				#> instead of my_function
				```
			- Note:
				- To circumvent this, it is done by importing the _functools_ modules, and using the _functools.wraps(func)_ decorator.
					- Example:
						```
						import functools as ft
						def my_decorator(func):
							@ft.wraps(func):
							def my_method():
								return func()
							return my_method

						@my_decorator
						def my_function():
							pass

						print(my_function().__name__) #> my_function
						```
						
	- Lambda functions
		- Definition:
			- A small anonymous function, it can take any number of arguments but can only have one expression.
		- Syntax:
			```
			lambda <arguments>: <expression>
			```
		- Example:
			```
			lambda x : x + 10
			```
		- Note:
			- Lambda functions are used in variables for quick initialization.
				- Example:
					```
					my_var = lambda yes : yes * 10
					my_var(10) #> 100
					```
			- Commonly used with these functions.
				- With map() function
					- Example:
						```
						map(lambda x : x * 2, [1, 2, 3]) #> returns a list object
						#> [2, 4, 6]
						```
				- With filter() function
					- Example:
						```
						filter(lambda x : x % 3 != 0, [1, 2, 3]) #> returns a list object
						#> [1, 2]
						```
				- With sorted() function
					- Example:
						```
						sorted([3, 1, 2, 5, 4], key = lambda x : x[1])
						sorted(['apple', 'banana', 'cherry'], key = lambda x : len(x))
						```

	- Recursive functions
		- Definition:
			- Also called "recursions", occurs when a function calls itself.
			- Recursive functions can be very dangerous when there are no end conditions, as it can lead to memory hog or performance loss.
				- Due to it never ending, eating up resources.
			- By default, Python has a default of 1000 recursive calls, this is queried through the _sys_ module.
		- Example:
			```
			import sys
			sys.getrecursionlimit() #> returns recursion limit
			sys.setrecursionlimit(200) #> sets recursion limit to 2000
			```
		- Note:
			- It is recommended to use iteration when handling very deep recursions.
				- Syntax:
					```
					def <function_name>(<parameters>) -> <return_type>:
						<base_cases> #> to prevent endless recursions
						return <function_name>(arguments) <expression>
	
					<function_name>(<arguments>)
					```
				- Example:
					```
					#> factorial sequence
					def factorial(n: int) -> int:
						if n == 1 or n == 0:
							return 1
						return n * factorial(n - 1)

					#> sum of list
					def sum_list(numbers) -> int:
						if len(numbers) == 0:
							return 0
						else:
							return numbers[0] + sum_list(numbers[1:])
	
					#> max number in list	
					def find_max(numbers) -> int:
						if len(numbers) == 1:
							return numbers[0]
						else:
							max_of_rest = find_max(numbers[1:])
						return numbers[0] if numbers[0] > max_of_rest else max_of_rest
					```
		- Two parts of a recursive function:
			- Base case:
				- Conditions that terminate the recursion
			- Recursive case:
				- The function calling upon itself with modified arguments.
				- It can be a return statement or a function call.

	- generator functions
		- Definition:
			- A form of function that can pause and resume their execution.
			- When called, it returns a generator object which is a iterable.
			- It uses the yield keyword.
			- Generators are able to save memory, due to it generating values on the fly.
			- Unlike normal functions that saves the entire range of values all at once.
		- Syntax:
			```
			def <generator_name>():
				<statements>
				yield <expression>
			```
		- Example:
			```
			def my_generator():
				yield 5
			```
		- Note:
			- Generators are able to be advanced using the next() function
				- Syntax:
					```
					next(<generator_variable>)
					```
				- Example:
					```
					def generator():
						yield 1
						yield 2
					
					my_generator = generator()
					next(my_generator) #> 1
					next(my_generator) #> 2
					```
			- When there are no longer any values to yield, the next manual advance will result in a StopIteration error.
				- Example:
					```
					def my_generator():
						yield 1 #> gives only one value

					my_var = my_generator()
					next(my_var)
					next(my_var) #> StopIteration
					```
		- Generator expressions
			- Definition:
				- Similar to list comprehension, it is possible to create generators with parentheses _( )_ instead of square brackets.
			- Syntax:
				```
				<variable_name> = (<expression>)
				```
			- Example:
				```
				my_var = (x * x for x in range(5))
				```
		- Generator control
			- Definition:
				- Generators has methods for controlling generator functions, refer to generator methods for more info.