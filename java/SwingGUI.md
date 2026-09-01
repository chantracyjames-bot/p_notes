
# Swing GUI
- Background
    - Abstract Window Toolkit (_AWT_)
        - AWT was Java's original _GUI_ library used for creating window-based applications.
        - It provides basic components fuch as buttons, labels, text fields, and menus, relying on the native operating system's _GUI_ components.
        - It was part of the _java.awt_ package and uses native platform components, leading it to be platform-dependent in appearance.
        - It provided basic _GUI_ controls and event-handling mechanisms, and serves as the foundation on which Java Swing is built.
    - Java Foundation Classes
        - It is the set of _GUI_ components that simplify desktop applications.
        - There is a common misconception that programmers think; _JFC_ and Java Swing are one and the same thing, but that is not the case.
        - _JFC_ contains Java Swing, and quite a number of other items:
            - Cut and paste — clipboard support.
            - Accessibility features — aimed at developing _GUIs_ for users with disablities.
            - Desktop Colors Features — introduced in Java 1.1.
            - Java 2D — has improved colors, images, and text support.
- Java Swing
	- Definition:
		- Is a Graphical User Interface (_GUI_) toolkit, that is part of the _JFC_ .
		- It provides a rich set of lightweight components for building desktop applications, all with a more flexible and feature-rich interface than _AWT_.
		- The _JFC_ provides a wide variety of _GUI_ components such as buttons, labels, trees, and trees.
		- It also supports a pluggable _Look and Feel_, allowing applications to have a customized appearance.
		- _JFC_ is platform-independent, allows applications to run consistently across different operating systems.
	- Swing Classes Hierarchy
		- The core GUI components such as _JFrame, JButton, JLabel, JCheckBox, JList, and JProgressBar_ are derived from base classes like _Container, JComponent_ within the Java Swing Framework.
	- Features of Java Swing:
		- Platform Independent
			- Swing components provide a consistent GUI across different operating systems without depending on native OS controls.
		- Lightweight Components
			- Swing components are written entirely in Java and do not rely on platform-specific system resources.
		- Pluggable Look and Feel 
			- Swing allows the appearance of components to be changed dynamically without modifying the application code.
		- MVC Architecture
			- Swing follows the Model-View-Controller (MVC) pattern, separating data, UI, and control logic.
		- Highly Customizable
			- Swing components can be easily customized to match specific application requirements.
		- Rich Set of Controls 
			- Swing provides advanced GUI components such as JTable, JTree, JTabbedPane, and JScrollPane.
		- Advanced Event Handling
			- Swing offers a robust event-handling mechanism to efficiently respond to user actions.
	- Advantages of Swing over AWT:
		- Image Support
			- Swing components such as buttons and labels can display images along with or instead of text.
		- Custom Borders 
			- Borders of Swing components can be easily customized to improve the UI appearance.
		- Non-Rectangular Components
			- Swing allows components such as buttons to have custom shapes, including round buttons.
		- Accessibility Support
			- Swing integrates well with assistive technologies like screen readers, making applications more accessible to users with disabilities.
	- GUI Creation:  
		- Prerequisites: 
			- In order to use the Java Swing, the library must first be imported.
		- Syntax:
			```
			import javax.swing.*;
			```
		- Note:
			- _import java.swing.*_ imports all top-level classes from the _javax.swing_ package.
			- The 'x' in _javax_ stands for extension, due to Swing being built on top of the old AWT.
		- JButton
			- Definition:
				- Is a component that allows an interactive visual button object.
			- Syntax:
				```
				JButton <buttomName> = new JButton(<buttonLabe>);
				```
				- Where;
					- buttonName
						- Is the name of the _JButton_ object.
					- buttonLabel
						- Is the label on the button when displayed.
			- Example:
				```
				JButton clickMe = new JButton("Don't Click Me");
				```
			- Methods:
				- .addActionListener()
					- Definition:
						- Adds an event listener object to a _JButton_ object's event handling list.
						- The argument is usually the single method of the _ActionListener_ interface, the abstract method of _actionPerformed_ which takes an _ActionEvent_ object.
					- Syntax:
						```
						<buttonName>.addActionListener(<listenerObject>);
						```
					- Example:
						```
						// uses a lambda expression implementing the ActionInterface's abstract method
						clickMe.addActionListener(e -> {...});
						```
					- Sample Code:
						```
						clickMe.addActionListener(e -> {
						String maybe = youShouldSay.getText();
						whatToSay.setText("you did not say "+ maybe);
						})
						```
		- JCheckBox
			- Definition:
				- Is a square toggle box with a text label, used to represent independent true/false choices or values.
			- Syntax:
				```
				JCheckBox <boxName> = new JCheckBox(<boxLabel>, <boxInitialState>);
				```
				- Where:
					- boxName
						- Is the name of the _JCheckBox_ object.
					- boxLabel
						- Is the text that is present on the check box.
					- boxInitialState
						- is the initially selected boolean, true for checked, false for unchecked.
			- Example:
				```
				JCheckBox chessStuff = new JCheckBox("Checkmate", true);
				```
			- Methods:
				- .isSelected()
					- Description:
						- Returns a boolean value to whatever state the button is in, true is ON, false if OFF.
					- Syntax:
						```
						<toggleName>.isSelected();
						```
					- Example:
						```
						turnItOff.isSelected();
						```
		- JColorChooser
			- Definition:
				- Is a class that provides a pane of controls to allow a user to manipulate and select a user.
			- Syntax:
				```
				JColorChooser <chooserName> = new JColorChooser(<colorObject>);
				```
				- Where:
					- chooserName
						- Is the name for the _JColorChooser_ object
					- colorObject
						- An instance of the Color class.
			- Example:
				```
				// default value is white
				JColorChooser colorBlind = new JColorChooser();
				```
		- JFrame
			- Definition:
				- _JFrame_ is a top-level container class extending _java.awt.Frame_, _java.awt.Window_, _java.awt.Container_, and _java.awt.Component_.
			- Syntax:
				```
				JFrame <windowName> = new JFrame(<windowTitle>);
				```
				- Where:
					- windowName
						- Is the variable that hols the JFrame instance.
					- windowTitle
						- Is the name of the window that has been created.
						- Look at the title bar of the window created using JFrame.
			- Example:
				```
				JFrame idkman = new JFrame("tarcy");
				```
			- Methods:
				- .add()
					- Definition:
						- Adds the _JPanel_ object into the _JFrame_ window.
						- In modern Java Swing, the _JFrame.add()_ method forwards this call to _JFrame_'s Content Pane (_JFrame.getContentPane().add(JPanel)_). The content pane acts as the primary layout root for any windows created by _JFrame_.
					- Syntax:
						```
						<windowName>.add(<panelObject>);
						```
					- Example:
						```
						idkman.add(pane);
						```
				- .setDefaultCloseOperation()
					- Definition:
						- Sets the default respone when the user closes the window, either by clicking the "X" button, or through any other means.
						- This method can take four different arguments, denoting what happens to the window:
							- DISPOSE_ON_CLOSE
								- Closes a specific window while leaving the other windows intact.
							- DO_NOTHING_ON_CLOSE
								- Does not close the window, leaving it to the  programmer on hwo to close the window.
							- EXIT_ON_CLOSE
								- Completely closes everything in the program.
							- HIDE_ON_CLOSE
								- Hides the window from view, can be brought back into visibility if desired.
					- Syntax:
						```
						<windowName>.setDefaultCloseOperation(<operation>);
						```
					- Example:
						```
						// closes the program when closed
						idkman.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
						```
				- .setResizable()
					- Definition:
						- Sets whether the frame is resizable by the user
					- Syntax:
						```
						<windowName>.setResizable(<boolean>);
						```
					- Example:
						```
						idkman.setResizable(false);
						```
				- .setSize()
					- Definition:
						- Sets the width and hight of the Window.
						- Inherited from _java.awt.Window_.
						- Only takes integers as arguments, denoting the number of pixels as size.
					- Syntax:
						```
						<windowName>.setSize(<width>, <height>);
						```
					- Example:
						```
						// 670 pixels in wdith
						// 690 pixels in height
						idkman.setSet(670, 690);
						```
				- .setTitle()
					- Definition:
						- Sets the window title of the JFrame object.
					- Syntax:
						```
						<windowName>.setTitle(<string>)
						```
					- Example:
						```
						idkman.setTitle("yes")
						```
				- .setVisible()
					- Definition:
						- A method that is inherited from _jave.awt.Window_.
						- Accepts a boolean as an argument.
						- By default, all newly created Swing windows or _JFrame_ window objects are invisible (_.setVisible(false)_) in memory. This allows building and positioning components without trigerring any premature graphical repaints.
						- Passing a _true_ argument validates the layout tree, calculates screen coordinates, binds native OS window handles, and draws the component hierarchy to the screen.
					- Syntax:
						```
						<windowName>.setVisible(<boolean>);
						```
					- Example:
						```
						idkman.setVisible(true);
						```
		- JFormattedTextField
			- Definition:
				- A single-line text field that restricts input according to a defined pattern.
				- Useful for having an input where only numbers are allowed.
			- Syntax:
				```
				JFormattedTextField <fFieldName> = new JFormattedTextField(<formatObject>);
				```
				- Where:
					- fFieldName
						- Is the name of the _JFormattedTextField_ object.
					- formatObject
						- Used to specify what type of format the text field should take, e.g. _MaskFormatter_.
			- Example:
				```
				JFormattedTextField stringsOnly = new JFormattedTextField(new MaskFormatter("(##) ###-###-####"));
				```
			- Methods:
				- .setColumns()
					- Definition:
						- used to set the number of columns of the text field.
					- Syntax:
						```
						<fFieldName>.setColumns(<int>);
						```
					- Example:
						```
						stringsOnly.setColumns(15);
						```
		- JLabel
			- Definition:
				- A class based on JComponent that is used for displaying non-editable text or images.
				- It can also be used to display images using _Icon_ objects.
			- Syntax:
				```
				JLabel <labelName> = new JLabel(<labelLabel>, <labelAlignment>);
				```
				- Where:
					- labelName
						- Is the name of the _JLabel_ object.
					- labelLabel
						- Is the text that the _JLabel_ object will display.
					- labelAlignment
						- Where the text is aligned, can be Centered, Right, or Left.
						- This arguemnt is optional.
				- Example:
					```
					// justifies the text to the right
					JLabel whatToSay = new JLabel("What to say?: ", JLabel.RIGHT);
					```
			- Methods:
				- .setFont()
					- Definition:`
						- Sets the font of the _JLabel_ object.
						- Takes a _Font_ object as an arguemnt.
					- Syntax:
						```
						<labelName>.setFont(<fontObject>);
						```
					- Example:
						```
						whatToSay.setFont(new Font("Serif", Font.ITALIC, 21));
						```
				- .setHorizontalAlignment()
					- Definition:
						- Sets the horizontal alignment of a _JLabel_ text.
						- Takes in any of the alignment constants of Swing.
					- Syntax:
						```
						<labelName>.setHorizontalAlignment(<direction>)
						```
					- Example:
						```
						whatToSay.setHorizontalAlignment(JLabel.CENTER);
						```
				- .setText()
					- Definition:
						- A setter method that sets the text in the _JLabel_ object to whatever the argument is.
					- Syntax:
						```
						<labelName>.setText(<string>);
						```
					- Example:
						```
						whatToSay.setText("you did not say " + maybe);
						```
		- JPanel
			- Definition:
				- It is a lightweight intermediate container that is a subclass from JComponent.
				- It holds and groupds components together before placing them into the frame
				- The constructor of this class can take any _LayoutManager_ layouts, like:
					- FlowLayout
					- BorderLayout
					- BoxLayout
					- CardLayout
					- GridBagLayout
					- GridLayout
					- GroupLayout
					- SpringLayout
			- Syntax:
				```
				JPanel <panelName> = new JPanel(<panelLayout>);
				```
				- Where:
					- panelName
						- Is the name of the panel to be used.
					- panelLayout
						- Is the panel to be used, refer to the Definition of JPanel for more information.
			- Example:
				```
				// panel layout using FlowLayout()
				JPanel pane = new JPanel(new FlowLayout);
				```
			- Methods:
				- .add()
					- Definition:
						- A method that is inherited from _java.awt.Component_.
						- It inserts any of the argument components inot the internal _Component[]_ array that is maintained by the _JPanel_ object.
						- Is is where the _LayoutManager_ manage the position of each component. The _FlowLayout_ automatically positions each compoonnts side-by-side in the exact order they were added to the _Component[]_ array.
					- Syntax:
						```
						<panelName>.add(<componentObject>);
						```
					- Example:
						```
						pane.add(whatToSay);
						```
		- JPasswordField
			- Description:
				- Is a component that presents a single-line text field that obscures characters to securely capture passwords.
			- Syntax:
				```
				JPasswordField <pfieldName> = new JPasswordField(<pfieldSize>);
				```
				- Where:
					- pfieldName
						- Is the name of the _JPasswordField_ object.
					- pfieldSize
						- Is the initial size of the text field to certain number of columns
						- Do note that it does not cap the maximum input length, only sets the width of the text field.
			- Example:
				```
				JPasswordField givLogin = new JPasswordField(10);
				```
			- Methods:
				- .getPassword()
					- Definition:
						- Returns a char[] value from what the user has typed in.
					- Syntax:
						```
						<pfieldName>.getPassword();
						```
					- Example:
						```
						givLogin.getPassword();
						```
		- JRadioButton
			- Description:
				- Is a component that presents circular buttons for mutually exclusive options.
			- Note:
				- This component requires to be grouped in a _ButtonGroup_ object.
			- Syntax:
				```
				JRadioButton <radioName> = new JRadioButton(<radioLabel>);
				```
				- Where:
					- radioName
						- Is the name of the _JRadioButton_ object.
					- radioLabel
						- Is the text present next to the button.
			- Example:
				```
				JRadioButton idkWhatToNameThisThing = new JRadioButton("This has a name");
				```
		- JTextArea
			- Definition:
				- Is a component that displays a box of text that the user can edit.
			- Syntax:
				```
				JTextArea <textAreaName> = new JTextArea(<textAreaLabel>, <textAreaRows>, <textAreaColumns>);
				```
				- Where:
					- textAreaName
						- The name of the _JTextArea_ object.
					- textAreaLabel
						- The text that appears in the _JTextArea_ object.
					- textAreaRows
						- An integer that defines the number of rows in the text area.
					- textAreaColumns
						- An integer that defines the number of columns in the text area.
			- Example:
				```
				JTextArea editMe = new JTextArea("Don't Edit Me");
				```
			- Methods:
				- .append()
					- Definition:
						- Appends a string to the text area, used to add text independent from the initial declaration of the object.
					- Syntax:
						```
						<textAreaName>.append(<string>);
						```
					- Example:
						```
						editMe.append("edit here");
						```
				- .setLineWrap()
					- Definition:
						- Takes in a boolean to indicate whether text should wrap around or not.
					- Syntax:
						```
						<textAreaName>.setLineWrap(<boolean>);
						```
					- Example:
						```
						editMe.setLineWrap(true);
						```
				- setWrapStyleWord()
					- Definition:
						- Takes in a boolean to indicate whether words should stay together when it line wraps or not.
					- Syntax:
						```
						<textAreaName>.setWrapStyleWord(<boolean>);
						```
					- Example:
						```
						editMe.setWrapStyleWord(false);
						```
		- JTextField
			- Definition:
				- Is a component that allows users to type single-line text input.
			- Syntax:
				```
				JTextField <fieldName> = new JTextField(<fieldSize>, <fieldAlignment>);
				```
				- Where:
					- fieldName
						- Is the name of the _JTextField_ object.
					- fieldSize
						- Is the initial size of the text field to certain number of columns
						- Do note that it does not cap the maximum input length, only sets the width of the text field.
					- fieldAlignment
						- Where the text is aligned, can be Centered, Right, or Left.
						- This arguemnt is optional.
			- Example:
				```
				JTextField youShouldSay = new JTextField(10);
				```
			- Methods:
				- .getText()
					- Definition:
						- A getter method that retrieves any text that the user may have typed in the text field.
					- Syntax:
						```
						<fieldName>.getText();
						```
					- Example:
						```
						youShouldSay.getText();
						```
		- JToggleButton
			- Definition:
				- A button with two states, on or off, that remains visually pressed down when clicked and pops back up when clicked again.
			- Syntax:
				```
				JToggleButton <toggleName> = new JToggleButton(<toggleLabel>, <toggleInitialState>);
				```
				- Where:
					- toggleName
						- Is the name of the _JToggleButton_ object.
					- toggleLabel
						- Is the text that is present on the button.
					- toggleInitialState
						- The initially selected boolean, on or off.
			- Example:
				```
				JToggleButton turnItOff = new JToggleButton("stop", false);
				```
			- Methods:
				- .isSelected()
					- Description:
						- Returns a boolean value to whatever state the button is in, true is ON, false if OFF.
					- Syntax:
						```
						<toggleName>.isSelected();
						```
					- Example:
						```
						turnItOff.isSelected();
						```
		- ActionListener
			- Definition:
				- Is an interface that is used to create event listeners.
				- Event listeners are objects that define functions that are called when a certain even happens; like when a user cliks the mouse of presses a key on the keyboard.
				- To create an event listener, the ActionListener is inherited (implemented) to a child class.
				- Do note that the ActionListener and AciontEvent classes are imported before any code can be created using them. They are imported from the _java.awt.event_ package.
				- Syntax:
					```
					import java.awt.event.ActionEvent;
					import java.awt.event.ActionListener;
					```
			- Syntax:
				```
				<modifier> class <className> implements ActionListener {
				<modifier> <dataType> actionPerformed(ActionEvent <eventObject>) {...}
				}
				```
			- Example:
				```
				public class eventStuff implements ActionListener {
				// the class must define the abstract method
				public void actionPerformed(ActionEvent yes) {
				System.out.println("smth smth");
				}
				}
				```
		- SwingUtilities
			- Definition:
				- Java Swing components are not thread-safe, it is vulnerable to memory corruption and visual glitches.
				- To prevent any unexpected problems, Swing enforces a single-theaded architecture.
				- Almost all code that Swing creates, modifies, or renders must be executed on a single thread, calle the Event Dispatch Thread (_EDT_).
				- When constructing or modifying any of the _JComponent_ through main(), it is directly accessing Swing components from the Main Thread while EDT is actively trying to render them.
				- Having two threads to manipulate the same memory address simultaneously without any form of synchronization can cause unexpended threading bugs.
				- To solve this, the _.invokeLater()_ method is used.
				- The Main Thread vs EDT:
					- Main Thread
						- When launching a normal Java appication, the Java Virtual Machine (JVM) starts executing on the Main Thread.
						- It is responsible for executing the entry point (_public static void main(String[] args)_) and the general application logic.
					- EDT
						- When a Swing application is launched, it starts a second background thread—the EDT.
						- It is responsible for painting graphics, managing window repaint cycles, and handling user inputs—like button clicks, key presses, mouse movements, etc.
				- Solution:
					- Main Point:
						- This method acts like a safe bridge between the Main Thread (or other threads) and to the EDT.
						- It takes a Runnable task (can be in the form of a lambda expression) and places it onto the back of Swing's FIFO System Event Queue.
						- The calling thread (e.g, The Main Thread.) does not stop or wait, it places the task on the queue instantly and resumes execution.
						- When the EDT finishes its current tasks, it pulss the Runnable task off the queue and executes it safely on the EDI.
					- Without it:
						- Failing to use _.invokeLater()_ method can break Swing's threading policy and lead to unpredictable behavior.
						- Two threads reading and writing component properties at the same time can cause Race Conditions.
						- Even if the application seemingly runs perfectly but under the hood, there is a chance that the program might fail due to heavy CPU load.
						- Changes made to any components on background threads can often trigger a screen refresh, rendering the GUI looking unresponsive.
			- Methods:
				- .invokeLater()
					- Definition:
						- Asynchronous and Non-Blocking.
						- Posts the and immediately continues.
						- Used for almost all UI initialization and standard updates.
					- Syntax:
						```
						SwingUtilities.invokeLater(<runnableTask>);
						```
					- Example:
						```
						SwingUtilities.invokeLater(() -> {...});
						```
				- .invokeAndWait()
					- Definition:
						- Synchronous and Blocking.
						- Posts the task and blocks the calling thread until the EDI finishes executing the task.
					- Note:
						- Never call _.invokeAndWait()_ from within the EDT itself, or it might cause the application to permanently deadlock.
					- Syntax:
						```
						SwingUtilities.invokeAndWait(<runnableTask>);
						```
					- Example:
						```
						SwingUtilities.invokeAndWait(() -> {...});
						```