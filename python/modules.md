# Modules
- Built-in modules
	- _datetime_
		- Definition:
			- Imports datetime objects, allowing to work on date and time.
		- Classes:
			- _date_
				- Represents a date; year, month or day.
				- Based on the Gregorian Calendar
			- _time_
				- Represents a time; hour, minute, second, microsecond or tzinfo (timezoneinfo).
				- It is independent of any date.
			- _datetime_
				- It combines both date and time; year, month, day, hour, minute, second, microsecond and tzinfo.
			- _timedelta_
				- Represents the difference between two dates or times.
			- _tzinfo_
				- An abstract base class for timezene information.
			- _timezone_
				- A fixed offset class, a subclass of _tzinfo_
	- _math_
		- Definition:
			- Extends the list of mathematical functions, refer to methods.md for base Python math modules.
		- Methods
			- _math.sqrt()_
				- Definition:
					- Returns the square root of a number.
				- Syntax:
					```
					math.sqrt(<number>)
					```
			- _math.ceil()_
				- Definition:
					- Returns the nearest ceiling rounding operation.
				- Syntax:
					```
					math.ceil(<number>)
					```
			- _math.floor()_
				- Definition:
					- Returns the nearest floor rounding operation.
				- Syntax:
					```
					math.floor(<number>)
					```
			- _math.pi_
				- Definition:
					- Returns the value of pi, which is a constant value.
				- Syntax:
					```
					math.pi
					```
	- _re_
		- Definition:
			- Short for regular expressions, or RegEx.

	- _json_
		- Definition:
			- Stands for JavaScript objext notation.
		- Methods:
			- _.loads()_
				- Definition:
					- Used for parsing JSON to Python.
				- Syntax:
					```
					json.loads(<json>)
					```
				- Example:
					```
					#> example json file as a variable
					json_test = '{ "yes":"no", "idk":"man", "Hello":"World"}'
					
					json.loads(json_test) #> converts the json into a Python dict object
					```
			- _.dumps()_
				- Definition:
					- Used for dumping Python to JSON.
				- Syntax:
					```
					json.dumps(<dict_name>)
					```
				- Example:
					```
					dict_test = '{ "yes":"no", "idk":"man", "Hello":"World"}'
					
					json.dumps(dict_test) #> converts the dict object into a json string
					```
				- Note:
					- This method has an indent, separators and sort_keys parameters.
						- _json.dumps(\<dict>, indent=\<number>)_
							- Specifies the amoount of spaces per indent.
						- _json.dumps(\<dict>, separators=\<separators>)_
							- Specifies the separators to use, the default value is (",", ":").
						- _json.dumps(\<dict>, sort_keys=\<bool>)_
							- Specifies if the keys should be sorted or not, it is either a True or a False.
			- List of objects convertible into JSON strings:
				- dict: Object
				- list: Array
				- tuple: Array
				- str: String
				- int: Number
				- float: Number
				- bool: true or false
				- None: null

- Python PIP
	- Definition:
		- It is Python's package manager, used to install packages and modules online.
		- Do note that it has to be used in Python's terminal, used for downloading a package.
	- Syntax:
	```
	pip install <package>
	```
	- Example:
	```
	pip install camelcase
	```
	- Using a package
		- Syntax:
		```
		#> inside a Python file
		import <package>
		```
		- Example:
		```
		import camelcase
		```
	- Removing a package
		- Syntax:
			``pip uninstall <package>``
		- Example:
		```
		pip uninstall camelcase
		```
	- List packages install
		- Syntax:
		```
		pip list
		```

  

- User-defined modules
	- Definition:
		- A file containing a set of functions, methods, or classes.
		- Similar to packages in Java.
		- User-defined modules are created by creating and defining a Python file (.py).
		- By default, Python looks for modules in the same folder as the current file.
	- Note:
		- Changing paths are done view the use of the sys module.
			- example:
				```
				import sys
				sys.path.append(/home/tarcy_arch/Documents/Programming/python/learning)
				#> Python will then look inside this path (folder) for modules when importing
				```
	- Importing modules:
		- Definition:
			- To import a module, the import keyword is used.
		- Note:
			- Importing user-defined modules will require the filename without extensions.
		- Syntax:
			```
			import <module_name>
			```
		- Example:
			```
			#> importing a custom module named my_module.py
			import my_module
			```
		- Note:
			- To import a module with an alias, the _as_ keyword is added.
				- Syntax:
					```
					import <module_name> as <alias>
					```
				- Example:
					```
					import my_module as custom_mod
					```
			- To import a single attribute in a module, the _from_ keyword is used.
				- Syntax:
					```
					from <module_name> import <attribute>
					```
				- Example:
					```
					#> importing a function called my_function
					from my_module import my_function
					```
			- When a module is imported, all of its attributes are available.
				- Attributes like collections, functions, methods and classes, e.g. lists, tuples, dictionaries, etc.
				- Example:
					```
					import my_module
					
					#> accessing a tuple named my_tuple in my_module
					my_module.my_tuple
					
					#> accessing a function called my_function()
					my_module.my_function()
					```
			- Viewing and accessing the available attributes of a module is done through the _dir()_ function.
				- Syntax:
					```
					dir(<module_name>)
					```
				- Example:
					```
					dir(my_module)
					```