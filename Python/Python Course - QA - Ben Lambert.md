
## Junior Developer

### Module 1 - Python Language Features

#### Introducing the Python Language

In this course we will learn:

- The purpose of the Python language;
- The concept of syntax;
- The purpose of the interpreter;
- The concept of code blocks;

#### Introducing the Python Language

The purpose of the Python language is to create and control **Objects**

**Objects**

- Are a means of modeling real world and abstract concepts
- They are Pythons low level building block
- An object's type is the name of the of the concept being modeled
- We model concepts by extracting meaningful attributes and methods

Python is an application built on top of the **C** language, when we start the **Python App**, we start the **Python Runtime**, a key feature of the Python Runtime is the **Interpreter**

**Interpreter**

- This is a program that understands the Python language
- Its role is to interpret the Python language and convert it to actions, such as:
	- Creating an object;
	- Performing an operation;
	- Calling a method;

In essence we feed the interpreter with code, that code then instructs the interpreter to interact with the objects in some way

There a set of rules that dictate how the code should be structured, when reading the code the interpreter compares it against the pre-established rules and confirms if the code is properly built 

If everything matches, the interpreter follows the rules created by us, if not it triggers an error

**Syntax**

	Just like human languages, programming ones have a set of rules that must be followed
	The same way we use a set of letters and symbols Python uses **Keywords**
	Python contains roughly 30 to 40 keywords
	These words have special meaning to the interpreter
	Actions will be determined by the different combiantion Keywords, Symbols and the names we give to objects

In programming we can see the different actions as a set of templates, these contain:

- Type
- Attributes
- Methods
- Symbols

Python can be written in any text based program, such as Notepad all the way up to VS Code with a `.py` extension

The second option is to run it straight from a terminal, we will see this more in depth in the future

The interpreter goes from top to bottom and left to right, just like the English language

#### Introduction to Code Blocks

Code blocks can be seen as paragraphs

Lines of code related to each other that have to be run all at once

Many programming languages use  `{}` in order to specify the beginning and end of lines of code.

Python on the other hand, uses indentation, which is a free space at the beginning of a line/block. The interpreter counts the number of white space characters.

**This indentation can either be spaces of tabs**

No white spaces indicate the first block
    4 white spaces indicate the second block
         8 white spaces indicate the third block

Each new level of indentation creates a nested block. The goal of indentation is to have the same blocks of code aligned

This still has some downsides:

- Its fairly easy to mistype a white space
- Both *spaces* and *tabs* are white space

The Python community established a 4 white space as the correct amount for each level of indentation

**Indentation is a real issue specially for fresh developers, especially when copying code from the internet**

#### Introduction to Text Editors

Code files have to be simple text, this is the reason why we use programs that do not add any formatting to the text.

In order to help developers with identifying errors, debugging and writing code, code editors have been created.

#### Introduction to the Python Interpreter

In other lessons we spoke about **Python Runtime**, which is where the **Interpreter** "lives" in.

As previously seen, Python is just an application that knows how to read Python code and interpret the actions within it.

As we saw, Python code can either be in a `.py` file which will then be transferred to the interpreter when we decide to run it, or, we can simply run it straight from the terminal if we go into interactive mode.

For the interactive mode we do:

	python3

This is not the best approach since the code we write is not saved anywhere, although it has some use cases, mainly when learning. Now that we are in interactive mode we can do:

	1+2

To this we get the answer 3, yet, we still did not work with objects so far, or did we?

Python has various ways to interpret the type of data we dealing with (we will see this in bigger depth further) and although we did not specify the data type, being an integer in this case, Python automatically recognizes whole numbers as being integers, being each of these, an object by itself

Lets try a different example now:

	10 + 3.5

At this stage we are dealing with an integer and a float number, yet we still manage to get the perfect result.

Lets see it from this perspective, when we feed data to Python, it stores it in an object, it then determines the operation to perform and then call the code responsible for handling that operation 

That code may or may not return an object

In case we want to use one of these results (objects) to further use it in our program, we can link to a name, this process is called **Name Binding** aka variable

Lets imagine we want to use the value of Pi, which is 3.14:

	pi = 3.14

We have now successfully created our first object linked to a name, being a **stand-in** (standard input) for our float object

If we run:

	type(pi)

We will get the class, in this case **float**

If we run:

	pi

We will get the object value, which is **3.14**

As we can confirm, even without providing Python with the data class, it knows what it is dealing with, the same is for text

Lets see the next example:

	"Hello World!"

The answer to this is `Hello World!`, and, based on the quotes we used, Python knows we are dealing with a **string**. We can either use "" or '', yet we should stick to one for the entire program

- Objects are made of attributes and methods 
- Attributes define meaningful aspects of a type
- Methods implement meaningful behaviors of a type 
- Bound names (variables) serve as a stand-in for an object

Since this name binding references a string, we can call any of the string methods which exist for strings 

To see further lets create a variable named greeting:

	greeting = "Hello World!"

Now that our variable is created, lets run:

	dir(greeting)

The result is out of my writing capabilities, but it shows all we can do with text.

As a few examples we have:

- join
- lower
- upper
- split
- replace

If we add **lower** to our variable as such:

	greeting.lower()

The result is:

	hello world!

If we do:

	greeting.upper()

The result is:

	HELLO WORLD!

If we do:

	greeting.replace("World", "Universe")

The result is:

	Hello Universe!

We can also perform operations in objects, for example

	3 + 1

**3** and **1** are objects and **+** is the operator, with integers this is pretty intuitive, yet with other classes it also works, for example

	"Hello" x 3

Will give us

	Hello Hello Hello

Along with **int** (integers) **char** (characters) **str** (strings) we also have **bool** (boolean). 

Boolean expressions are based on true or false, so if we run:

	3 > 1

Python will reply to us:

	True

If we run:

	1 > 3

Python will reply to us:

	False

Understanding if something is true or false is basis of decision making in programming, such as:

- Is this date correct?
- Is this user authenticated?
- Is this data correct?

#### Dictionaries in Python

Dictionaries are **key value pairs** in Python.

Key value pairs consists of two related objects, for example

| Key                  | Value          |
| -------------------- | -------------- |
| Name                 | Python         |
| initial_release_date | Feb 20th, 1991 |
| ID                   | 32             |
Key value pairs is a recurring theme in programming, these are extremely versatile because of how many concepts can be conveyed in therms of key-value pairs

From the perspective of the table **above** we can see that even variables follow this concept, when we bind a name with a value

Key value pairs allow us to store great amounts of information which is what makes them interesting, this because each individual key value pair can describe one aspects of the whole data being stored

##### Creating dictionaries in Python

**1st**

Lets create a a dictionary for `cat`:

	cat = {"name": "Ada", "Age": 3}

When we run:

	print(cat)

We get:

	{"name": "Ada", "Age": 3}

As we can see we can store multiple attributes of in a single object

**2nd**

Python allows us to create our object type dictionary, as such:

	nothing = dict()

When we `print` it:

	print(nothing)

We get:

	{}

Simply because it is empty

In dictionaries 

- `key` and `value` are separated by a `:` 
- `value pairs` are separated by a `,`
- A dictionary's key must be hashable (we will see this further)

With dictionaries we can interact directly with the whole dictionary **or** with its elements individually, although the rules differ a bit

##### Creating and managing dictionaries in Python

###### Creating
Lets begin with an empty dictionary, binding it to the name cat:

	cat = {}

###### Adding a Key-Value Pair

In order to interact with specific values we reference them by key, a bit like a list so in order to add info to the dictionary we do:

	cat ["Name"] = "Ada"

The first part, related to the `Name` is the syntax key for the value `Ada`. When we ask for this the interpreter will iterate for the key and if a value exists it will return it to us.

Now lets add more info to the `cat` dictionary, in this example **age**:

	cat ["Age"] = 3

When we print `cat`:

	print(cat)

We get:

	{"Name": "Ada", "Age": 3}

###### Incrementing a Value for a Specific key

Now lets imagine that `Ada` has birthday, we need to increment the value by 1, so we do:

	cat ["Age"] += 1

When we print it:

	print(cat)

We get:

	{"Name": "Ada", "Age": 4}

###### Deleting a Key-Value Pair

In case we want to **delete** a **key** from our dictionary, we can use the `del` function, as such:

	del cat ["Age"] 

###### Querying a Dictionary

In case we want to fetch specific **Key-Value** pair, we can use **boolean** expressions with the **in** operator :

	"Name" in cat
	True

	"Fav_Toy" not in cat
	True

###### Alternatives

We can also fetch a specific **Key-Value** pair using the `get` function:

	cat.get("Name")
	"Ada"

And we can change the value of a key using the `update` fucntion:

	cat.update({"Age": 5})

When we print it:

	print(cat)

We get:

	{"Name": "Ada", "Age": 5}

###### Querying only Values or Keys

If we want to fetch all the **keys** we can do:

	cat.keys()
	dict_keys(["Name", "Age"])

If we want to fetch all the **values** we can do:

	cat.values()
	dict_values(["Ada", 3])

###### Merging Dictionaries

Lets imagine for instance we need to update a dictionary with values from another dictionary

In this case we have 2 different dictioanries:

- Configuration
- User Settings

Lets create them:

	configuration = {"enable_sound": False, "resolution": (1920, 1080)}

	user_settings = {"enable_sound": True}

For us to merge them we do:

	configuration |= user_settings

When we print it:

	print(configuration)

We get:

	{"enable_sound": True, "resolution": (1920, 1080)}

Since we specified that the `configuration` is the same as `user_settings` the values in `configuration` are updated with the ones in `user_settings`

If we invert the logic, `user_settings` would inherit the **values** in `configutation`

#### Intro to Python Objects

Python is a program that based on C that runs on all OS's.

The Python Runtime reads the Python code, turning it into objects

Objects model real world concepts by defining its attributes and behaviors which best describe the concept we are trying to model.

This may seem abstract, but lets use a cat has an example

A cat will have a set of **Attributes** and **Values**

| Atribute | Value    |
| -------- | -------- |
| Name     | Ada      |
| Age      | 3        |
| Breed    | Lewinska |
| Weight   | 5kg      |
| Play     | *method* |
| Meow     | *method* |

The entire goal of modeling concepts and behaviors is to make it easier for developers to work with data

Python considers both data and methods to be attributes, however these are different concepts, since behaviors can do things

Methods is where our code lives, and the attributes the different variables inside a single object that will feed our code with date 

The concept being modeled is referred to as the **objects type**, for example, object's type - cat / heart / ball

How about abstract concepts, such as numbers, lists and texts, why would these become objects?

We do so in order to have them behaving just like in real world, we create the different parts that constitute an object so we can interact with each one individually, changing the final result

We can see objects as lego bricks, these have their own attributes, size, color, weight etc, which can be used on its own, or, become a fully function part of something bigger

To better understand this, we will create a `lemonade_stand` object

Type: lemonade_stand

| Attribute      | Type     | Vale |
| -------------- | -------- | ---- |
| Inventory      | Float    | 15   |
| Sales          | Float    | 1.25 |
| Price          | Float    | .25  |
| Serve          | *method* |      |
| Calculate Loss | *method* |      |
	There are still **3** things we did not see about methods, they can:
	- Accept Input;
	- Return Output;
	- Interact with Attributes;

We need to build the `serve` method in a way that it will prompt the costumer to tell us how many cups of lemonade it wishes to have

Along with this, for **every** cup sold, it will subtract 1/2 lemon from the inventory and add its respective value to the sales 

The `calculate` method will add all the money we are loosing due to mistakes

#### Modeling a Concept

For this module we will build an object!

	The concept of this object is a counter that will increment its value by 1, every time an event occurs 

From here we can see 2 things:

	counter that will increment its value by 1

- This is to say the attribute references an integer

And

	"Every time an event occurs"

- A method to model the even that causes the number to increment

We can see this has:

| Atribute | Value                               |
| -------- | ----------------------------------- |
| Number   | 0                                   |
| Count    | Method - Increment by 1 when called |

This can roughly be translated into code as such

	class Counter:
		def __init__(self):
			self.number = 0
		de count(self):
			self.number += 1

Lets see what we can understand from our code

- `class` is just a blueprint to create an object

- `Counter` is the object type

- `number` an attribute mentioned 2x in our code, once set to 0 when the object is created and one set to increment by 1

With this in mind, every time we get invoke the `Counter` we know that it will start at 0 and increment itself

#### Introduction to Flow Control

Lets imagine a simple game.

A person thinks of a number, and the other person has to guess it.

Here we have 2 main components:

- Processing the answer
- Give it a `yes` or `no` answer

The same happens in programming.

###### if, elif, else

Lets say for example we have built a program where we ask a user what is its favorite language. Based on certain conditions we will give an appropriate answer.

For this we will need to see the following statements:

- `if
- `elif
- `else

Lets create our program:

	if favorite_programming_language == "python"
		print("The best!")
	elif favorite_programming_language == "java"
		print("Someone likes phones")
	elif favorite_programming_language == "assembly"
		print("Old School")
	else
		print("No need to have one!")

What we did here is to create a question, the answer can meet 4 different conditions:

- `Python`
- `Java`
- `Assembly`
- `Default`

For all the possibilities we have thought of we can create an answer, this is the `elif` statement

For an answer we haven't thought of we have the `else` statement

###### Loops

Sometimes we need to keep asking a question until we get the correct answer, for example in a guessing game. Here we use loops, these can be:

- `Forever`
- `While`

**Forever**

A `for` loop is used to loop over a constrained collection of objects

Lets imagine we want to send an email to all the emails in a list:

	for email_address in ["example@mail.com", "example2@mail.com"]
		send_welcome_message(email_address)

This will iterate through all the emails and follow the instructions on `send_welcome_message` for each of them

We can also break from a `for` loop

	for player in players:
		if player.is_player_one():
			print("Press the spacebaar to start!")
			break

What we will be doing here is to search for a player in a collection of player
If this player is the player 1 we present a message and break from the loop
In case not 

**While**

A `while` loop continues to pose a question until a condition is **false** or until we intentionally break it, as such:

	while game_is_running:
		render_graphics()

Or

	while true:
		guess = input ("Guess the correct number? ")
		if guess == "9":
			print("You rock!!")
			break
		else:
			print("Sorry, try again!")


#### Intro to `if elif else

Lets analyze the following piece of code

             if true:

                            pass

             elif true:

                            pass

             else

                            pass

Python considers what comes after the `if` `:` statement to be true

This logic is based on Boolean expressions, for that we need to analyze them in order to understand the basis of this concept

             Please note that the `pass` keyword does not do anything and serves as a placeholder for future code

Boolean expression are based in the simple idea of:

- yes / no

- true / false

- 0 / 1

When the interpreter finds the keyword **true** it knows we are making reference to a Boolean expression with the value `true` and vice versa

Booleans are commonly produced as the result of performing operations or from calling code, which produces a result after comparing 2 statements

We can even use the `and` or `or` operators to compare 2 different Boolean expressions, as such

             a = 2

             b = 3

             print(a == 2 or b == 3)

This will give the output

             True

Lets see another example

This one happens to be very interesting:

             command = input("Enter command: ")

             age = 42

             if command in ["cook", "bake", "read"]:

                            print("Sounds fun")

             elif command == "jog" and age > 40:

                            print("Its a trap")

             elif command == "learn Python":

                            print("Way to go")

             else:

                            print("I did recognize the command")

We start out by creating 2 variables:

- input (to receive data from the user)

- we inform the compiler of an age, in this case 42

From here we start to play around with this 2 pieces of data, initially we tell the compiler that

- `if` the input from the user matches a value in the list `["cook", "bake", "read"]` we reply `Sounds fun`

- In case this did not happen we create a 2nd possibility with the first `elif` statement, in this case if the answer is `"jog"` and the age is above 40, which is then the condition is met and we print `"Its a trap"`

- As in the previous example we create another possibility, which is if the answer from the user is `"learn Python"` we answer `"Way to go"`

- In case non of these conditions is met we just throw the default answer `"I did recognize the command"`

###### Nesting `if` Statements

It is also possible to nest `if` statements, this means to have `if` inside `if` with the proper indentation of course

Lets see the following example:

             if content.isa_video():

                            if content.type == "mpeg":

                                          do_one_thing()

                            else:

                                          do_another_thing()

Here we have:

- a name `content`

- a method `isa_video`

- an attribute `type`

If in the first `if` statement the conditions are met, met and the both `content` and `isa.video` are present we move to the next `if` statement, once again, if the conditions are met we follow to `do_one_thing()` if not we break the Boolean with `else`


#### Exploring `for` loops

Loops are used to repeat a block of code until a certain condition is met

- The `while` loop keeps itself on going until a false condition is found, which breaks the loop, or if we use the `break` keyword

- The `for` loop is used to bind an object in a collection, such as iterating through a list, set, tuple or dictionary. Every time the loop progresses, it picks the new result (object) to the code we created

###### for

Lets see the following example:

             letters = ["a", "b", "c", "d"]

             for letter in letters:

                            print(letters)

Here we have:

- A variable `letters`

- A `for` loop

- A name `letter`

- A `print` function

What this code will do is to iterate through the list of letters and print them one by one.

We can break and continue `for` loops as we wish

###### Break

Break as an example:

             letters = ["a", "b", "c", "d"]

             for letter in letters:

                            if letter == "c":

                                          break

                            print(letters)

What will happen now is the following

- `for` loop will check the list

- Letter == to a

- `print`

- `for` loop will check the list

- Letter == to b

- `print`

- `for` loop will check the list

- Letter == to c

- `break` the loop

###### Continue

Continue as an example:

             letters = ["a", "b", "c", "d"]

             for letter in letters:

                            if letter == "c":

                                          continue

                            print(letters)

- `for` loop will check the list

- Letter == to a

- `print`

- `for` loop will check the list

- Letter == to b

- `print`

- `for` loop will check the list

- Letter == to c

- Since the letter equals to c we will not jump straight to `print` instead we `continue` the loop, which brings us to the letter d, resulting in ignoring the letter c

###### Range

It may also happen that we need to perform an operation for a specific number of times, instead of having a condition to `break` / `continue` the loop, this is where the **range** built in function comes into play. It will automatically iterate through all the integers in the `range` we specified

Here is an example:

             for number in range(10)

                            print(number)

What this code does is to print all the numbers from 0 to 10. If we want to skip a number, we can add the continue loop, if we want to stop at a specific number we can break it based on a condition

###### Enumerate

There is a built function called `enumerate` which can take a collection as input, this is a function that returns a collection of **tuples**

###### Tuples

`tuples` are a fundamental part in Python since they can store different values under one single variable, along tuples we have lists, dictionaries and sets, we will see more about this in `collections`

Tuple unpacking allows us to bind multiple names to corresponding objects inside of a `tuple`

Unpacking also works with the name binding of `for` loops. Using this with the built in enumerate function enables us to bind one name to the loop counter and another to the value

Here is an example:

             letters = ["a", "b", "c", "d"]

             for i, value in enumerate(letters):

                            print(f'The loop index is: {i} and the value is: {value}')

The result is:

The loop index is: 0 and the value is: a

The loop index is: 1 and the value is: b

The loop index is: 2 and the value is: c

The loop index is: 3 and the value is: d

What this code will do is:

- `for` count `i`

- `for` `enumerate` function, iterating through the list of letters provide the result to the variable `value`

These built in function have their use cases, however those are specific to the code
#### Exploring `while` loops

This class is a resume of all we have seen about `while` loops, still there is something we should check, lets consider the following program:

             answer = 9

             guess = input("Guess a number between 0 and 10: ")

             guess = int(guess)

             if guess == answer:

                            print("You win!")

             else:

                            print("You lost!")

Lets break it down:

- We start of by creating a variable `answer` with the value of 9

- We then proceed to ask the user for `input` under and store its value in the `guess` variable

- We specify that the `guess` variable will be an integer

- We build the flow by creating an `if` statement, if the value of `guess` equals the `answer` the user wins

- `else` user looses

Its important to note that we can create loops inside loops, but we need to be very careful on how we set the conditions to break free from it, since this can get us in an infinite loop forever

#### Callables

Callables are used to take actions whereas as conditional statements are used for making decisions

The concept of a callable is named after this basic structure, they take input perform an action and serve output

Object's methods are examples of a callable, when we invoke it the code inside it runs and returns a result

For example (in a terminal):

             greeting = "hello, world"

Note that we wrote everything down case, to make it title friendly we run:

             greeting.title()

We have now added our `greeting` variable to the `title()` function, the result is:

             Hello World

Lets now see the `replace` callable:

             greeting.replace("world", "universe")

The result is:

             hello universe

###### Functions

These are a common means of modeling self contained actions, allowing developers to create individual pieces of code that serve a developer-defined purpose. Since `functions` are callables, they allow input, they perform an action and they spit back a result.

The syntax to define a function starts with the `def` keyword followed by the `name` we want to attribute it which defines its purpose

After this, we need to define the callable's inputs:

- When referring the input used to define (build) a function we refer to `parameters`;

- When referring the input used to call (fill) a function we refer to `arguments`;

Yet there is no problem if we mix them together

- Parameters are specified inside `()`;

- These are name bindings for objects that will be used when a callable is called;

- Parameter names are finished with `:` and a new line;

Contents

- These are indented followed by our code, when the interpreter sees this, it knows that we just created a new function;

- The code inside of the `function` is what runs when the function is called;

As an example:

             def calculate(number):

                            pi = 3.14

                            return number * pi

- Here we created the calculate function with a `parameter` set to `number`

- We specified a variable named *pi*

When we call a function, first we specify its name with its input inside the parenthesis

#### Introduction to Collections

Collections are object types used to store other objects.

There are several different types of collections included in Python's standard library, yet 4 of them are so common that they are included in the syntax, these are:

- List object:

They are most commonly used to store related objects, although this is not a rule

             These can:

             Have object added

             Have object removed

             Be sorted

             Be reversed

             Be searched

- Set object:

Similar to lists but they cant have duplicated entries, removing them automatically, they are useful when we require a collection of distinct objects. Sets have some limitation, for example, we cant store a list inside of a set, although often they are used to remove duplicated entries out of lists

             These can:

             Contain only unique objects

             Have objects added and removed

             Be searched

             Be compared to **other** sets

- Dictionaries

This in on top of the list for the most used objects, and we fetch the info from them by using a keyword, due to being a collection of key-value pairs

             These can:

             Have objects added which are bound to keys

             Have objects removed

             Be searched

             Be merged with other dictionaries

- Tuple

A tuple is a limited type of list, meant to store a fixed number of related objects

#### Python introduction to built in functions

Python's built in functions fall under different groups depending on their purpose.

###### Sequences

First up, functions are designed to interact with sequences. A sequence is an object with multiple sequential values

Examples:

             sum([1, 2, 3, 4])

- This function will add all the numbers under a list

             min([43, 56, 92, 23])

- This function will the smallest number under a list

             max([43, 56, 92, 23])

- This function will the largest number under a list

             len("hey")

- This function will show the number of characters in a string

This category is related in some aspect with sequences

###### Object Types

This section details how we can convert objects from one type to another object of a given type, or, to create a new object of the given type.

As an example:

	number = "100"

We just created a variable with a `str` 100. If we try to add it to a number, we will get an error

	number + 1

So what we have to do is to change the object type into `int`  

	number = int(number)

And just like that with the `int ()` function we changed the object type

###### Data Enconding

This revolves around `Unicode` which is an information technology standard for the consistent encoding representation, and handling of text expressed in most of the worlds writing systems.

Basically it contains all the letters and symbols in the world, which are assigned a specific code, when a letter is written in the backend a code is taking place which is then translated to binary 

###### Functions related to objects

Python provides quite a few functions which are able to inspect and interact with objects

As an example (on the terminal):

	class Counter:
		def __init__(self)
			self.number = 0

Here we created a `class` named `Counter` with a function called `__init__`

The value of the `argument` is 0

If we run:

	callable(Counter)

The answer is:

	True

Means this that there is a callable object named `Counter`

If we ask the `callable function` if `"hello"` is callable:

	callable("hello")

We get:

	False

###### Functions used for name bindings

This functions are all used to inspect which names the runtime has bound.

The `dir` function accepts an object as input and returns a list containing all the attributes and methods bound to that object:

If we run:

	dir(counter)

We get:

	['__class__', '__delattr__', '__dict__' ]...

##### Functions used for input and output

Most applications contain a GUI, yet since these give too much work to build, we just go for the terminal based options.

The `input` and `print` functions allow us to receive and provide data to an user.

These are used as any other functions, we just evoke them and provide all the needed arguments inside the parenthesis.

#### Introduction to  Comments and Docstrings

Since sometimes our code can be hard to understand we have the option to include notes in our program

These comments can be:

- Single line;
- Multi line;

**Single Line**

These comments are creating by adding an `#` before the comment, we can place:

- Before the code;
- After the code;
- On the same line of the code

As an example:

	people_to_know ["lovelace", "Curry", "tesla"]
	# convert the names to title for consistency
	people_to_know = [people.title() for person in people_to_know]
	count_of_people = len(people_to_know) # number of invites to send

**Multi Line**

These comments are creating by adding a set of `"""` before and after the comment

However in certain cases it may have meaning to the interpreter, this because this kind of commenting is part of the **Docstring** system

A `Docstring` is a multi-line comment which is used at the start of a:

- Script
- Module
- Class
- Callable

When the interpreter encounters this style of commenting it can retrieve it and add it to the **Python** documentation

#### Introduction to Modules and Packages in Python

**Modules** are a simple way to re-use code

When we write a script, all the code resides in one file, but lets imagine we have a function in it that we will need to replicate in other programs over and over again

It would become hard to scale if all the time we had to copy and paste that same function

For that there is the option of script exporting, along the syntax preparation to accept such evocation

This whole idea is known as `modules`

If objects can be seen as Lego bricks, then modules can be seen as a full Lego block, since all the objects inside the same module share the same purpose.  However more complex blocks may need more than a single `module`, this is where the **Package**  comes in handy

A `package` is a set of `modules`, which all share the same purpose

The `urllib` is an example of a package with the goal of sending web requests to sites, the same way a browser would, we can specify an URL and make a request, doing this will attempt to connect to the server responsible for that URL and download the contents

When analyzing the modules that make this package we can see that all of them are in some way related to URL usage

In sum:

- Modules are meant to group code with the same purpose
- Packages are meant to group Modules with the same purpose

Lets check how the `urllib` works

	from urllib.request import urlopen
	response = urlopen("https://example.com")
	if response.status == 200:
		response = response.read()
	print(response)

Lets take a look at this code:

- We start out by importing the `urlopen` function from the `urllib.request`module
- Then we specify the parameter we want to request, in this case "https://example.com"
- In this case if the connection is successful, which is bind to the code 200 (404 for page not found) 
- If the response was successful, we will call the results with the `response.read()` function
- After this we will `print` the results of the page

#### Exploring Modules and Packages

Understanding the concept of modules is important since this concept is baked inside Python's runtime

**Creating a Module**

A module is a piece of Python code with a `.py` extension

Lets imagine we are creating a game of cards, *Solitaire* and *BlackJack*, both of these will use the same card deck

So, in order for us not having to code the same deck 2x we can simply create a file with the code inside, this way we created a `module`

**The module is named after the file where the code is written, minus the extension**

In the new file where we want to use the previous created module and its contents, in this case the `card deck` we start by specifying the `module` from which we want to import an object followed by the `function`

In this case:

	from cards import deck

**Creating a Package**

To create a `package` we start by creating a folder and inside it a file with the name `__init__.py`

The existence of this folder tells the runtime it is dealing with a package and the, the runtime uses the folder name as the package name

**Importing a Module**

When a module resides inside of a package we need to specify the name of the `module` and the name of the `package` 

Python uses a `.` to separate these packages and modules

Lets check an example:

	from urllib.request import urlopen

This line tells the interpreter to look for a package`urllib` with a module `request` and import the `urlopen` function 

The interpreter finds these packages and their modules due to a setting named path, which specifies the folders where packages and modules reside

By default the path is set to the folder which contains Python's standard library

This path setting can be set to identify more folders

To help developers better understand what objects are bound to a given module we can use the built in function named `dir()` this function accepts an object as input and will display all the names that are bound to that object 

Using the `dir()` function, enables us to see all the objects bound to a module

For example:

	import cards
	print(dir(dir(cards)))

The answer is:

	["card", "deck"]


#### A tour of the `standard lib

Starting out we will check how we can see all the modules inside the `standard lib`

To do we can  use the `help()` function. By passing a `sys` into the help function we can see documentation of the module

As such

	help(sys)

Using the interpreter is another way to get information about the standard library

**`sys` Module**

The `sys` module provides access to variables used or maintained by the interpreter and to functions that interact with the interpreter

The name variable refers to name bindings, providing access to objects and functions used to interact with the Python runtime

`sys` provides us access to the runtime itself, it includes info such as the OS and where the code is running, it also includes the path biding which is used to define directories containing models as well as the `exit` function which will make the runtime shutdown

The reason for this module is to provide a way to interact with the interpreter

**`os` Module**

The `os` module is used to interact with the OS

It is used for tasks such as creating and moving files and directories sending commands to the shell, checking how many CPU's are available and other OS related tasks

**`math` Module**

This module includes all the math related functions, from powers to roots and arithmetic formulas

**`collections` Module**

Python already includes several object types, such as:

- lists
- sets
- dictionaries
- tuples

These are all so common that are available to our code without the need to import a module

**`random` Module**

This provides access to functions which can create:

- Random numbers;
- Shuffle objects in a list;
- Create semi-randomness;

#### Introduction to Comprehensions in Python

Comprehension is the syntax we have to follow when invoking the objects present in **Python's** runtime, such as:

- Dictionary
- Set
- List
- Tuple

The style of the syntax is referred to as comprehensions 

**Lists

We have 2 ways to interact with them:

- We can create an empty list and from there add info to it
- We can create a list and provide all the needed info right away

As such:

Lets take a look at the first example:

	people_to_know = ["lovelace", "curry", "tesla", "sagan"]
	revised_people = []
	for person in people_to_know:
		revised_people.append(person.title())
	print(revised_people)

The result will be:

	["Lovelace", "Curry", "Tesla", "Sagan"]

What we did was:

- Creating a list of people
- Create an empty list
- `for` loop iterating through all the objects `person` in the list of people 
- Inside this `for` loop we will pick each object and use `append` function to transfer the results to  the new empty list as well as capitalizing the 1st letter by using the `title` function
- From here we `print` the newly created list

Since lists maintain a sense of order the newly created list maintains the order

Now lets see list comprehension in action:

	people_to_know = ["lovelace", "curry", "tesla", "sagan"]
	people_to_know = [person.title() for person in people_to_know]
	print(people_to_know)

The result will be:

	["Lovelace", "Curry", "Tesla", "Sagan"]

List comprehension is used to achieve the same result in less and more consistent lines of code, these live inside a pair of square brackets []

The first component of this syntax is the object that we want to include in the new list, in this case `person` followed by the `title` function and from here we bind this same object to the list:

	[person.title() for person in people_to_know]

The result will be:

	["Lovelace", "Curry", "Tesla", "Sagan"]

As we can see we went from 3 lines to a single line of code

We can also remove objects from a list, by adding the `split()` function, as such:

	people_to_know = ["lovelace", "curry", "tesla", "sagan"]
	[person.title() for person in people_to_know if person in 'curry sagan'.split()]

The result will be:

	["Curry", "Sagan"]

Comprehensions can also be nested by looping through multiple lists, as such:

	number = ["1", "2", "3", "4"]
	letter = ["A", "B", "C", "D"]
	list = [f'{l}{n}' for n in number for l in letter]
	print(cards)

The result will be:

	["A1", "A2", "A3", "A4", "B1", "B2", "B3", "B4", "C1", "C2", "C3", "C4", "D1", "D2", "D3", "D4"]

The downside of comprehensions is that they can make the code less readable when they become too complex

**Dictionaries**

Lets imagine we have a dictionary, with `key - value` objects. This dictionary contains an a number of players and their score on a game, along with this we want to add a bonus from a level completion

Note that `dictionaries` start with `{}`

	player_scores = { "player1": 2_000, "player2": 3_000, "player3": 4_0000, "player4": 5_000 } 
	player_scores = {palyer: score + 10_000 for (player, score) in player_scores.items()}
 
 When we call the `player_scores` dictionary we get:

	 { "player1": 12_000, "palyer2": 13_000, "player3": 14_0000, "player4": 15_000 } 

What we did was:

- Providing 2 values `player` and `score`
- Through a `for` loop `(player, score)` we bind them together

**Set**

Lets imagine we have a set of people, and we need to remove all the duplicates, while turning their names in title case, this is where `set` comes in handy

	people_to_know = ["lovelace", "curry", "tesla", "sagan", "curry", "tesla"]
	people_to_know = { person.title() for person in people_to_know }

When we invoke `people_to_now` we get:

	["Lovelace", "Curry", "Tesla", "Sagan"]

#### Intro to Exceptions

Sometimes the code we write spits back an error, there are many ways how **Python handles errors**

For example, the syntax may be wrong, for example we forgot a `:` it becomes impossible for the interpreter to validate this code, the same way that if we ask it to open a file that does not exist the result will be the same

- The first case we have a syntax error, and its the most common
- When the second scenario takes place it happens the interpreter raises an exception (since these are exceptions to the normal code flow)

When syntax errors are spitted the interpreter tells us where the error is coming from, yet this is not fully accurate at times, for that we should confirm around the provided place 

Exceptions are **Python models** containing usually details about the reason for the exception, including line numbers, error messages 

There are different types of error objects, for example `file not found error`

**Try Family of Keywords**

This family includes:

- `try`
- `except`
- `finally`

- Try: When is used when we want to run code that we know might raise an exception. 

- Except: This tell the runtime that in case such issue appears in the code block above, we should run `except` code block

- Finally: This tells the runtime to run this no matter if an exception was raised or not

Lets check the present code:

	try:
		number = open("number.txt").readline()
		number = int(number) # convert to int from str 
		number = number / number
	except FileNotFoundError:
		print("Cannot locate number.txt")
	except ValueError:
		print("Cannot convert str to int")
	except ZeroDivisionError:
		print("Cannot Divide by 0")
	finally:
		print("Always run")

What we did here was 

- Telling the machine to `try` to open a a file and fetch a number from a line
- Convert it into `int` so arithmetic functions can be applied
- Divide it by itself
- Unless file is not found
- Unless this cant be converted (imagine in the file/line there is a letter)
- Unless it is a 0
- In the end we print `"Always run"` not sure why

**`err`**

We have a keyword to specify when an error is encountered in such situations

	try:
		number = open("number.txt").readline()
	except FileNotFindError as err:
		print(f'"Cannot read {err.filename}")
	finally:
		print("Always run")

This `err` allow us to bind the file name to the error, making it possible to display it

