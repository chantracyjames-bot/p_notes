
# Iteratives
- Definition:
	- Common called as loops, as it runs a code block until a certain condition is met.
	- Runs until the loop counter reaches a certain condition, or the condition becomes false, etc.
	- It uses a boolean value to dictate if the loop runs or stops.
	- Using loop counter values other than whole numbers will case errors, except in the case of iterables.
- Note:
	- The _else_ statement:
		- Definition:
			- Unlike what the name suggests, it runs after the loop has been finished.
			- It only runs if the loop runs without interruptions.
		- Syntax:
			```
			while (<condition>):
				<statements>
			else:
				<statements>
			
			#> or
			
			for <expression>:
				<statements>
			else:
				<statements>
			```
		- Example:
			```
			while (True):
			break
			else:
			print("lumbago")
			```
- Loop keywords:
	- _break_
		- The break keyword is used to stop loops, breaking a loop ends it prematurely.
	- _continue_
		- The continue keyword is used to skip the current loop iteration, using it will end the current iteration and move on to the next.
- Types of loops:
	- _while_
		- Definition:
			- Runs a block of statement while the condition is True.
			- If the initial condition is false, the loop never runs.
		- Syntax:
			```
			while(<condition>):
				<statements>
			```
		- Example:
			```
			while (True):
			print(yes) #> note that this will get printed infinitely
			```
	- _for_
		- Definition:
			- An extensive type of loop.
			- Differs from other loops from different languages with the same name.
			- It is a type of loop that uses an iterable instead of a loop counter, which can either be a list, tuple, string, etc.
			- For instance, it can be used with the range() function.
		- Syntax:
			```
			for <expression>:
				<stataments>
			```
		- Example:
			```
			for i in range(10):
			print("idkman")
			```
- Iterators
	- Definition:
		- Objects that contains countable elements, or is an object that can be iterated upon.
		- Meaning, it is traversable values or objects.
		- An iterator is an object which implements the iterator protocol, consisting of the _next_() and _next_() methods
- Iterables
	- Definition:
		- It is a container which can possess an iterator, i.e. lists, tuples, dictionaries, etc.
		- Do note that strings are also iterable objects.
		- These objects have a iter() method which is used to get an iterator, using the iterator of an iterable
	- Example:
		```
		my_list: list = [1, 2, 3, "yes"]
		my_iterator: = iter(my_list)
		
		next(my_iterator) #> 1
		next(my_iterator) #> 2
		next(my_iterator) #> 3
		next(my_iterator) #> "yes"
		next(my_iterator) #> StopIteration
		```
	- Iterators are commonly used in a loop, which leveraging iterables.
		- Example:
			```
			my_string: str = 'idkman'
			for i in my_string:
				print(i)
			```
	- Creating custom iterators:
		- Definition:
			- Uses the __iter__() and __next__() methods to initialize and advance an iterable.
		- Example:
			```
			class MyNumbers:
				def __iter__(self) -> MyNumbers:
					self.a: int = 1
					return self
				def __next__(self) -> int:
					x: int = self.a
					self.a += 1
					return x
					
			my_obj: MyNumbers = MyNumbers
			my_iterator = iter(my_obj)    #> initializes the __iter__() method
											#> sets the first element to be 1
			print(next(my_iterator))      #> 1
										  #> next() returns the current value
											#> and then initializes the next element, 1 += 1 (2)
			```
	- Stopping iterators:
		- Definition:
			- To stop the iteration from going on forever or to set a limit, the StopIteration statement is used
		- Example:
			```
			class MyNumber:
				def __iter__(self) -> MyNumber:
					self.yes: int = 1
					return self
				def __next__(self) -> int:
					if self.yes >= 10:
						no: int = self.yes
						self.yes += 1
						return no
					else:
						raise StopIteration #> stops the iteration after 10 next() calls
			```