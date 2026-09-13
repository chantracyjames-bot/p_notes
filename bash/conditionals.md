
# Conditionals
- Definition:
	- Used for program flow.
- _if-elif-else_
	- Note:
		- To end and if-elif-else statement, the _fi_ keyword is required as it marks an end to the conditional statements.
	- _if_
		- Definition:
			- Runs a block of code if the condition is true.
		- Syntax:
			```
			if [[<condition>]]; then
			<code_block>
			fi
			#> or
			if [<condition>]; then
			<code_block>
			fi
			```
		- Example:
			```
			if [[ 10 -gt 9]]; then
			echo "idkman"
			fi
			```
	- _elif_
		- Definition:
			- Runs a block of code if the condition is true, only running after an _if_ block returns false.
		- Syntax:
			```
			elif [[<condition>]]; then
			<code_block>
			fi
			#> or
			elif [<condition>]; then
			<code_block>
			fi
			```
		- Example:
			```
			elif [[ 11 -lt 90]]; then
			echo "lumbago"
			fi
			```
	- _else_
		- Definition:
			- Runs if all conditions from the _if_ and _elif_ statements return false.
		- Syntax:
			```
			else
			<code_block>
			fi
			```
		- Example:
			```
			else
			echo "idk"
			fi
			```
	- Sample code:
		```
		if [[ "$my_name" == "tarcy"]]; then
		echo "hi"
		elif [[ "$my_name" == "tracy" ]]; then
		echo "hello"
		else
		echo "idkman"
		fi
		```
- _case_
	- Definition:
		- An altenative to if-elif-else statements.
	- Syntax:
		```
		case <expression> in
			<condition>)
				<code_block>
				;;
			<condition>)
				<code_block>
				;;
			*)
				<code_block>
				;;
		```
	- Note:
		- The asterisk _*_ is a wildcard, usually used for the remaining values similar to default statements in other languages.
		- The double semicolon _;;_ is required for each case, as it marks the case as terminated.
	- Sample code:
		```
		case "$my_name" in
			"tarcy")
				echo "hi"
				;;
			"tracy")
				echo "hello"
				;;
			*)
				echo "idkman"
				;;
		```