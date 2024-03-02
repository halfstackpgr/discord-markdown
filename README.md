Usage
Import the desired functions or classes into your Python code:

python
Copy code
from text_formatting_utils import underline, italics, bold, strikethrough, inline_code, code_block, quote, blockquote, spoiler, mention, timestamp_popup
Then, you can use the functions and classes as follows:

python
Copy code
text = "Hello, world!"
formatted_text = bold(text)
print(formatted_text)  # Output: **Hello, world!**
Refer to the docstrings and comments within the code for more detailed usage instructions.

Functions and Classes
underline(text: str) -> str: Adds underline formatting to the input text.
italics(text: str) -> str: Adds italics formatting to the input text.
bold(text: str) -> str: Adds bold formatting to the input text.
strikethrough(text: str) -> str: Adds strikethrough formatting to the input text.
inline_code(text: str) -> str: Encloses the input text in an inline code block.
code_block(text: str, language: str = "") -> str: Encloses the input text in a code block with optional language highlighting.
quote(text: str, author: str = "") -> str: Formats the input text as a quote, with optional author attribution.
blockquote(text: str) -> str: Formats the input text as a blockquote.
spoiler(text: str) -> str: Encloses the input text in a spoiler tag.
mention: A class containing methods for formatting user, role, and channel mentions.
timestamp_popup: A class for generating Discord timestamp strings based on a Unix timestamp.
License
This project is licensed under the MIT License. See the LICENSE file for details.