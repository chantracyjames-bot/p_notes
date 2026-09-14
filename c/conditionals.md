
# Conditionals
- Definition:
	- Conditional statements control the flow of the program.
	- It uses boolean as the logic with conditional operations controlling the resulting booleans.
- Note:
	- All conditional operators must return a boolean value.
- types of conditional statements:
	- _if_
		- Definition:
			- Only runs the code block if the condition is _true_.
		- Syntax:
			```
			if (<condition>) {
				<statements>
			}
			```
		- Example:
			```
			if (10 > 29) {
				printf("no"); // runs since condition is true
			}
			```
	- _else if_
		- Definition:
			- Offers another condition apart from the _if_ statement, similar syntax as the if statement.
		- Syntax:
			```
			else if (<condition>) {
				<statements>
			}
			```
		- Example:
			```
			if (7 < 2) {
				printf("no"); // does not run since condition is false
			}
			else if (9 > 2) {
				printf("yes"); // runs since condition is true
			}
			```
	- _else_
		- Definition:
			- Runs if all of the conditions from the _if_ and _else_ statements return _false_.
		- Syntax:
			```
			else {
				<statements>
			}
			```
		- Example:
			```
			if (1 > 9) {
				printf("no"); // does not run since condition is false
			}
			else {
				printf("maybe"); // runs since all condition are false
			}
			```
	- _if-else_
		- Definition:
			- A combination of the _if_ and _else_ statements
		- Example:
			```
			if (90 == 12) {
				printf("no");
			}
			else {
				printf("maybe");
			}
			```
	- _if-else if-else_
		- Definition:
			- A combination of the _if_, _else if_ and _else_ statements.
		- Example:
			```
			if (90 == 12) {
				printf("no");
			}
			else if (75 != 89) {
				printf("yes");
			}
			else {
				printf("maybe");
			}
			```
	- _switch_
		- Definition:
			- An alternative approach to _if-else if-else_ statements, offering a cleaner and more organized approach.
		- Syntax:
			```
			switch (<expression>) {
				case <condition>:
					<statements>
					break;
				case <condition>:
					<statements>
					break;
				default:
					<statements>
					break;
			}
			```
			- Where
				- _case_
					- The _case_ condition is similar to the _if_ and _else if_ statements, being a conditional statement.
					- It runs the code block if is _true_.
				- _break_
					- The _break_ statement is required to end the case statements.
					- If not present, it will run other case conditions instead of stopping when reaching the first _true_ condition.
				- _default_
					- the _default_ condition is similar to the else statement, it runs if all case conditions are _false_.
		- Example:
			```
			int num = 10;
			switch (num) {
				case num <= 9:
					printf("no");
					break;
				case num >= 11:
					printf("yes");
					break;
				default:
					printf("maybe");
					break;
			}
			```
