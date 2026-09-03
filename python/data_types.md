
# Data Types
- Definition:
	- Python has 8 data types, being a text type, numeric type, sequence type, mapping type, set type, boolean type, binary type and none type
- Text Type:
	- _str_
		- Definition:
			- _str_, or strings, stores string or text values, encased in either single or double quotation marks
				- Single quotes _' '_.
				- Double quotes _" "_.
		- Note:
			- Strings are arrays
				- While python doesn't have a char type like other languages, a single character is a string with a length of 1.
			- Strings are immutable
				- String cannot be modified after being declared.
		- Example:
			```
			"Hello World"
			'idkman'
			```
		- Type Casting:
			- Definition:
				- Values are able to be casted as _str_ using the _str()_ class.
			- Syntax:
				```
				str(<value>)
				```
			- Example:
				```
				str("Hello World")
				
				str('idkman')
				```
		- Multi-line strings
			- Definition:
				- It is possible to have string that span multiple lines, done through the use of triple quotes.
					- single quotes _''' '''_.
					- double quotes _""" """_.
				- It is commonly used for documentation.
- Numeric Type:
	- _int_
		- Definition:
			- _int_, or integer, are whole numbers.
		- Note:
			- declaring integers must be done without decimals.
		- Example:
			```
			1, 2, 3, 4, 5
			```
		- Type Casting
			- Definition:
				- Values are able to be casted as _int_ using the _int()_ class.
			- Syntax:
				```
				int(<value>)
				```
			- Example:
				```
				int(23)
				int("12")
				```
		- Note:
			- Using string values when casting must only be numeric values.
			- Casting with letters or a mix of letters and numbers values will result into errors.
	- _float_
		- Definition:
			- _float_, or floating points, are decimal numbers.
		- Note:
			- It can be declared with or without decimals.
		- Example:
			```
			3.14, 4.19, 5.15
			```
		- Type Casting:
			- Definition:
				- values are able to be casted as _float_ using the _float()_ class
			- Syntax:
				```
				float(<value>)
				```
			- Example:
				```
				float(6.12)
				float"1.11")
				```
		- Note:
			- Using string values when casting must only be numeric values.
			- Casting with letters or a mix of letters and numbers values will result into errors.
	- _complex_
		- Definition:
			- _complex_, or complex numbers, are combinations of real and imaginary numbers.
			- j or J represents the imaginary number, commonly represented as R + iJ
				- Where:
					- R is the real number.
					- iJ is the imaginary number
		- Example:
			```
			7j, 2 + 3j, 10J
			```
		- Type Casting:
			- Definition:
				- Values are able to be casted as _complex_ using the _complex() _class.
			- Syntax:
				```
				complex(<value>)
				```
			- Example:
				```
				complex(3 + 7j)
				complex("2+6J")
				```
			- Note:
				- Using string values when casting must be in the form of complex numbers, the string value must also not contain spaces.
				- Casting with any other string value will result into errors
- Boolean Type
	- _bool_
		- Definition:
			- _bool_, or booleans, contains a boolean value, either a _True_ or a _False_.
		- Example:
			```
			True
			1
			"yes"
			```
		- Note:
			- Any value can be a boolean, called _truthy_ values.
			- Numeric values aside from 0 are _True_, with 0 being _False_
			- Text values aside from an empty string are _True_, with _""_ being _False_.
			- Collections aside from an empty collection are _True_, an empty _[]_, _{}_ or _()_ is _False_.
		- Type Casting
			- Definition:
				- Values are able to be casted as a boolean using the _boolean() _class.
			- Syntax:
				```
				boolean(<value>)
				```
			- Example:
				```
				bool(True)
				bool(0) #> False
				bool("yes") #> True
				```
- Sequence Type:
	- _list_
		- Definition:
			- Contains ordered and mutable collections of values, allowing duplicate entries.
		- Note:
			- Lists are denoted by the brackets _[ ]_ symbol, anything inside the brackets are considered as an element of that _list_.
		- Example:
			```
			[1, 3.14, "idkman"]
			```
		- Type Casting
			- Definition:
				- Values or collections are able to be casted as a _list_ using the _list()_ class.
			- Syntax:
				```
				list(<iterable>)
				```
			- Example:
				```
				list([1, 2, 3])
				list("yes")
				```
			- Note:
				- Tote that the value required by the _list()_ class must be an iterable.
				- It can be another _list_, _tuple_, _dictionary_, _set_, or strings
	- _tuples_
		- Definition:
			- Contains ordered and immutable collections of values, allows duplicate entries. 
		- Note:
			- Tuples are denoted by the parenthesis ( ) symbol, anything inside the parentheses are considered as a tuple.
		- Example:
			```
			(1, 3.14, "lumbago")
			```
		- Type Casting
			- Definition:
				- Values or collections are able to be casted as a _tuple_ using the _tuple()_ class.
			- Syntax:
				```
				tuple(<iterable>)
				```
			- Example:
				```
				tuple((4, 5, 6))
				tuple("no")
				```
			- Note:
				- The values required by the _tuple()_ class must be an iterable.
				- It can be another _tuple_, _list_, _dictionary_, _set_, or strings.
	- _range_
		- Definition:
			- Are a range of values, and the value inside must be an integer.
		- Note:
			- declaring a _range_ object uses the _range()_ class.
		- Syntax:
			```
			range(<start>, <stop>, <step>)
			```
		- Example
			```
			range(5)
			range(1, 4)
			range(2, 6, 3)
			```
- Mapping Type:
	- _dict_
		- Definition:
			- _dict_, short for dictionaries, contains unordered and mutable collection of pairs of values.
			- Pairs must be in the form of keys and value, keys duplicates are not allowed and value duplicates are allowed.
		- Example:
			```
			{"yes": "no", "idkman": "lumbago", "Hello": "World"}
			```
		- Type Casting
			- Definition:
				- Values or collections are able to be casted as a _dict_ using the _dict()_ class.
			- Syntax:
				```
				dict(<dictionary>)
				#> or
				dict(<variable1> = <value1>, <variable2> = <value2>)
				```
			- Example:
				```
				dict({"idk": "man"})
				```
			- Note:
				- The _dict()_ class can only take in dictionary objects or a _list_ of variable declarations.
- Set Type:
	- _set_
		- Definition:
			- Contains unordered and immutable collections of values, does not allow duplicate entries.
		- Example:
			```
			(1, 10, 3, "maybe", False)
			```
		- Type Casting
			- Definition:
				- Values or collections are able to be casted as a _set_ using the _set()_ class
			- Syntax:
				```
				set(<iterable>)
				```
			- Example:
				```
				set((1, 2, 3, "yes"))
				```
			- Note:
				- The value required by the _set()_ class must be an iterable.
				- It can be another _set_, _list_, _tuple_, _dict_, or strings
	- _frozenset_
		- Definition:
			- a "frozen" form of a regular set, it does not allow any modifications to the set.
		- Example:
			```
			frozenset(1, "maybe", True)
			```
		- Type Casting:
			- Definition:
				- Values or collections are able to be casted as a _frozenset_ using the _frozenset()_ class.
			- Syntax:
				```
				frozenset(<set>)
				```
			- Example:
				```
				frozenset(("yes", "maybe", False))
				```
			- Note:
				- The value required by the set() class must be an iterable.
				- It can be another _set_, _list_, _tuple_, _dict_, or strings.
- Binary Type
	- _bytes_
		- Example:
			```
			bytes(4)
			```
	- _bytearray_
		- Example:
			```
			bytearray(2)
			```
	- _memoryview_

- _NoneType_
	- _None_
		- Definition:
			- Represents no type, a special constant in Python.
			- Is the absence of a value and it is the only instance of the _NoneType_ object.
			- Commonly used to set a variable to 'no value' or 'not set', and evaluates as _False_ in a boolean context.
		- Note:
			- Functions with no return statements return None by default
		- Example:
			```
			x = None
			```

  
