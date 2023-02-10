# Module

## JavaScript Modules
## JavaScript modules allow you to break up your code into separate files.

# This makes it easier to maintain a code-base.

# Modules are imported from external files with the import statement.

# Modules also rely on type="module" in the <script> tag.

# In JavaScript, we use the import and export keywords to share and receive functionalities respectively across different modules.
- The export keyword is used to make a variable, function, class or object  accessible to other modules. In other words, it becomes a public code.
- The import keyword is used to bring in public code from another module.

Let's look at a simple example of this:
- 
![](/images/1.PNG)

# This module has three functions defined in it:

- getPower: This function gets the power of a number
- capitalize: This function capitalizes the first letter in a word
- roundToDecimalPlace: This function rounds a given number to a specified number of decimal places.

# At the end of the file, you can see that two of the three functions were exported. In other words, they became public functions which could be used by any other script.

# To export two functions out of the three, you use the export keyword, followed by an object containing the functions you want to make accessible. Once you do this, the functions can be accessed by any program within that codebase which require them.

Let's take a look at how we can use them:
![](/images/2.PNG)

# The displayTotal.js module does not have capitalize() and roundToDecimalPlace() but wants to use the capitalize and round-to-decimal-place functionality. So how did we bring it in? With import!
# We did this by using the import keyword followed by the name of the functions we want to import from the module, which in our case are capitalize and roundToDecimalPlace.
# What if you only wanted to import the capitalize function into your program?
Simple – import only capitalize(), like so:
![](/images/3.PNG)

# N/B: Understanding how file structuring works is very important when working with modules. In the above example, we are simply importing from a file which exists in the same directory, which is why we use the notation './import'.


# Default Exports
# If you want to export all three functions but intend to make one of them a default (perhaps because you are most likely to use that single function), you simply use the default keyword.

# The default keyword makes importing a function easier. Let's consider the following example:
![](/images/4.PNG)

# As you can see, we have made capitalize our default function. This essentially means we have given it some sort of privilege.
# Say we want to import the capitalize function from the module into another program. The syntax for that will be very similar, except you don't have to import the function into curly braces:
![](/images/5.PNG)
# If you want to import the default function along with any other functions, you mix the bare 'default' function with other functions in curly braces:
![](/images/6.PNG)