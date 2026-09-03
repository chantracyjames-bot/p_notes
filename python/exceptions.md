
# Exceptions
- Exception Handling
	- Definition:
		- Python has five main ways of exception handling.
	- Types of exception handling statements:
		- _try_
			- Definition:
				- Runs a block of code and "tests" for errors or exceptions while being executed, any errors will be intercepted by the except statement.
			- Syntax:
				```
				try:
					<stataments>
				```
			- Example:
				```
				try:
					print("lumbago")
				```
		- _except_
			- Definition:
				- Runs a block of code after the an exception is encountered.
				- It can catch any exceptions in a program from broad to specific exceptions
			- Note:
				- In order to use an _except_ statement, it requires a _try_ statement before it.
			- Syntax:
				```
				except <exception>:
					<statament>
				```
			- Example:
				```
				except: #> catches all exceptions
					print('error')
				```
		- _finally_
			- Definition:
				- Runs regardless of the result of the try-except statements, or runs after a try-except.
			- Note:
				- In order to use a _finally_ statement, it requires a _try_ and _except_ statement before it.
			- Syntax:
				```
				finally:
					<statement>
				```
			- Example:
				```
				finally:
					print('code finished')
				```
		- _else_
			- Definition:
				- Runs only if the _try_ and _except_ statements returns no errors.
			- Note:
				- In order to use an _else_ statement in exception handling, a _try_ and _except_ statement is required.
			- Syntax:
				```
				else:
					<statements>
				```
			- Example:
				```
				else:
					print('no errors')
				```
		- _raise_
			- Definition:
				- Used to manually throw or raise exceptions, typically used in a _try-except_ statement.
			- Note:
				- A _raise_ statement is able to be used outside but do note that the program will stop after an exception is thrown.
			- syntax:
				```
				raise <exception>
				```
			- Example:
				```
				raise ArithmeticError
				```
	- Note:
		- Multiple _except_ blocks are able to declared in a try-except statement, helping in handling multiple exceptions by being more specific by targeting specific Exceptions.
			- Example:
				```
				try:
					my_list: list[int] = [1, 2, 3, 4]
					my_list[5] #> IndexError
					my_list[1] / 0 #> ZeroDivisionError
				except IndexError as err:
					print('index out of bounds yo')
				except ZeroDivisionError as err:
					print('idiot, cannot by zero bro')
				finally:
					print('program finished')
				else:
					print('program finished without errors, 5 stars')
				```