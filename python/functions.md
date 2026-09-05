
# Functions

- built-in methods

- universal functions

- print()

- used to print text to the screen

- syntax:

print(<value>)

- multiple values can be printed

- must be seprated by commas (,)

- syntax:

print(<value1>, <value2>, <value3>)

- has an end= parameter

- used to replace the neweline ('\n') after each defauit print() call

- syntax:

print(<value>, end = <value>)

- input()

- used for user input

- syntax:

input(<prompt>)

- the prompt parameter is used to display text when the input function is ran

- example:

input('lumbago? ') #> prints and then asks for user input

- note that the input() function returns a string

- using it in as another data type is done via type casting

- type()

- used to query the data type of a variable

- syntax:

type(<value or variable name>)

- example:

x: int = 10

type(x) #> `<class 'int'>`

- len()

- queries the size of a list

- by extension, strings also

- syntax:

len(<list>)

- example:

a: str = "idkman"

len(a) #> 6

- isinstance()

- determines if the value is the same type as the first parameter

- syntax:

isinstance>(<variable>, <data type>)

- example:

x: float = 3.14

isinstance(x, float) #> True

- range()

- returns a range of integers

- starts at 0

- syntax:

range(<integer>)

- example:

range(6) #> 0, 1, 2, 3, 4, 5

- similar to slicing, there are start, stop and step values

- syntax:

range(<start>, <stop>, <step>)

- example:

range(3, 6, 2) #> 3, 5

- range values are able to be displayed when transform into a list() object

- map()

- applies a function to every iterable

- mostly used in lambda functions

- syntax:

map(<lambda function>, <container>)

- filter()

- creates a list of items when the condition is True

- syntax:

filter(<lambda function>, <container>)

- sorted()

- sorts item alphanumerically

- syntax:

sorted(<values>)

- next()

- manually advances a generator object iterable

- used when dealing with generator functions

- syntax:

<variable> = <generator function>

next(<variable>)

- random()

- requires the random module

- generates random numbers

- example:

#> random number generator with a range

random.randrange(1, 10) #> 1 - 9

#> 1 is inclusice, 10 is exclusive

  

- string methods

- .lower()

- converts the characters inside a string into their lowercase forms

- syntax:

<string>.lower()

- example:

my_string: str = 'IDKMAN'

my_string.lower() #> 'idkman'

- .upper()

- converts the characters inside a string into their uppercase forms

- syntax:

<string>.upper()

- example:

my_string: str = 'idkman'

my_string.lower() #> 'IDKMAN'

- .strip()

- removes the whitespace present before or after the text

- syntax:

<string>,strip()

- example:

my_string: str = " Hello World "

my_string.strip() #> "Hello World"

- .replace()

- replaces a keyword (or a character) in a string

- syntax:

<string>.replace(<string to be replaced>, <replacement string>)

- example:

my_string: str = 'lumbago'

my_string.replace('l', 'd') #> 'dumbago'

- .split()

- splits the string into a list dictated by the split parameter

- typically used to transform list values from comma separators

- syntax:

<string>.split(<string separator>)

- exmaple:

my_string: str = "Hello,World"

my_list: list[str] = my_string.split(',') #> ['Hello', 'World']

- .format()

- presents a way to format strings

- replaced by the f-string in python 3.6

- different syntax to f-strings

- but still uses curly braces { } as placeholder

- syntax:

<string>.format(<placeholder>)

- example:

"yes{}".format("no")

- multiple placeholders are possible

- example:

my_text: str = "my number is {} and adding {} equals {}"

my_text.format(10, 20, 30)

- it is common to use index numbers to mark the number and order of placeholders

- example:

test: str = "one {0}, yes {1}, idkman {2}"

- it is also common to use names as indexes

- example:

test = "{one}, {two}, {three}"

- math methods

- abs()

- returns the absolute value on a number

- i.e. returns it as a positive

- syntax:

abs(<number>)

- example:

abs(-9.23) #> 9.23

- min()

- returns the minimum value of an iterable

- syntax:

min(<iterable>)

- example:

min(1, 78, 10, 29, 199) #> 199

- max()

- returns the maximum value of an iterable

- syntax:

max(<iterable>)

- example:

max(9, 34, 23, 22, 31) #> 34

- pow()

- returns the value an value raised to a power

- syntax:

pow(<num1>, <num2>)

- num1 is the base number and num2 is the exponent

- example:

pow(2, 4) #> 16

- list methods

- adding elements

- .insert()

- inserts values at a specified index

- syntax:

<list_name>.insert(<index>, <value>)

- example:

my_list: list[int] = [1, 2, 3]

my_list.insert(1, 10) #> [1, 10, 2, 3]

- .append()

- adds items at the end of the list

- syntax:

<list_name>.append(<value>)

- example:

my_list: list[int] = [1, 2, 3]

my_list.append(4) #> [1, 2, 3, 4]

- .extend()

- used to extend (or append) elements from another list to the current list

- it is possible to extend from other containers

- like tuples, sets and dictionaries

- syntax:

<list name1>.extend(<list name2>)

- example:

my_list: list[int] = [1, 2, 3]

my_other_list: list[int] = [4, 5, 6]

my_list.extend(my_other_list) #> [1, 2, 3, 4, 5, 6]

- removing elements

- .remove()

- removes the first occurence of a value

- syntax:

<list_name>.remove(value)

- example:

my_list: list[int] = [1, 2, 3]

my_list.remove(1) #> [2, 3]

- .pop()

- removes a value specified by its index value

- similar to the del keyword

- syntax:

<list_name>.pop(<index>)

- example:

my_list: list[int] = [1, 2, 3]

my_list.pop(2) #> [1, 2]

- .clear()

- clears the whole list

- leaves an empty list

- syntax:

<list_name>.clear()

- example:

my_list: list[int] = [1, 2, 3]

my_list.clear() #> []

- organiizng elements

- .sort()

- sorts the list alphanumerically

- sorts uppercase strings first then lowercase

- syntax:

- <list_name>.sort

- example:

my_list: list[int] = [2, 3, 1]

my_list.sort() #> [1, 2, 3]

- can be reversed through the reverse argument

- syntax:

<list_name>.sort(reverse = True)

- example:

my_list: list[int] = [2, 3, 1]

my_list.sort(reverse = True) #> [3, 2, 1]

- .reverse()

- returns a reverse order of elements in a list

- syntax:

<list_name>.reverse()

- example:

my_list: list[int] = [2, 3, 1]

my_list.reverse() #> [1, 3, 2]

- duplicating lists

- .copy()

- copies lists

- instead of sharing the same reference in memory

- .copy() changes that

- syntax:

<list name1> = <list name2>.copy()

- example:

my_list: list[int] = [1, 2, 3]

my_other_list = my_list.copy() #> [1, 2, 3]

- querying values

- .count()

- used to count the number of occuerences of the specified value

- syntax:

<list_name>.count(<value>)

- example:

my_list: list[int] = [1, 2, 3]

my_list.count(1) #> 1

- .index()

- returns the index of specified value in a list

- syntax:

<list_name>.index(<value>)

- example:

my_list: list[int] = [1, 2, 3]

my_list.index(2) #> 1

  

- tuple methods

- querying values

- .count()

- used to count the number of occuerences of the specified value

- syntax:

<tuple_name>.count(<value>)

- example:

my_tuple: tuple[int] = (1, 2, 3)

my_tuple.count(1) #> 1

- .index()

- returns the index of specified value in a list

- syntax:

<list_name>.index(<value>)

- example:

my_tuple: tuple[int] = (1, 2, 3)

my_tuple.index(2) #> 1

  

- set methods

- adding elements

- .add()

- adds elements into a set

- syntax:

<set_name>.add(<value>)

- .update()

- adds items from another set to the current set

- its not restricted to sets only, it is possble to add lists, tuples or dictionaries

- updates the original set

- syntax:

<set_name1>.add(<set_name2>)

- removing elements

- .remove()

- removes an element in a set

- will raise an error if the element to be removed is not present

- syntax:

<set_name>.remove(<value>)

- .discard()

- removes an element in a set

- will not raise an error is the element to be removed is not present

- syntax:

<set_name>.discard(<value>)

- .pop()

- removes an element in a set

- the item remove is random

- syntax:

<set_name>.pop()

- .clear()

- clears the set

- syntax:

<set_name>.clear()

- duplicating lists

- .copy()

- copies sets

- instead of sharing the same reference in memory

- .copy() changes that

- syntax:

<set_name1> = <set_name2>.copy()

- example:

my_set: set[int] = {1, 2, 3}

my_other_set: set[int] = my_set.copy() #> {1, 2, 3}

- joint sets

- .union()

- adds the elements from two sets

- it is possible to unionize a set and a tuple

- alternative to the | set operator

- discards any duplicates

- must be declared as a new set

- syntax:

<new_set_name> = <set_name1>.union(<set_name2>)

- .intersection()

- keeps only the duplicates from two sets

- alternative to the & set operator

- discards non-duplicates

- must be declared as a new set

- syntax:

<new_set_name> = <set_name1>.intersection(<set_name2>)

- .intersection_update()

- keeps only duplicates

- updates the original set

- instead of requiring a new set

- syntax:

<set_name1>.intersection_update(<set_name2>)

- .difference()

- keeps only the unique items from the first set

- discards duplicates and items from the second set

- alternative to the - set operator

- must be declares as a new set

- syntax:

<new_set_name> = <set_name1>.difference(<set_name2>)

- .difference_update()

- keeps unique items fronm the first set

- updates the original set

- instead of requiring a new set

- syntax:

<set_name1>.difference_update(<set_name2>)

- symmetric_difference()

- keeps items present in both sets

- alternative to the ^ set operator

- discards any items that are possible duplicates

- syntax:

<set_name1>.symmetric_difference(<set_name2>)

- .symmetric_difference_update()

- keeps items present in both sets

- updates the original set

- instead of requiring a new set

- syntax:

<set_name1>.symmetric_difference_update(<set_name2>)

  

- dictionary methods

- adding values

- .update()

- updates the value of a key in a dictioanry

- if the key doesn't exist, adds a new entry

- syntax:

<dict_name>.update({<key>:<value>})

- then argument must be a dictionary

- example:

my_dictionary: dict[str, str] = { "idk" : "Hello" }

my_dictionary.update({"idk" : "man"}) #> { "idk" : "man" }

- removing values

- .pop()

- removes items through their key in a dictionary

- syntax:

<dict_name>.pop(<key>)

- example:

my_dictionary: dict[str, str] = { "idk" : "man" }

my_dictionary.pop("idk") #> {}

- .popitem()

- removes the last item added in a dictionary

- syntax:

<dict_name>.popitem()

- sidenote:

- Python version before 3.7, .popitem() removes random items

- .clear()

- clears the items inside a dictionary

- syntax:

<dict_name>.clear()

- duplicating dictionaries

- .copy()

- copies dictionaries

- instead of sharing the same reference in memory

- .copy() changes that

- syntax:

<dict name1> = <dict name2>.copy()

- example:

my_dictionary: dict[str, str] = { "idk" : "man" }

my_other_dictionary = my_dictionary.copy() #> { "idk" : "man" }

- querying values

- .get()

- returns a the value a key holds inside a dictionary

- syntax:

<dict_name>.get(<key>)

- example:

my_dictionary: dict[str, str] = { "idk" : "man" }

my_dictionary.get("idk") #> "man"

- .keys()

- returns all keys inside a dictionary

- returns a list

- any changes in the dictionary are reflected on the list

- syntax:

<dict_name>.keys()

- example:

my_dictionary: dict[str, str] = { "idk : "man" }

my_dictionary.keys() #> ["idk"]

- .values()

- returns all values inside a dictionary

- returns a list

- any changes in the dictionary are reflected on the list

- syntax:

<dict_name>.values()

- example:

my_dictionary: dict[str, str] = { "idk" : "man" }

my_dictionary.values() #> ["man"]

- .items()

- returns all items inside a dictionary

- returns tuples in a list

- any changes in the dictionary are reflected on the list

- syntax:

<dict_name>.items()

- example:

my_dictionary: dict[str, str] = { "idk" : "man" }

my_dictionary.items() #> [("idk", "man")]

  

- generator methods

- .send()

- allows sending values to a generator

- must first prime the generator using next()

- syntax:

#> assuming <generator name> is a generator object

<generator name>.send(<values>)

- example:

def my_generator() -> str:

while True:

my_value = yield

print(my_value)

my_generator = my_generator()

next(my_generator) #> priming the generator object

my_generator.send("hello") #> "hello"

my_generator.send("idkman") #> "idkman"

- .close()

- closes the generator object or function

- syntax:

<generator name>.close()

- example:

def my_generator() -> str:

try:

yield 'yes'

finally:

print('no') #> runs when the try block finishes

  

my_var = my_generator()

my_var.close #> runs the finally statement

  

- user-defined functions

- enables the creation of user-defined functions or methods

- these are defined by the programmer

- rules when naming functions

- can contain letters, numbers and underscores _

- must start with a letter or an underscore

- names are case-sensitive

- my_function and my_Function are not the same

- functions are used for code repeatability

- functions are resuable

- removes the hassle of typing the same code over and over again

- the name must match the purpose of the function

  

- declaration and definition

- custom methods can either have a return statement or not

- without return statament

- syntax:

def <function_name>() -> <return_type>:

<statament>

- example:

def my_function() -> None:

print("idkman")

- with return statement

syntax:

def <function_name>() -> <return_type>:

<statament>

return <value>

- example:

def my_function() -> int:

x = 10

return x

- sidenote:

- the return value can be any value

- it can be a collection, a variable, etc.

- any code declared after the return statement is considered as useless

- after the custom method runs the return statament, it jumps back to the main program

- ignoring the code after it

  

- functions with paramethers

- methods and functions that require an input of data

- when declaring a function that requires an input, it is called as a parameter

- multiple inputs are called parameters

- syntax:

def <function_name>(<parameter>) -> <return_type>:

<stataments>

- example:

def yes(idk) -> None:

print(idk)

- note that parameters are strictly temporary

- it disappears after the function ends

- functions that requires multiple inputs can also have multiple parameters

- example:

def sum_of_num(x, y, z) -> int:

retrun x + y + z

  

- access and function cals

- functions are accessed using the method name followed by parentheses ()

- syntax:

<function_name>()

- example:

my_function()

  

- functions calls with arguments

- if a function requires certain parameters, that is called an "argument"

- or arguments if there are multiple parameters

- calling functions with parameters requires the corresponding arguments

- variables and values are able to be passed as arguments

- syntax:

<function_name>(<arguments>)

- example:

my_function("yes")

- when there are multiple arguments needed

- the order of the parameters matter

- if the order of arguments doesn't match the order of parameters, an error occues

- example:

my_function(a, b, c)

- arguments can be in the form of keyword arguments (or kwargs)

- example:

my_function(a = 1, b = 2, c = 3)

  

- function or method overloading

- multiple functions or methods can have the same name

- if they have different parameters

- is a form of polymorphism

- syntax:

def <function_name>(<parameters1>) -> <return_type>:

<stataments>

def <function_name>(<parameters2>) -> <return_type>:

<stataments>

- example:

def print_stuff(yes: int) -> None:

print(yes)

def print_stuff(no: str) -> None:

print(no)

  

- *args and **kwargs

- allows a function to accept multiple arguments as input

- arbitraty arguments (*args):

- allows multiple arguments and stores it in a tuple

- syntax:

def <function_name>(*<args>) -> <return_type>: #> note that *args can be any name

#> the single star * is what defines the *args

<stataments>

- example:

def idkman(*lumbago: int) -> None:

for i in lumbago:

print(i)

- positional arguments are able to be combined with arbitrary arguments

- note that positional arguments must be declared first

- syntax:

def <function_name>(<parameters>, *<args>) -> <return_type>:

<statements>

- example:

def my_function(my_string: str, *my_num: int) -> None:

for i in my_num:

for n in range(i):

print(my_string)

- note that the positional arguments must be satisfied when calling the function

- arbitrary keyword arguments (**kwargs):

- allows passing of multiple keyword arguments

i.e. variables that are defined while calling the function

- stores the received values in a dictionary

- syntax:

def <function_name>(**<kwargs>) #> note that **kwargs can be any name

#> the double star ** is what defines the **kwargs

- example:

def my_function(**idkman):

print(idkman.values())

- positional arguments are able to be combined with keyword arguments

- note that positional arguments must be declared first

- syntax:

def <function_name>(<parameters>, **<kwargs>) -> <return_type>:

<stataments>

- example:

def my_function(yes: str, **maybe) -> str:

print(str)

return maybe

- *args and **kwargs are able to be declared simultaneously

- *args must come before **kwargs

- syntax:

def <function_name>(*<args>, **<kwargs>) -> <return_type>:

<statament>

- example:

def idkman(*yes, *no*) -> None:

pass

- it is possible to unpack lists and tuples, or dictionaries when calling *args and **kwargs functions or methods

- *args

- example:

def idkman(a, b, c) -> None:

print(b)

my_list: list = [2, 3, 4]

idkman(*my_list)

- note that a star * must be present

- **kwargs

- example:

def lumbago(a, b) -> None:

print(a)

print(b)

my_dict = { "a" : "idk", "b": "man" }

lumbago(**mydict)

- note that double stars ** must be present

- combining positional arguments, *args, and **kwargs

- note that positional arguments must come first, then *args, and then **kwargs

- syntax:

def <function_name>(<parameters>, *<args>, **<kwargs>) -> <return_type>:

<stataments>

- example:

def my_function(yes, *no, **maybe) -> None:

pass

  

- decorator functions

- adds more functionality to a function or a method

- does this without alreting the code of the original function or method

- takes a function as an input and returns a new function

- returns an altered form of the orginal function

- are able to be called multiple times

  

- declaration and definition

- without parameters

- syntax:

def <decorator_name>(func):

def <function_name>(): #> can be any other name

<statements>

return <expression>

return <function_name>

- example:

def change_to_uppercase(func):

def to_upper():

return func().upper()

retrun to_upper

- with parameters

- it is possible to modify or "decorate" function parameters

- syntax:

def <decorator_name>(func):

def <function_name>(<parameters>):

<statements>

return <expression>

return <function_name>

- exapmple:

def my_decorator(func):

def my_function(*args, **kwargs):

retrun my_function(*args, **kwargs).lower()

return my_function

- sidenote:

- decorators have no control over *args and **kwargs arguments

- to solve this, add *args and **kwargs to the decorator function

- with parameters

- decorators can accept their own arguments

- done by adding another wrapper level

- syntax:

def <decorator_name>(<parameters>):

def <decorator_name>(func):

def <function_name>():

<statements>

return <expression>

return <function_name>

return <decorator_name>

  

- access and calls

- uses the at @ symbol to call the function

- without arguments

- syntax:

@<decorator_name>

- example:

@change_to_upper

def my_function():

print("change this to upper")

- sample decorator:

def to_lower(func):

def function_stuff(*idk, **man):

return function_stuf(*idk, **man).lower()

return function_stuff

@to_lower

def print_stuff(stuff):

print(stuff)

  

print_stuff("IDKMAN")

- with arguments

- syntax:

@<decorator_name>(<arguments>)

- multiple decorators

- it is possible to call more than one decorator to work on a single function

- example:

#my_decorator1

@my_decorator2

def my_function():

pass

  

- preserving metadata

- when a function is decorated, metadata is lost

- example:

def my_decorator(func):

def my_method():

return func()

return my_method

@my_decorator

def my_function():

print('yes')

  

print(my_function().__name__) #> my_method

#> instead of my_function

- to circumvent this, it is done by importing the functools modules

- and using the functools.wraps(func) decorator

- example:

import functools as ft

def my_decorator(func):

@ft.wraps(func):

def my_method():

return func()

return my_method

  

@my_decorator

def my_function():

pass

  

print(my_function().__name__) #> my_function

  

- lambda functions

- a small anonymous function

- it can take any number of arguments but can only have one expression

- syntax:

lambda <arguments>: <expression>

- example:

lambda x : x + 10

- used in variables for quick initialization

example:

my_var = lambda yes : yes * 10

my_var(10) #> 100

- commonly used with these functions

- with map() function

- example:

- map(lambda x : x * 2, [1, 2, 3]) #> returns a list object

#> [2, 4, 6]

- with filter() function

- example:

- filter(lambda x : x % 3 != 0, [1, 2, 3]) #> returns a list object

#> [1, 2]

- with sorted() function

- example

- sorted([3, 1, 2, 5, 4], key = lambda x : x[1])

- sorted(['apple', 'banana', 'cherry'], key = lambda x : len(x))

  

- recursive functions

- also called "recursions"

- it occurs when a function calls itself

- can be very dangerous when there are no end conditions

- can lead to memory hg or performance loss

- due to it never ending, eating up resources

- by default, Python has a default of 1000 recursive calls

- this is queried through the sys module

- example:

import sys

sys.getrecursionlimit() #> returns recursion limit

sys.setrecursionlimit(200) #> sets recursion limit to 2000

- it is recommended to use iteration when handling very deep recursions

- syntax:

def <function name>(<parameters>) -> <return_type>:

<base cases> #> to prevent endless recursions

return <function name>(arguments) <expression>

#> or

<function name>(<arguments>)

- example:

#> fibonacci sequence

def factorial(n: int) -> int:

if n == 1 or n == 0:

return 1

return n * factorial(n - 1)

#> sum of list

def sum_list(numbers) -> int:

if len(numbers) == 0:

return 0

else:

return numbers[0] + sum_list(numbers[1:])

#> max number in list

def find_max(numbers) -> int:

if len(numbers) == 1:

return numbers[0]

else:

max_of_rest = find_max(numbers[1:])

return numbers[0] if numbers[0] > max_of_rest else max_of_rest

- two parts of a recursive function:

- base case:

- conditions that terminate the recursion

- recursive case:

- the function calling upon itself with modified arguments

- can be a return statement or a function call

  

- generator functions

- a form of function that can pause and resume their execution

- when called, it returns a generator object which is a iterable

- uses the yield keyword

- generators are able to save memory

- due to it generating values on the fly

- unlike normal functions that saves the entire range of values all at once

- syntax:

def <generator_name>():

<statements>

yield <expression>

- example:

def my_generator():

yield 5

- generators are able to be advanced using the next() function

- syntax:

next(<generator_variable>)

- example:

- def generator():

yield 1

yield 2

my_generator = generator()

next(my_generator) #> 1

next(my_generator) #> 2

- note that when there are no longer any values to yield

- the next manual advance will result in a StopIteration

- example:

def my_generator():

yield 1 #> gives only one value

  

my_var = my_generator()

next(my_var)

next(my_var) #> StopIteration

- generator expressions

- similar to list comprehension

- it is possible to create generators with parentheses ( )

- instead of square brackets

- syntax:

<variable_name> = (<expression>)

- example:

my_var = (x * x for x in range(5))

- generator control

- generators has methods for controlling generator functions

- refer to generator methods