
# Classes
- Object-Oriented Programming
	- Definition:
		- Focuses on dealing with objects that holds both data and functions to work on the same data.
		- Everything is required to be associated with classes and objects.
	- Main points of OOP:
		- Clearer structure to programming.
		- Focuses on the DRY principle.
			- Don't Repeat Yourself
				- Implies that duplicate code must be reused.
				- Helps in maintaining, reusing and debugging pieces of code.
	- OOP focuses on objects and classes:
		- Classes
			- A user-defined type, which works as an object constructor.
			- Serves as a blueprint for creating objects, as it defines what an object should look like.
		- Object
			- Created based on the class, uses the "blueprints" provided by the class.
		- Inherits the attributes and methods of the class it is based on, and it becomes an instance of the class.
- Python classes
	- Declaration and Definition:
		- Definition:
			- To create a user-defined class, the _class_ keyword is used.
		- Syntax:
			```
			class <class_name>:
				<statements>
			```
		- Example:
			```
			class MyCLass:
				idkman = 'lumbago'
			```
	- _\_\_init\_\_()_
		- Definition:
			- Also known as a class constructor, a built-in method in Python.
			- It is method that gets called when the class is being initiated, or when object instance of a class is being created.
			- It is used to initialize object properties or perform operations that are when the an object of a class is created.
		- Declaration and definition:
			- Definition:
				- When declaring a class constructor, it must use the _\_\_init\_\_()_ method name.
			- Syntax:
				```
				class <class_name>:
					def __init__() -> <return_type>:
						<statements>
				```
			- Example:
				```
				class MyClass:
					def __init__() -> None:
						print('lumbago')
				```
		- Parameters and arguments
			- Definition:
				- Like normal methods, it is possible to assign parameters to a constructor.
			- Syntax:
			```
				class <class_name>:
					def __init__(<parameters>) -> <return_type>:
						<statements>
			```
			- Example:
				```
				class Idkman:
				def __init__(self, lumbago) -> None:
					self.lumbago = lumbago
				```
		- _self_
			- Definition:
				- A special keyword that is a reference to the current instance of the class or object of the class.
				- Used to access attributes and methods that belongs to that particular object instance.
				- Without it, Python won't know what attribute is being accessed.
				- The self parameter is the most important parameter in a class, as it is used to initialize variables during the object creation.
			- Note:
				- _self_ must be the first parameter when declared.
				- It can be named as anything, but self is the preferred name by convention.
				- It is possible to call attributes and methods using the self parameter
					- Example:
						```
						#> with __init__() and self
						class TestClass:
							def __init__(self, idkman) -> None:
								self.idkman = idkman            #> creates and object and initializes the idkman variable
						
						my_obj = TestClass("lumbago")          #> auto initializes idkman with "lumbago"
						
						#> without __init__() and self
						class TestClass:
							pass
						
						my_obj = TestClass()
						my_obj.idkman = "lumbago"              #> have create the object attribute manually
						```
		- Default variables as parameters
			- Definition:
				- Similar to normal methods, it is possible to assign values to parameters.
				- Objects are able to be created without assigning the assigned attribute, using the default value instead.
				- Assigning it through arguments will override the default value.
			- Syntax:
				```
				class <class_name>:
					def __init__(self, <variable> = <value>) -> <return_type>:
						self.<variable> = <variable>
				```
			- Example:
				```
				class HelloWorld:
					def __init__(self, hello, world = 'idkman') -> None:
						self.hello = hello
						self.world = world
				
				
				my_obj = HelloWorld('yes', 'maybe') #> overriding the default value
				my_other_obj = HelloWorld('no')     #> using the default value
				```
	- class properties
		- Definition:
			- Similar to attributes in Java, refers to the variables that a class possesses.
			- A variable in a class becomes a property or an attribute of the class.
		- Accessing properties:
			- Definition:
				- In Python, there are to types of properties.
			- Class properties:
				- Definition:
					- Similar to static class attributes in Java, where every single instance object share the same class attribute.
				- Example:
					```
					class YesNo:
						idkman = 'lumbago' #> class property
					
					hello = YesNo()
					world = YesNo()
					hello.idkman           #> 'idkman'
					world.idkman           #> 'idkman'
					#> shares the same property
					```
				- Note:
					- Modifying value will be shared by all object instance, only if the class is being modified.
						- Example:
							```
							YesNo.idkman = 'maybe'
							world.idkman           #> maybe
							hello.idkman           #> maybe
							```
					- Modifying the value using an object will make that class property be an object property, it becomes part of the object rather than the class.
						- The value of that property will be unique to that object.
						- Example:
							```
							world.idkman = 'yes'
							hello.idkman         #> 'lumbago'
												 #> retains the class property value 
							```
					- Deleting the value will delete the class property, and trying to access it after being deleted will cause an error.
						- Example:
							```
							del hello.idkman
							world.idkman     #> causes an error
							```
			- Object properties
				- Definition:
					- Similar to non-static attributes in Java, where every single instance object have unique object properties.
				- Example:
					```
					class Lumbago:
						def __init__(self, idkman) -> None:
							self.idkman = idkman    #> creates a 'unique' property for the object
					
					
					hello = Lumbago('Hello')
					world = Lumbago('World')
					hello.idkman                    #> 'hello'
					world.idkman                    #> 'world'
					#> doesn't share the same property
					```
					- modifying the value retains the uniqueness of other object instances
					- Example:
					```
					hello.idkman = 'yes'
					world.idkman         #> 'world'
					#> still holds the same value
					```
				- Note:
					- Unlike class properties, deleting the value won't cause an error.
						- Example:
							```
							del world.idkman
							hello.idkman     #> 'yes'
							```
					- Unlike class properties, it is possible to add new object properties.
						- It is unique to the object instance, it cannot be accessed by other objects.
						- Example:
							```
							world.new_var = yes
							hello.new_var       #> causes an error
							```
	- Class methods
		- Definition:
			- Similar to normal functions, refer to methods.md for normal method declaration
		- Declaration and definition:
			- Definition:
				- Like normal Python methods, there are two types.
			- Static methods
				- Definition:
					- Methods that belong to a class, and non-unique to any object.
					- requires the _@staticmethod_ decorator
				- Syntax:
					```
					class <class_name>:
						@staticmethod
						def <method_name>() -> <return_type>:
							<statements>
					```
				- Example:
					```
					class Lumbago:
						@staticmethod
						def idkman() -> None:
							print('worldhello')
					```
			- Non-static methods
				- Definition:
					- Methods that belong to a class, defining the behavior of objects created from the same class.
				- Syntax:
					```
					class <class_name>:
						def <method_name>() -> <return_type>:
							<statements>
					```
				- Example:
					```
					class MyClass:
						def my_method() -> None:
							print('idkman')
					```
		- Parameters
			- Definition:
				- Class methods can contain parameters.
			- Static methods
				- Syntax:
					```
					class <class_name>:
						@staticmethod
						def <method_name>() -> <return_type>:
							<statements>
					```
				- Example:
					```
					class Yes:
						@staticmethod
						def no() -> None:
							print('maybe')
					```
			- Non-static methods
				- Syntax:
					```
					class <class_name>:
						def <method_name>(self, <parameters>) -> <return_type>:
							<statements>
					```
				- Example:
					```
					class MyClass:
						def my_method(self, idkman) -> None:
							print('lumbago')
					```
				- Note:
					- All methods must contain _self_ as the first parameter.
						- Using _self_ will enable the method to access any properties of the current object instance.
						- Methods are able to directly modify the properties provided by _self_.
						- Example:
							```
							class MyClass:
								def __init__(self, yes) -> None:
									self.yes = yes
								def my_method(self) -> None:
									yes = 'idkman'
							```
					- Classes can contain multiple methods.
						- Example:
							```
							class MyClass:
								def idkman() -> None:
									pass
								def maybe() -> None:
									pass
								def lumbago() -> None:
									pass
							```
		- _\_\_str\_\_()_
			- Definition:
				- Similar to _\_\_init\_\_()_, that being a another dunder method, it is commonly used to modify the string value when trying to print a property of an object.
			- Syntax:
				```
				class <class_name>:
					def __str__(self, <parameters>) -> str:
						<statements>
						return <expression>
				```
		- Access and calls:
			- Definition:
				- To access methods, there are two ways.
			- Static methods
				- Definition:
					- Static methods are able to be accessed directly, without using an object.
				- Syntax:
					```
					<class_name>.<method_name>()
					```
				- Example:
					```
					MyClass.my_method()
					```
			- Non-static methods
				- Definition:
					- Non-static methods requires an object to be able to access its methods.
				- Syntax:
					```
					<object_name>.<method_name>()
					```
				- Example:
					```
					my_obj = MyClass()
					my_obj.my_method()
					```
			- Note:
				- Methods are able to be deleted using the _del_ keyword.
					- Syntax:
						```
						#> static methods
						del <class_name>.<method_name>
						#> non-static methods
						del <object_name>.<method_name>
						```

	- Nested classes
		- Definition:
			- Classes can exist inside other classes.
			- The main purpose of nested classes is to group classes that belong together.
		- Declaration and definition
			- Definition:
				- Similar to declaring normal classes but is done inside of another class.
			- Syntax:
				```
				class <outer_class_name>:
					class <inner_class_name>:
						<statements>
				```
			- Example:
				```
				class OuterClass:
					class InnerClass
						pass
				```

		- Accessing inner classes
			- Definition:
				- To access an inner class, an object of the outer class must first be created.
			- Syntax:
				```
				<object_name1> = <class_name>(<arguments>)
				<object_name2> = <object_name1>.<inner_class_name>(<arguments>)
				```
			- Example:
				```
				my_outer = OuterClass()
				my_inner = my_outer.InnerClass()
				```
		- Note:
			- Inner classes are able to access the properties and methods from the outer classes.
			- By default, inner classes don't have access to the properties and methods of the outer class.
				- However, it is possible to access it by creating an object of the outer class inside the inner class.
			- There are two ways:
				- Static elements
					- Example:
						```
						class Yes:
							my_var = 'yes'
							class No:
								Yes.my_var
						```
				- Non-static elements
					- Definition:
						- Works by passing self into the inner class.
					- Example:
						```
						class Outer:
							def __init__(self, yes) -> None:
								self.yes = yes
								self.inner = self.Inner(self)
							class Inner:
								def __init__(self, outer_self) -> None:
									self.outer = outer_self
						```
	- Python objects
		- Definition:
			- Objects are an instance of a class.
		- Declaration and initialization
			- Definition:
				- To create an object, it must become an instance of a class.
			- Syntax:
				```
				<object_name> = <class_name>()
				```
			- Example:
				```
				my_obj = MyClass()
				```
		- Note:
			- It is possible to declare more than one instance of a class
				- Example:
					```
					idk = MyClass()
					man = MyClass()
					```
		- Access and deletion
			- Definition:
				- To remove or delete a class, the _del_ keyword is used.
			- Syntax:
				```
				del <object_name>
				```
			- Example:
				```
				del my_obj
				```
	- Inheritance
		- Definition:
			- Allows child classes to reuse properties from the parent class.
			- Prevents the duplication of the same methods and allows reusing without redeclaring the same methods.
			- Inheritance is grouped into two categories:
				- Parent class
					- Also known as the superclass or the base class.
					- It it where the child class inherits from.
				- Child class
					- Also knows as the subclass or the derived class.
					- It is what inherits from the parent class.
		- Declaration and definition
			- Definition:
				- In Python, inheritance is done by enclosing the parent class in parentheses, right next to the name of the child class/
				- Syntax:
					```
					class <child_class_name>(<parent_class_name>):
						<statements>
					```
				- Example:
					```
					class ChildClass(ParentClass):
						pass
					```
		- Note:
			- By default, when the _\_\_init\_\_()_ method is not declared in the child class, it uses the _\_\_init\_\_()_ method of the parent class.
				- This is due to it inheriting every method including the constructor method, declaring another _\_\_init\_\_()_ method overrides parent class' _\_\_init\_\_()_ method.
				- Syntax:
					```
					class <child_class_name>(<parent_class_name>):
						def __init__(self, <parameters>) -> <return_type>:
							<statements>
					```
			- Adding the parent's _\_\_init\_\_()_ method will complete the inheritance and without it, it loses access to the properties of the parent class.
				- Syntax:
					```
					class <child_class_name>(<parent_class_name>):
						def __init__(self, <parameters>) -> <return_type>:
							<parent_class_name>.__init__(self, <parameters>)
					```
				- Example:
					```
					class ChildClass(ParentClass):
						def __init__(self, yes, no) -> None:
							ParentClass.__init__(self, yes, no)
					```
		- _super()_
			- Definition:
				- Lets the child inherit all properties and methods from its parent class, replacing the parent's _\_\__init\_\_()_ method of inheriting.
			- Syntax:
				```
				class <child_class_name>(<parent_class_name>):
					def __init__(self, <parameters>) -> <return_type>:
						super().__init__(<parameters>)
				```
			- Example:
				```
				class ChildClass(ParentClass):
					def __init__(self, yes) -> None:
						super().__init__(yes)
				```
			- Note:
				- Child classes can declare their own properties and methods, the parent class won't have access to new properties or methods declared by the child class.
					- Example:
						```
						class MyClass(ParentClass):
							def __init__(self, no, idkman) -> None:
								super().__init__(no):
								#> new property
								self.idkman = idkman
							#> new method
							def my_method(self) -> None:
								print('probs')
						```
	- Polymorphism
		- Definition:
			- It means "many forms".
			- Occurs when multiple classes that are related through inheritance, multiple functions or methods having the same name but perform different tasks.
			- Overloading is a form of polymorphism.
		- Syntax:
			```
			class <superclass_name>:
				def <method_name>(<parameters>) -> <return_type>:
					<statements>
			class <subclass_name1>:
				def <method_name>(<parameters>) -> <return_type>:
					<statements>
			class <subclass_name2>:
				def <method_name>(<parameters>) -> <return_type>:
					<statements>
			class <subclass_name3>:
				def <method_name>(<parameters>) -> <return_type>:
					<statements>
			```
		- Example:
			```
			class MyClass:
				def my_method(self) -> None:
					print('idkman')
			class Yes(MyClass):
				def my_method(self) -> None:
					print('lumbago')
			class No(MyClass):
				def my_method(self) -> None:
					print('hello')
			class Maybe(MyClass):
				def my_method(self) -> None:
					print('world')
			
			#> all classses possesses the same methods but have different purposes
			```
		- Note:
			- Child classes are considered as polymorphism, as they inherit the methods and properties of their parent class.
				- Child classes can use the same methods as the parent class, and they can also override the parent's methods.
	- Encapsulation
		- Definition:
			- Ensures that sensitive data are hidden from users, any important value are hidden to prevent data leaks.
			- Encapsulation is achieved through access modifiers, to access and retrieve private data certain methods are created and used, these are getter and setter methods.
			- Why Encapsulation?
				- It provides better control of classes, methods, and properties:
					- Read-only for getter methods.
					- Write-only for setter methods.
				- Increases security and flexibility.
					- Parts of code can be changed without compromising others
				- Better data protection and validation.
					- It prevents accidental modification of private data and better validation.
		- Access modifiers
			- public / default
				- Definition:
					- Properties and methods are able to be accessed outside the class, either directly or through objects.
					- It no special declaration, properties are public by default.
				- Syntax:
					```
					class <class_name>:
						#> static properties
						<variable_name1>
						#> non-static method
						def <method_name1>(<parameters>) -> <return_type>:
							#> non-static properties
							self.<variable_name2>
						#> static method
						@staticmethod
						def <method_name2>(<variables>) -> <return_type>:
							<statements>
					```
				- Example:
					```
					class MyClass:
						#> static properties
						maybe = 'yes'
						#> static method
						@staticmethod
						def static_method(self) -> None:
							pass
						#> non-static method
						def idkman(self) -> None:
							#> non-static properties
							self.probs = 'no'
					
					#> accessing public properties and methods
					#> static elements
					MyClass.static_method()
					MyClass.maybe
					#> non-static methods
					lumbago = MyClass()
					lumbago.idkman()
					lumbago.probs
					```
			- protected
				- Definition:
					- Python does not have a "protected" Syntax like Java and C++ but by convention, having a single underscore _ before the name denotes a variable is protected.
						- It means that the properties and methods must stay inside the class, while controlling how data can be accessed from the outside but elements are still accessible outside.
				- Syntax:
					```
					class <class_name>:
						#> static properties
						_<variable_name1>
						#> non-static method
						def _<method_name1>(<parameters>) -> <return_type>:
							#> non-static properties
							self._<variable_name2>
						#> static method
						@staticmethod
						def _<method_name2>(<variables>) -> <return_type>:
							<statements>
					```
				- Example:
					```
					class MyClass:
						#> static properties
						_maybe = 'yes'
						#> static method
						@staticmethod
						def _static_method(self) -> None:
							pass
						#> non-static method
						def _idkman(self) -> None:
							#> non-static properties
							self._probs = 'no'
					
					#> accessing public properties and methods
					#> static elements
					MyClass.static_method()
					MyClass.maybe
					#> non-static methods
					lumbago = MyClass()
					lumbago.idkman()
					lumbago.probs
					```
			- private
				- Definition:
					- Elements are completely inaccessible from outside the class, only through getter and setter methods.
					- Declared using two underscores before the name, triggering name mangling.
				- Name mangling
					- Definition:
						- Declaring an element name with a double underscore __ prefix before the name itself triggers name mangling, renaming the element by adding a \_<class_name> prefix before the name.
							- Example:
								```
								class Yes:
									__my_var
								
								#> becomes
								_Yes__my_var
								```
						- Private methods and attributes are technically accessible via the "mangled" name but is unadvised.
					- Syntax:
						```
						class <class_name>:
							#> static properties
							__<variable_name1>
							#> non-static method
							def __<method_name1>(<parameters>) -> <return_type>:
								#> non-static properties
								self.__<variable_name2>
							#> static method
							@staticmethod
							def __<method_name2>(<variables>) -> <return_type>:
								<statements>
						```
					- Example:
						```
						class MyClass:
							#> static properties
							__maybe = 'yes'
							#> static method
							@staticmethod
							def __static_method(self) -> None:
								pass
							#> non-static method
							def __idkman(self) -> None:
								#> non-static properties
								self.__probs = 'no'
						
						#> accessing public properties and methods
						#> static elements
						MyClass.static_method() -> Error
						MyClass.maybe           -> Error
						#> non-static methods
						lumbago = MyClass()
						lumbago.idkman()        -> Error
						lumbago.probs           -> Error
						```

		- getter and setter methods
			- Definition:
				- To access and modify private properties of a class, getter and setter methods are used.
				- Since private properties are accessible inside the class, other methods or properties from the same class can influence it.
			- Setter methods
				- Definition:
					- Sets the value of a private property.
				- Example:
					```
					class MyClass:
						__my_var = None             #> private property, cannot be modified from the outside
						def set_var(maybe) -> None: #> setter method
							__my_var = maybe        #> sets the value using a parameter
					
					MyClass.set_var(10)            #> sets the private property through the setter method  
					```                
			- Getter methods
				- Definition:
					- Retrieves the value of a private property.
				- Example:
					```
					class MyClass:
						__my_var = 'yes'      #> private property, cannot be accessed from the outside
						def get_var() -> str: #> getter method
							return __my_var   #> retieves the value
					
					MyClass.get_var()         #> 'yes'
					#> retrieves the private property through the setter method   
					```