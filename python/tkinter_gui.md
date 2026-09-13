
# Tkinter GUIs
- Background
	- GUIs
		- Definition:
			- Stands for Graphical User Interface.
			- Are desktop applications that allows users to interact with content on the screen.
	- Widgets
		- Definition
			- When developing GUIs, widgets are the building blocks of an application's user interface.
			- A widget can be anything that the user sees or interacts with on the screen.
			- Widgets are the general name for these controls.
		- Types of widgets:
			- Buttons,
			- Labels,
			- Text Inputs,
			- Checkboxes,
			- Dropdowns,
			- Sliders, etc.
	- Layouts
		- Definition:
			- This controls where and how widgets appear on the screen.
			- In Tkinter, layouts are handled using geometry managers.
			- Geometry managers are special methods that place and organize widgets inside windows.
		- These methods are:
			- _pack()_
				- Used to place a widget on top.
				- Stacks widgets vertically or horizontally.
			- _grid()_
				- Arranges widgets in a table-like grid, with rows and columns.
			- _place()_
				- Places widgets at exact x, y coordinates, a manual layout.
				- If the app needs to be responsive to any screen or window size, using _pack()_ or _grid()_ is recommended.
- Tkinter 
	- Definition:
		- Is the most beginner friendly when it comes to GUI development.
		- It is Python's standard GUI library.
		- It is a sophisticated object-oriented interface.
	- GUI Creation
		- Prerequisites:
			- In order to use Tkinter, it must first be imported from the _tkinter_ module.
			- After importing, there are many methods that _tkinter_ has that are used for GUI creation.
		- Syntax:
			```
			import tkinter
			```
		- Note:
			- It is recommended to give the imported module an alias, to prevent repetitive typing.
				- Example:
					```
					import tkinter as tk
					```
			- It is possible to import all of the modules in the _tkinter_ module.
				- Syntax:
					```
					from tkinter import *
					```
			- This guide assumes that _tkinter_ has been imported with an alias of _tk_.
		- Methods:
			- _.Tk()_
				- Definition:
					- Used to make the main window or a secondary window.
				- Syntax:
					```
					<tk_object> = tk.Tk()
					```
					- Where:
						- tk_object
							- Is the name of the _tk.Tk()_ instance.
				- Example:
					```
					window: Tk = Tk()
					```
				- Methods
					- _.attributes()_
						- Definition:
							- Enables the modification of attributes of a window.
						- Syntax:
							```
							<tk_object>.attributes(<attribute>, <value>)
							```
						- Attributes:
							- -alpha
								- Definition
									- Sets the transparency of the window;
								- Note:
									- This attribute requires a float value between 0.0 and 1.0
									- 1.0 means an opaque window while values closer to 0.0 means increasingly transparency.
								- Example:
									```
									# opaque window
									window.attributes('-alpha', 1.0)
									```
					- _.deiconify()_
						- Definition:
							- Renders the window that is either in a _iconic_ or _withdrawn_ state back into view.
						- Syntax:
							```
							<tk_object>.deiconify()
							```
						- Example:
							```
							window.deiconify()
							```
					- _.destroy()_
						- Definition:
							- Destroys the _tkinter_ window and all of its associated widgets.
						- Note:
							- Destroying a window does not stop the program, only parts of code that is connected to the _tkinter_ object.
						- Syntax:
							```
							<tk_object>.destroy()
							```
						- Example:
							```
							window.destroy()
							```
					- _.iconify()_
						- Definition:
							- Lets the window enter the _iconic_ state, or letting it be minimized onto the taskbar.
						- Syntax:
							```
							<tk_object>.iconify()
							```
						- Example:
							```
							window.iconidy()
							```
					- _.iconphoto()_
						- Definition:
							- Sets the window icon to a desired _PhotoImage_ object.
						- Note:
							- The bool argument denotes whether the icon spreads to all of the icon or just the window only.
							- This method requires a _PhotoImage_ objects as an image file object.
						- Syntax:
							```
							<tk_object>.iconphoto(<bool>, <photoimage_object>)
							```
						- Example:
							```
							window.iconphoto(True, photo)
							```
						- Sample Code:
							```
							file: PhotoImage = PhotoImage(file="idkman.png")
							window.iconphoto(True, photo)
							```
					- _.geometry()_
						- Definition:
							- Sets the window size of the _tkinter_ object, with width and height.
						- Note:
							- This method also accepts another two integer arguments, determining the offset of the window from the top left of the screen.
							- The x, y offsets are optional.
							- A positive x offsets the window from the left, while a negative x offsets the window from the right.
							- A positive y offsets the window from the top, while a negative x offsets the window from the bottom.
						- Syntax:
							```
							<tk_object>.geometry("<width>x<height>-<x_offset>+<y_offset>");
							```
						- Example:
							```
							window.geometry("100x200")
							# or
							window.geometry("100x200+300+400")
							```
					- _.mainloop()_
						- Definition:
							- A loop that runs the application.
							- It waits for an event, and processes it as soon as the window is open.
						- Syntax:
							```
							<tk_object>.mainloop()
							```
						- Example:
							```
							windot.mainloop()
							```
					- _.maxsize()_
						- Definition:
							- Sets the maximum window size when the user reizes the _tkinter_ window object manually.
						- Syntax:
							```
							<tk_object>.maxsize(<max_width>, <max_height>)
							```
						- Example:
							```
							window.maxsize(1920, 1080)
							```
					- _.minsize()_
						- Definition:
							- Sets the minimum window size when the user resizes the _tkinter_ window object manually.
						- Syntax:
							```
							<tk_object>.minsize(<min_width>, <min_height>)
							```
						- Example:
							```
							window.minsize(200, 400)
							```
					- _.resizable()_
						- Definition:
							- Controls whether the user can manually drag and resize the window borders.
							- It is possible to set whether only the width or the height is able to be set as resizable or not.
						- Syntax:
							```
							<tk_object>.resizable(<width_boolean>, <height_boolean>)
							```
						- Example:
							```
							window.resizable(True, True)
							```
					- _.title()_
						- Definition:
							- Sets the title of the _tkinter_ object window.
						- Syntax:
							```
							<tk_object>.title(<string>)
							```
						- Example:
							```
							window.title("insert window title here")
							```
					- _.state()_
						- Definition:
							- Returns the current state of the _tkinter_ window object.
								- Syntax:
									```
									<tk_object>.state()
									```
								- Example:
									```
									window.state()
									```
							- It can take three string arguments to change the window state.
							- The states that it can take are:
								- normal
									- The default state.
								- iconic
									- Minimizes the window onto the taskbar.
								- withdrawn
									- Hides the window from the screen and taskbar, but does not destroy the window.
						- Syntax:
							```
							<tk_object>.state(<new_state>)
							```
						- Example:
							```
							window.state("normal")
							```
					- _.winfo_reqheight()_
						- Definition:
							- Returns the current height of the window.
						- Syntax:
							```
							<tk_object>.winfo_reqheight();
							```
						- Example:
							```
							window.winfo_reqheight()
							```
					- _.winfo_reqwidth()_
						- Definition:
							- Returns the current width of the window.
						- Syntax:
							```
							<tk_object>.winfo_reqwidth();
							```
						- Example:
							```
							window.winfo_reqwidth()
							```
					- _.winfo_screenheight()_
						- Definition:
							- Returns the current height of the screen.
						- Syntax:
							```
							<tk_object>.winfo_screenheight();
							```
						- Example:
							```
							window.winfo_screenheight()
							```
					- _.winfo_screeneidth()_
						- Definition:
							- Returns the current width of the screen.
						- Syntax:
							```
							<tk_object>.winfo_screenwidth();
							```
						- Example:
							```
							window.winfo_screenwidth()
							```
					- _.withdraw()_
						- Definition:
							- Lets the window enter the _withdrawn_ state, or hides the window from the screen or taskbar without destroying the window.
						- Syntax:
							```
							<tk_object>.withdraw()
							```
						- Example:
							```
							window.withdraw()
							```
			- _.Button()_
				- Definition:
					- Creates a clickable button on the window.
				- Syntax:
					```
					<button_object> = tk.Button()
					```
					- Where:
						- button_object
							- Is the name of the _tk.Button()_