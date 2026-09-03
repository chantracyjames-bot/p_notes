
# Conditionals
- Definition:
	- Conditional statements control the flow of the program.
	- It uses boolean as the logic with the conditional expressions controlling the value of said boolean.
- Note:
	- All conditional operators must return a boolean value, either a _True_ or a _False_.
- Types of conditional statements:
	- _if_
		- Definition:
			- only runs the if the condition is _True_
		- Syntax:
			```
			if <condition>:
				<statements>
			```
		- Example:
			```
			if 10 > 9:
				print("yes")
			```
	- _elif_
		- Definition:
			- Offers another condition apart from the if statement, having similar syntax as the if statement.
		- Note:
			- In order to create an _elif_ statement, an _if_ statement must precede it.
		- Syntax:
			```
			elif <condition>:
				<statements>
			```
		- Example:
			```
			elif (10 < 8):
				print("no")
			```
		- _else_
			- Definition:
				- It only runs if all conditions are _False_.
			- Note:
				- In order to use an _else_ statement, an _if_ or _elif_ statement must precede it.
			- Syntax:
				```
				else:
					<statements>
				```
			- Example:
				```
				else:
					print("maybe")
				```
		
		- _match_
			- Definition:
				- An alternative approach to the if-elif-else statements, offering a clean and organized approach.
				- It is similar to the switch-case statement in Java, having a _case_ statement for each condition.
			- Note:
				- the _case_ statement is similar to the if and elif statements, being a conditional statement where it runs the code block if is _True_.
				
				- case _ acts as the default statement, running if all case conditions are _False_.
			- Syntax:
				```
				match <expression>:
					case <condition>:
						<statements>
					case _:
						<statements>
				```
			- Example:
				```
				match (10):
					case 100:
						print("maybe")
					case 1:
						print("no")
					case _:
						print("yes")
				```
- Chaining and Nesting
	- Conditional statements are about to be chained together.
		- For instance, an _if_, _elif_, and _else_ statements are about to become an _if-elif-else_ statement.
		- _if-else_ statements
			- Definition:
				- A combination of the _if_ and _else_ stataments.
			- Example:
				```
				if (100 == 28):
					print("Hello")
				else:
					print("World")
				```
		- _if-elif-else_ statements
			- Definition:
				- A combination of if, elif and else if statements 
			- Note:
				- Multiple elif statements are possible.
			- Example:
				```
				if ("idkman" == "lumbago"):
					print("no")
				elif ("yes" == "maybe"):
					print("probs")
				elif (True is False):
					print(10)
				else:
					print(3.14)
				```
	- Nesting conditional statements inside of each other is possible:
		- Example:
			```
			if 100 == 100:
				if True is True:
					print("yes")
			```