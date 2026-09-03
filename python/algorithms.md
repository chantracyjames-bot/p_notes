
# Algorithms
- Definition:
	- Are a way of working with data and solving problems.
	- Problems like sorting, searching, or iterating are able to be solved through algorithms.
- Note:
	- Algorithms are designed to be fast and efficient.
	- At a large enough data size, algorithms will inevitably become slow.
	- That is why time complexity is very important in data structures, and especially in algorithms.
- Example:
	```
	my_list: list[int] = [2, 1, 5, 3, 4, 8, 0]
	min_val: int = my_list[0]
	for i in my_list:
		min_val = i if min_val > i else min_val
		#> loops though the list finding the minimum value
	```
- Time complexity:
	- Definition:
		- The time for an algorithm to do its job is called "runtime".
		- It is one of the fundamental concepts of algorithms, as it dictates the time and efficiency of it.
	- Runtime
		- Definition:
			- Knowing the runtime of an algorithm will show it efficiency.
			- Inefficient algorithms can make programs slow or even unworkable.
			- By understanding the runtime of an algorithm, the right algorithm can be made for the problem to solve and in return, making the program faster and enables the algorithm to deal with even larger states of data.
		- Actual runtime
			- Definition:
				- When looking at the runtime of a given algorithm, the actual time is not considered.
				- This is due to varying factors that an algorithm have to account for.
			- Factors:
				1. The programming language
					- The language that is used to implement the algorithm.
				2. How it is written
					- How the programmer writes and design the algorithm.
				3. The compiler or interpreter
					- How the compiler or interpreter interprets the code or how it translate it to machine code.
				4. The current hardware
					- The hardware that the algorithm is current running on as differing hardware can influence the efficiency of an algorithm.
				5. The operating system
					- The current operating system and the other ongoing background tasks as different tasks in the background can limit resources.
				6. The amount of data
					- Larger amounts of data can increase the time that an algorithm takes, as smaller amounts of data can do the opposite.
					- Instead of looking at the actual runtime of the algorithm, it is better to look at the time complexity of it as it is more abstract than actual runtime and does not consider the hardware and the language.
	- Operation:
		- Background:
			- Time complexity is the number of operations needed to run an algorithm, most specially when dealing with large amount of data.
			- This is were the number of operations is considered as "time", as the computer takes time in-between operations.
			- For instance, an algorithm that find the minimum value of an array.
				- The algorithm must go through every single value in that array since it has to be compared to the current minimum value.
				- Each comparison is considered as an operation and each of those said comparisons must a certain amount of time.
				- So the total time that the algorithm takes to find the lowest value depends on the number of items or values in that array.
				- As a result, if the array has a total of 100 items, then it will take 100 operations to do so.
				- The relationship for this instance of an algorithm is linear as each value adds on to the number of operations, also known as a linear algorithm.
		- Definition:
			- The term operation can become very misleading as some operations takes one or more CPU cycles.
			- "One operation in an algorithm can be understood as something we do in each iteration of the algorithm, or for each piece of data, that takes constant time".
			- For instance, comparing two elements and them swapping the bigger one.
				- It is considered as one operation, an example being the Bubble Sort algorithm.
				- Understanding it as one or more operations doesn't really matter as the algorithm takes a constant amount of time in-between.
			- If an operation takes the same amount of time when processing any amount of data it can be considered as taking a "constant" amount of time.
			- As comparing two elements and then swapping the bigger one, even if there are 10 or 1000 elements present, it will still take a constant amount of time to finish.
	- Big O Notation:
		- Definition:
			- Comes from a mathematical concept.
			- This notation describes the upper bound of a function
			- In computer science:
				- This notation more or so represents the worse case time complexity or the worse case scenario for the amount of time an algorithm takes.
				- This notation is usually represented by the capital letter O with parentheses and inside those parentheses, is an expression that indicates the runtime of an algorithm.
				- Runtime is represented with the letter _n_, which is the number of values in the data set being worked on by the algorithm
			- Examples of O():
				- O(1)
					- Definition:
						- The fastest algorithm with the smallest time complexity.
						- It usually is done by looking at a certain index on an array.
					- Example:
						```
						my_array[24] #> O(1)
						```
					- Note:
						- Since looking up the value with using an index takes only one operation, it is considered as an O(1).
						- Do note that not all algorithms can be made to be like this, it only serves as an example as to how important time complexity is.
				- O(n)
					- Definition:
						- One of the most ideal time complexities.
						- It is usually done by finding a value by comparing all elements inside a data set, like finding the minimum or maximum value of an array.
						- This algorithm is linear, as the amount of time it takes is proportional to how many elements are present.
				- (On^2)
					- Definition:
						- One of the slowest algorithms.
						- It is usually is done by going through the data set twice, like sorting using Bubble or Insertion sort.
						- This algorithm scales with how large the data set is, as large data sets can slow down this algorithm dramatically.
				- O(n log n)
					- Definition:
						- Faster than O(n^2).
						- It is usually is implemented in the Quicksort algorithm, being faster on average than Bubble or Insertion sort but it still has the O(n^2) worse case scenario.
						- This algorithm doesn't scale as dramatically, it is one of the faster algorithms.
		- Worst case scenario
			- Definition:
				- If an algotihm has to go through n values requiring _n_ operations to do so, it will always have the same best, average and worst case scenarios.
				- Though with some algorithms, even if _n_ values stay the same, the amount of requirements is not the same, depending on how it is implemented.
				- like in sorting algorithms, some can take a short amount of time (best case), while some take a really long time (worst case).
				- These are all dependent on the data set they are given and more importantly, how these algorithms are designed.