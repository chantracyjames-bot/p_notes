
# Syntaxes
## Statements
- Definition:
	- A statement is a single (or multiple) line of code doing once particular task.
	- i.e. initializing a variable, declaring a loop, a function, etc.
- Semicolons
	- Definition:
		- Unlike C/C++, Java or similar languages, Python doesn't need a semicolon to end statements, it is still possible to use semicolons but it is generally unadvised.
		- Semicolons are used to chain multiple statements in a single line.
	- Example:
		```
		m = 10; n = 'Hello'; yes = False
		```
	- Note:
		- It is not recommended to use semicolons due to it not being the Pythonic way to code as it can also make code unreadable.
- Indentation
	- Definition:
		- Python requires indents for compound statements to run.
		- Statements like a loop, coditional, function declaration, etc.
	- Note:
		- Compound statements without indents will throw an error, called _IndentationError_.
		- A compound statement requires a colon to be considered as one.
	- Example:
		```
		while (true):    #> colon signifies a compound statement
			print("yes") #> substatements must be indented
		```
## Case-sensitivity
- Definition:
	- Python is case-sensitive when it comes to naming.
	- true and True are different things.

## Numbers and Text
- Numbers
	- Definition:
		- Numbers in python don't need to be encased in quotes, doing so will convert them into string.
	- Example:
	   ```
	   my_num = 100
	   yes = 1
	   ```
- Text
	- Definition:
		- Text in python must be wrapped in either single or double quotes.
			- single quotes ' '
			- double quotes " "
	- Example:
		```
		my_string = 'Hello World'
		idkman = "lumbago"
		```
	- Concatenation
		- Definition:
			- Numbers and string cannot be added together through the use of the addition + operator, doing so results into a _TypeError_.
			- _f-strings_ are design to circumvent this
		- _f-strings_
			- Definition:
				- A type of string that is formatted.
				- Replaces the old _.format()_ method.
				- To declare an f-string, the letter "f" must be the prefix of a string literal.
		   - Syntax:
				```
				f'<value>'
				#> or
				f"<value>"
				```
		   - Example:
				```
				f'yes and yes'
				#> or
				f"idkman"
				```
			- Note:
				- To add other variable or elements to form a string, they must be enclosed in curly braces _{ }_.
				   - These are commonly called as placeholders, as operations are able to declared inside placeholders.
				   - It allows adding, multiplying, etc., and it also allows conditional statements, mainly the shorthand if else statements.
				   - Function or method executions are also allowed inside placeholders.
				   - Syntax:
						```
						f'{<value>}'
						#> or
						f"{<value>}"
						```
				   - Example:
						```
						f'the sum is: {10 + 10}'
						#> or
						f"{100} is my number"
						```
				- String modifiers are possible in f-strings.
				   - A colon _:_ suffix must be declared in the variable.
				   - Syntax:
						```
						f'{<variable>:<modifiers>}'
						#> or
						f"{<variable>:<modifiers>}"
						```
				   - Example:
						```
						f'pi is {3.141592:f}' #> pi is 3.14
						#> or
						f"{'idkman':10s yes}" #> idkman    yes
						```
## Naming Conventions
- Definition:
	- There are industry convention when naming certain elements in Python.
- Attributes and variables
	- Usually in snake_case.
	- Example:
		```
		my_string = "idkman"
		my_bool = True
		```
- Functions and methods
	- Usually in snake_case
	- Example:
		```
		my_method()
		sum_result()
		```
- Filenames and folders
	- Usually in snake_case
	- Example:
		```
		my_program.py
		odd_or_even.py
		```
- Classes and enumerations
	- Usually in PascalCase
	- Example:
		```
		MyClass()
		InventoryClass()
		```
- Constants and enum values
	- Usually in SCREAMING_SNAKE_CASE
	- Note 
		- Python does not have a constant keyword, the naming convention notifies to other developers that the value is not going to be changed throughout the program.
		- it is by convention to name unchanging values in SCREAMING_SNAKE_CASE
	- Example:
		```
		CONSTANT_VAR = "immutable"
		SUNNY_DAY
		```

## Scope
- Definition:
	- By default, the compiler (or interpreter) reads code from top to bottom, the first line until the last line of the file.
	- Calling a variable that is not defined until later in the code will throw an error.
- Example:
	```
	print(sum)    -> Error
	sum = 10 + 10 #> sum is decalred later
	```
- Python uses the LEGB rule
	- Local
		- Inside the current function or compound statement.
	- Enclosing
		- Inside the enclosing function or nested statement.
	- Global
		- At the top level or lowest level indentation.
	- Built-in
		- Uses Python's namespace
- Built-in functions
	- Definition:
		- Are also called local variables.
		- If the variables are declared inside a user-defined function or method.
		- The variable/s created is/are a local variable.
	- Example:
		```
		def my_function():
		x = 100        #> declared inside a local function
		print(x)       #> 100
		print(x)           -> Error
					  #> it doesn't see x
		```
- Global variables
	- Definition:
		- It is possible to declare a variable as global even if its located locally.
		- It uses the _global_ keyword.
	- Syntax:
		```
		global <variable>
		```
	- Example:
		```
		def my_function():
			global x
			x = 10
		print(x)           #> 10
		```

## Python keywords
- _global_
	- Definition:
		- Declares the variable as global, creating the variable if it doesn't exist.
	- Note:
		- The keyword is usually unadvised to use, as passing arguments are more preferred.
	- Syntax:
		```
		global <variable_name>
		<variable_name> = <value>
		```
	- Example:
		```
		yes = 10
		def my_function():
			global yes
			yes = 100
		```
- _nonlocal_
	- Definition:
		- Lets the variable be assessible by the outer function.
	- Note:
		- The statement will fail if the variable doesn't exist.
	- Syntax:
		```
		nonlocal <variable_name>
		<variable_name> = <new_value>
		```
	- Example:
		```
		def my_outer():
			x = 10
		def my_inner():
		   nonlocal x
		   x = "no"
		```
- _del_
	- Definition:
		- Similar to the _.remove()_ method, removes the pointer associated with the variable.
		- Renders the variable name useless.
	- Syntax:
		```
		del <variable_name>
		```
	- Example:
		```
		del x
		```
	- Note:
		- The keyword can also be used to remove elements in a list of tuple.
			- Syntax:
				```
				del <list_name>[<index>]
				```
			- Example:
				```
				del my_list[1]
				```
- _pass_
	- Definition:
		- Allows statements to be declared with empty blocks of codes, useful for placeholder code.
		- Used to bypass the _IndentationError_.
	- Syntax:
		```
		#> inside an empty statement
		pass
		```
	- Example:
		```
		def empty_func():
		   pass
		```
- _def_
	- Definition:
		- Used to create user-defined functions, refer to methods for more information.
	- Note
		- The the methods must be defined, failing to do so results in an error.
		- The _pass_ keyword is able to be used to bypass this error.
	- Syntax:
		```
		def <method_name>():
			<statements>
		```
	- Example:
		```
		def my_func():
		```
- _yield_
	- Definition:
		- Used to pause functions, generally used in generator functions.
		- refer to generator functions on methods for more information.
	- Syntax:
		```
		#> inside a generator function
		yield <value>
		```
	- Example:
		```
		def my_generator():
		yield 10
		```
## escape sequences
- _\n_
	- the most common escape sequence
	- represents a new line
- _\t_
	- represents a horizontal tab rule
- _\\\\_
	- represenst a single backslash as text
- _\\"_
	- represents a single double quote as text
- _\\'_
	- represents a single single quote as text
- _\b_
	- represenst a single backspace
- _\r_
	- represents a Carriage Return
- _\f_
	- represents a Form Feed
- _\ooo_
	- represents an octal value
- _\xhh_
	- represents a hex value

