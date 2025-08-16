# Representing Text in Python: Strings

In Python, direct words typed into the `REPL`  without proper syntax will result in an error. To represent text, Python uses strings. A string is created by enclosing the desired characters within either:

- **Double quotes:** "Hello World"
- **Single quotes:** 'Hello World'
## String Concatenation

Strings can be combined to form a new, longer string using the `+ (plus)` symbol. This operation is known as string concatenation, which effectively "smashes" the strings together. 

Attempting to create a multi-line string by simply hitting Enter within single or double quotes will cause an error, as Python interprets the Enter key as the end of the statement. To create a string that spans multiple lines, triple quotes must be used. 

>[!NOTE]
>When a multi-line string is initiated with triple quotes in the REPL and Enter is pressed, the prompt changes from >>> to .... This indicates that Python is expecting more input to complete the multi-line string. Users can continue typing lines of text and pressing Enter. The multi-line string is concluded by typing three more matching triple quotes.

Strings are fundamental in Python programming and are widely used for:

- Displaying text to users.    
- Storing textual data in files.
- Performing text-based queries or analysis.
- Sending text data between different processes within a computer or over a network.

Given their versatility, strings are an essential component of virtually all Python programs.