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
