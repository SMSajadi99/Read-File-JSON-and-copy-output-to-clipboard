# Tutorial-JSON
#json #dictionary 
```python
import json

with open(r"C:\Users\smsaj\Downloads\results_nusc.json") as f:
    table = json.load(f)
tokens = list(table['results'].keys())
```

To save printed output or copy it to the clipboard automatically, you can use the following steps depending on the programming language or operating system you are using:

Python:
1. Install the `pyperclip` library by running `pip install pyperclip` in your command line.
2. Import the library in your Python script using `import pyperclip`.
3. After printing the output, use `pyperclip.copy()` to copy the text to the clipboard.

Here's an example:

```python
import pyperclip

# Your code that generates the output
output = "This is the printed output."

# Print the output
print(output)

# Copy the output to clipboard
pyperclip.copy(output)
```

This code will both print the output and copy it to the clipboard using the `pyperclip` library.

Other programming languages and operating systems may have different methods for accessing and manipulating the clipboard. If you let me know which language or OS you are using, I can provide more specific instructions.
The `pyperclip` library in Python allows copying only certain data types to the clipboard, such as strings (`str`), integers (`int`), floats (`float`), and booleans (`bool`). If you're trying to copy a list to the clipboard using `pyperclip.copy()`, you'll encounter the `PyperclipException` you mentioned.

To work around this limitation, you can convert the list to a string before copying it to the clipboard. Here's an example:

```python
import pyperclip

# Your list
my_list = [1, 2, 3, 4, 5]

# Convert the list to a string
output = str(my_list)

# Print the output
print(output)

# Copy the output to clipboard
pyperclip.copy(output)
```
For input list:
```python
import pyperclip
import json

# Example list
my_list = [1, 2, 3, 4, 5]

# Convert list to JSON string and copy to clipboard
list_as_json = json.dumps(my_list)
pyperclip.copy(list_as_json)

# Retrieve JSON string from clipboard and convert back to list
json_from_clipboard = pyperclip.paste()
list_from_clipboard = json.loads(json_from_clipboard)

print(list_from_clipboard)  # Output: [1, 2, 3, 4, 5]

```
