
# Iteratives
- Definition:
	- Commonly called as loops.
	- Runs a code block until a certain condition is met, may it be until the loop counter reaches a certain number, the condition becomes false, etc.
	- Uses a boolean value to dictate if the loop runs or stops.
- Note:
	- using loop counter values other than whole numbers will cause errors.
- Loop keywords
	- _break_
		- The break keyword is used to stop loops, or ending it prematurely.
	- _continue_ 
		- The continue keyword is used to skip the current iteration, using it will end the current iteration and move on to the next.
- Types of loops:
	- _while_
		- Definition:
			- Runs a loop while the condition is true.
		- Note:
			- If the initial condition is false, the loop never runs.
		- Syntax:
			```
			while (<condition>) {
				<statements>
			}
			```
		- Example:
			```
			while (10 > 11) {
				printf("lumbago");
			}
			```
	- _do-while_
		- Definition:
			- A variant of the _while_ loop.
			- Unlike the _while_ loop, this loop runs the block of code first before checking the condition.
		- Note:
			- It always runs the statements once and stops when the condition becomes false.
		- Syntax:
			```
			do {
				<statements>
			} while (<condition>)
			```
		- Example:
			```
			do {
				printf("idkman");
			} while (29 < 1);
			```
	- _for_
		- Definition:
			- An extensive type of loop.
			- Runs a loop while the condition is true
		- Note:
			- If the initial condition is false, the loop never runs
		- Syntax:
			```
			for(<statement1>; <statement2>; <ststement3>) {
				<statement>
			}
			```
			- Where
				- statement1
					- Executed before the code block, usually is reserved for initializing the loop counter (or variable).
				- statement2
					- Represents the condition of the loop, usually is reserve for conditional operations.
				- statement3
					- Executed after the code block, usually is reserved to increment or decrement the loop counter (or variable).
		- Example:
			```
			for(int i = 0; i < 10; i++) {
				printf("yes");
			}
			```