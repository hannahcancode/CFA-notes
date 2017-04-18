# Ruby

	* puts 				// print statement with /n
	* print 			// print statement with no /n
	* gets				// user input
	* gets.chomp 		// user input with /n chopped off
	* @variable 		// instance variable
	* &&				// and
	* ||				// or


# Atom

	* Ctrl + /			// comment out

# Scope

	* @variable			// instance variable only exists within the class
						but can be called between methods within
						the class.

# Conventions

	* snake case for variables 			// (e.g. is_it_hot) 
	* classes start with a capital 		// (Person)
	* variables start with lowercase 	// (person)
	* constants are all uppercase 		// (PERSON)

# methods

	* Ruby returns the last line of the method
		so you may not need a return statement!
	
# arrays

	* array << thing				// places thing in array
	* array.each do	|i|				// loops through array with i as current item
	* array.each_with_index	|a, i|	// as above but with index
	* array.select do 				// if true adds thing to list
	* array.join(')					// makes a string from array with joiner
	* array.pop()					// pops the last variable
	* array.map {|e| e + " rules!"} 
	* puts array					// prints each item on new line
	
# classes

	* variable = Classname.new(a, b, c)
	
	* Getter 						// gets info
	  
		def grade
			@grade
		end
	  
	* Setters						// sets info
	  
		def teacher_notes=(note)
	    	@teacher_notes = note
		end
		
	* attr_accessor(:name, :age)	// automatically sets ups getters and setters

# Files

	* File.open(filename)					// opens a new file (defaults to read)
	* File.open(filename, 'a+')				// append and read
	* opened_file.write(city)				// writes to file
	* opened_file.rewind					// rewinds
	* opened_file.close						// closes file
	* File.open(filename, '.txt', 'w+')			// creates a new file with .txt
					// extension, with write access
										
# Loops

	10.times do
	 thing 
	end

	for year in 2000...2020 		// doesn't include last iteration (...)
		puts year
	end

	for year in 2000..2020 			// includes last iteration (..)
		puts year
	end

# Strings

	.split					// splits string into array
	.join('_')				// joins arrays usings provided character
	.strip					// removes whitespace from beginning and end
	.chomp					// removes \n from end
	'=' * 15				// will repeat = 15 times ===============
	.center(12, '=')			// will centre string between characters
	.prepend				// add to beginning of string
	.concat					// add to end of string
	strings					// take 255 chars
	text					// take 65536 chars

# Variables

	var.class 				//get class
	var.to_i 				//convert to integer
	var.to_s 				//convert to string
	var.methods 				//gives all methods available (e.g. strip etc.)
	
	"blah #{variable} blah"	 				//string interpolation
	'blah #{x} blah' 				//won't change #{x} to the variable
	' \n' 				//won't change \n to new line
	%{} 				//format multiple values
	
		formatter = "%{first} %{third} %{second} %{fourth}"
		puts formatter % {first: 1, second: 2, third: 3, fourth: 4}
		
		#{'%.2f' % ten_percent} // rounds a float
	
# Flags

	first, second, third = ARGV 	// add them after the .rb in terminal
		// come into your program as variable ARGV
		#{first}	// they are strings


# CSV

	* Ruby has an inbuilt csv library

# Encoding

	 # -*- coding: utf-8 -*- 	//put at top of file
 
	\				// escape code
	
	Escape		What it does.
	
	\\				Backslash ()
	\'				Single-quote (')
	\"				Double-quote (")
	\a				ASCII bell (BEL)	
	\b				ASCII backspace (BS)
	\f				ASCII formfeed (FF)
	\n				ASCII linefeed (LF)
	\r				ASCII Carriage Return (CR)
	\t				ASCII Horizontal Tab (TAB)
	\uxxxx				Character with 16-bit hex value xxxx (Unicode only)
	\v				ASCII vertical tab (VT)
	\ooo				Character with octal value ooo
	\xhh				Character with hex value hh

# Order of operations

PEMDAS
Parenthesis, Exponents, Multiplation/Division, Add, Subtract

# Help

	ri "File#open" 		// in terminal use to get manual with examples!

# Function checklist

When writing:

1. Did you start your function definition with def?
2. Does your function name have only characters and _ (underscore) characters?
3. Did you put an open parenthesis ( right after the function name?
4. Did you put your arguments after the parenthesis ( separated by commas?
5. Did you make each argument unique (meaning no duplicated names)?
6. Did you put a close parenthesis ) after the arguments?
7. Did you indent all lines of code you want in the function two spaces?
8. Did you end your function with end lined up with the def above?
	
When you run ("use" or "call") a function, check these things:

1. Did you call/use/run this function by typing its name?
2. Did you put the ( character after the name to run it?
3. Did you put the values you want into the parenthesis separated by commas?
4. Did you end the function call with a ) character?
5. Functions that don't have parameters do not need the () after them, but would it be clearer if you wrote them anyway?

# Tests

	Fixtures
	Factory Girl
	Factory
	Faker
	Factory - traits - override booleans etc. (like approved true)