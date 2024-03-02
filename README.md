Module `dcmarkdown`
===================

Functions
---------

`def blockquote(text: str) ‑> str`

Returns a string with a blockquote of the input text.

Parameters
----------

*   text (str): The text to be quoted.

Returns
-------

A string with the input text formatted as a blockquote.

Expand source code

    def blockquote(text: str) -> str:
        """
        Returns a string with a blockquote of the input text.
    
        Parameters:
            - text (str): The text to be quoted.
    
        Returns:
            A string with the input text formatted as a blockquote.
        """
        lines = text.split('\n')
        quoted_lines = [f'> {line}\n' for line in lines]
        return ''.join(quoted_lines)

`def bold(text: str) ‑> str`

Returns a string with a bold version of the input text.

Parameters
----------

*   text (str): The text to be made bold.

Returns
-------

A string with the bold version of the input text.

Expand source code

    def bold(text: str) -> str:
        """
        Returns a string with a bold version of the input text.
    
        Parameters:
            - text (str): The text to be made bold.
    
        Returns:
            A string with the bold version of the input text.
        """
        return f"**{text}**"

`def code_block(text: str, language: str = '') ‑> str`

Returns a string with a code block containing the input text.

Parameters
----------

*   text (str): The text to be enclosed in the code block.
*   language (str): The programming language used in the code block (optional).

Returns
-------

A string with the input text enclosed in a code block, with optional language highlighting.

Expand source code

    def code_block(text: str, language: str = "") -> str:
        """
        Returns a string with a code block containing the input text.
    
        Parameters:
            - text (str): The text to be enclosed in the code block.
            - language (str): The programming language used in the code block (optional).
    
        Returns:
            A string with the input text enclosed in a code block, with optional language highlighting.
        """
        if language:
            return f"```{language}\n{text}\n```"
        else:
            return f"```\n{text}\n```"

`def hyperlink(url: str, alt_text: str = '') ‑> str`

Formats a hyperlink with the specified URL and alternate text.

Parameters
----------

*   url (str): The URL for the hyperlink.
*   alt\_text (str): Optional alternate text for the hyperlink.

Returns
-------

A string with the formatted hyperlink.

Expand source code

    def hyperlink(url: str, alt_text: str = '') -> str:
        """
        Formats a hyperlink with the specified URL and alternate text.
    
        Parameters:
            - url (str): The URL for the hyperlink.
            - alt_text (str): Optional alternate text for the hyperlink.
    
        Returns:
            A string with the formatted hyperlink.
        """
        return f'[{alt_text}]({url})'

`def inline_code(text: str) ‑> str`

Returns a string with an inline code block containing the input text.

Parameters
----------

*   text (str): The text to be enclosed in the code block.

Returns
-------

A string with the input text enclosed in an inline code block.

Expand source code

    def inline_code(text: str) -> str:
        """
        Returns a string with an inline code block containing the input text.
    
        Parameters:
            - text (str): The text to be enclosed in the code block.
    
        Returns:
            A string with the input text enclosed in an inline code block.
        """
        return f"`{text}`"

`def italics(text: str) ‑> str`

Returns a string with an italicized version of the input text.

Parameters
----------

*   text (str): The text to be italicized.

Returns
-------

A string with the italicized version of the input text.

Expand source code

    def italics(text:str)->str:
        """
        Returns a string with an italicized version of the input text.
    
        Parameters:
            - text (str): The text to be italicized.
    
        Returns:
            A string with the italicized version of the input text.
        """
        return f"*{text}*"

`def quote(text: str, author: str = '') ‑> str`

Returns a string with a formatted quote of the input text.

Parameters
----------

*   text (str): The text to be quoted.
*   author (str): The author of the quote (optional).

Returns
-------

A string with the input text formatted as a quote, with optional author attribution.

Expand source code

    def quote(text: str, author: str = "") -> str:
        """
        Returns a string with a formatted quote of the input text.
    
        Parameters:
            - text (str): The text to be quoted.
            - author (str): The author of the quote (optional).
    
        Returns:
            A string with the input text formatted as a quote, with optional author attribution.
        """
        if author:
            return f"> {text}\n> - {author}"
        else:
            return f"> {text}"

`def spoiler(text: str) ‑> str`

Returns a string with a spoiler tag enclosing the input text.

Parameters
----------

*   text (str): The text to be enclosed in the spoiler tag.

Returns
-------

A string with the input text enclosed in a spoiler tag.

Expand source code

    def spoiler(text: str) -> str:
        """
        Returns a string with a spoiler tag enclosing the input text.
    
        Parameters:
            - text (str): The text to be enclosed in the spoiler tag.
    
        Returns:
            A string with the input text enclosed in a spoiler tag.
        """
        return f'||{text}||'

`def strikethrough(text: str) ‑> str`

Returns a string with a strikethrough version of the input text.

Parameters
----------

*   text (str): The text to be given a strikethrough.

Returns
-------

A string with the strikethrough version of the input text.

Expand source code

    def strikethrough(text: str) -> str:
        """
        Returns a string with a strikethrough version of the input text.
    
        Parameters:
            - text (str): The text to be given a strikethrough.
    
        Returns:
            A string with the strikethrough version of the input text.
        """
        return f"~~{text}~~"

`def underline(text: str) ‑> str`

Returns a string with an underlined version of the input text.

Parameters
----------

*   text (str): The text to be underlined.

Returns
-------

A string with the underlined version of the input text.

Expand source code

    def underline(text:str)->str:
        """
        Returns a string with an underlined version of the input text.
    
        Parameters:
            - text (str): The text to be underlined.
    
        Returns:
            A string with the underlined version of the input text.
        """
        return f"__{text}__"

Classes
-------

`class mention`

A class that contains methods for formatting user, role, and channel mentions.

Expand source code

    class mention:
        """
        A class that contains methods for formatting user, role, and channel mentions.
        """
        def user(self, user_id) -> str:
            """
            Returns a string with a user mention given a user ID.
    
            Parameters:
                - user_id (int): The user ID to be mentioned.
    
            Returns:
                A string with the user mention.
            """
            if user_id == 0:
                return NOT_FOUND
            return f'<@{user_id}>'
        def role(self, role_id) -> str:
            """
            Returns a string with a role mention given a role ID.
    
            Parameters:
                - role_id (int): The role ID to be mentioned.
    
            Returns:
                A string with the role mention.
            """
            if role_id == 0:
                return NOT_FOUND
            return f'<@&{str(role_id)}>'
        def channel(self, channel_id) -> str:
            """
            Returns a string with a channel mention given a channel ID.
    
            Parameters:
                - channel_id (int): The channel ID to be mentioned.
    
            Returns:
                A string with the channel mention.
            """
            if channel_id == 0:
                return NOT_FOUND
            return f'<#{channel_id}>'

### Methods

`def channel(self, channel_id) ‑> str`

Returns a string with a channel mention given a channel ID.

Parameters
----------

*   channel\_id (int): The channel ID to be mentioned.

Returns
-------

A string with the channel mention.

Expand source code

    def channel(self, channel_id) -> str:
        """
        Returns a string with a channel mention given a channel ID.
    
        Parameters:
            - channel_id (int): The channel ID to be mentioned.
    
        Returns:
            A string with the channel mention.
        """
        if channel_id == 0:
            return NOT_FOUND
        return f'<#{channel_id}>'

`def role(self, role_id) ‑> str`

Returns a string with a role mention given a role ID.

Parameters
----------

*   role\_id (int): The role ID to be mentioned.

Returns
-------

A string with the role mention.

Expand source code

    def role(self, role_id) -> str:
        """
        Returns a string with a role mention given a role ID.
    
        Parameters:
            - role_id (int): The role ID to be mentioned.
    
        Returns:
            A string with the role mention.
        """
        if role_id == 0:
            return NOT_FOUND
        return f'<@&{str(role_id)}>'

`def user(self, user_id) ‑> str`

Returns a string with a user mention given a user ID.

Parameters
----------

*   user\_id (int): The user ID to be mentioned.

Returns
-------

A string with the user mention.

Expand source code

    def user(self, user_id) -> str:
        """
        Returns a string with a user mention given a user ID.
    
        Parameters:
            - user_id (int): The user ID to be mentioned.
    
        Returns:
            A string with the user mention.
        """
        if user_id == 0:
            return NOT_FOUND
        return f'<@{user_id}>'

`class timestamp_popup (timestamp: int)`

A class that generates Discord timestamp strings based on a Unix timestamp.

Parameters:
-----------

timestamp: int A Unix timestamp representing the time in seconds since the Unix epoch (January 1, 1970).

Attributes:
-----------

timestamp: int A Unix timestamp representing the time in seconds since the Unix epoch (January 1, 1970).

Methods:
--------

short\_time() -> str: Returns a string representing the short time format of the timestamp in Discord's format. Example: ""

long\_time() -> str: Returns a string representing the long time format of the timestamp in Discord's format. Example: ""

short\_date() -> str: Returns a string representing the short date format of the timestamp in Discord's format. Example: ""

long\_date() -> str: Returns a string representing the long date format of the timestamp in Discord's format. Example: ""

short\_datetime() -> str: Returns a string representing the short date and time format of the timestamp in Discord's format. Example: ""

long\_datetime() -> str: Returns a string representing the long date and time format of the timestamp in Discord's format. Example: ""

relative\_time() -> str: Returns a string representing the relative time format of the timestamp in Discord's format. Example: ""

Expand source code

    class timestamp_popup:
        """
        A class that generates Discord timestamp strings based on a Unix timestamp.
    
        Parameters:
        -----------
        timestamp: int
            A Unix timestamp representing the time in seconds since the Unix epoch (January 1, 1970).
    
        Attributes:
        -----------
        timestamp: int
            A Unix timestamp representing the time in seconds since the Unix epoch (January 1, 1970).
    
        Methods:
        --------
        short_time() -> str:
            Returns a string representing the short time format of the timestamp in Discord's format.
            Example: "<t:1613075120:t>"
    
        long_time() -> str:
            Returns a string representing the long time format of the timestamp in Discord's format.
            Example: "<t:1613075120:T>"
    
        short_date() -> str:
            Returns a string representing the short date format of the timestamp in Discord's format.
            Example: "<t:1613075120:d>"
    
        long_date() -> str:
            Returns a string representing the long date format of the timestamp in Discord's format.
            Example: "<t:1613075120:D>"
    
        short_datetime() -> str:
            Returns a string representing the short date and time format of the timestamp in Discord's format.
            Example: "<t:1613075120:f>"
    
        long_datetime() -> str:
            Returns a string representing the long date and time format of the timestamp in Discord's format.
            Example: "<t:1613075120:F>"
    
        relative_time() -> str:
            Returns a string representing the relative time format of the timestamp in Discord's format.
            Example: "<t:1613075120:R>"
        """
        def __init__(self, timestamp: int):
            self.timestamp = timestamp
        def __repr__(self):
            """
            Returns the Unix timestamp value as a string.
    
            Returns:
            --------
            str:
                A string representing the Unix timestamp value.
            """
            return str(self.timestamp)
        def short_time(self) -> str:
            """
            Returns a string representing the short time format of the timestamp in Discord's format.
            Example: "<t:1613075120:t>"
    
            Returns:
            --------
            str:
                A string representing the short time format of the timestamp.
            """
            return f'<t:{self.timestamp}:t>'
        
        def long_time(self) -> str:
            """
            Returns a string representing the long time format of the timestamp in Discord's format.
            Example: "<t:1613075120:T>"
    
            Returns:
            --------
            str:
                A string representing the long time format of the timestamp.
            """
            return f'<t:{self.timestamp}:T>'
        def short_date(self) -> str:
            """
            Returns a string representing the short date format of the timestamp in Discord's format.
            Example: "<t:1613075120:d>"
    
            Returns:
            --------
            str:
                A string representing the short date format of the timestamp.
            """
            return f'<t:{self.timestamp}:d>'
        def long_date(self) -> str:
            """
            Returns a string representing the long date format of the timestamp in Discord's format.
            Example: "<t:1613075120:D>"
    
            Returns:
            --------
            str:
                A string representing the long date format of the timestamp.
            """
            return f'<t:{self.timestamp}:D>'
        def short_datetime(self) -> str:
            """
            Returns a string representing the short date and time format of the timestamp in Discord's format.
            Example: "<t:1613075120:f>"
            Returns:
            --------
            str:
                A string representing the short date and time format of the timestamp.
            """
            return f'<t:{self.timestamp}:f>'
        def long_datetime(self) -> str:
            """
            Returns a string representing the long date and time format of the timestamp in Discord's format.
            Example: "<t:1613075120:F>"
    
            Returns:
            --------
            str:
                A string representing the long date and time format of the timestamp.
            """
            return f'<t:{self.timestamp}:F>'
        def relative_time(self) -> str:
            """
            Returns a string representing the relative time format of the timestamp in Discord's format.
            Example: "<t:1613075120:R>"
    
            Returns:
            --------
            str:
                A string representing the relative time format of the timestamp.
            """
            return f'<t:{self.timestamp}:R>'

### Methods

`def long_date(self) ‑> str`

Returns a string representing the long date format of the timestamp in Discord's format. Example: ""

Returns:
--------

str: A string representing the long date format of the timestamp.

Expand source code

    def long_date(self) -> str:
        """
        Returns a string representing the long date format of the timestamp in Discord's format.
        Example: "<t:1613075120:D>"
    
        Returns:
        --------
        str:
            A string representing the long date format of the timestamp.
        """
        return f'<t:{self.timestamp}:D>'

`def long_datetime(self) ‑> str`

Returns a string representing the long date and time format of the timestamp in Discord's format. Example: ""

Returns:
--------

str: A string representing the long date and time format of the timestamp.

Expand source code

    def long_datetime(self) -> str:
        """
        Returns a string representing the long date and time format of the timestamp in Discord's format.
        Example: "<t:1613075120:F>"
    
        Returns:
        --------
        str:
            A string representing the long date and time format of the timestamp.
        """
        return f'<t:{self.timestamp}:F>'

`def long_time(self) ‑> str`

Returns a string representing the long time format of the timestamp in Discord's format. Example: ""

Returns:
--------

str: A string representing the long time format of the timestamp.

Expand source code

    def long_time(self) -> str:
        """
        Returns a string representing the long time format of the timestamp in Discord's format.
        Example: "<t:1613075120:T>"
    
        Returns:
        --------
        str:
            A string representing the long time format of the timestamp.
        """
        return f'<t:{self.timestamp}:T>'

`def relative_time(self) ‑> str`

Returns a string representing the relative time format of the timestamp in Discord's format. Example: ""

Returns:
--------

str: A string representing the relative time format of the timestamp.

Expand source code

    def relative_time(self) -> str:
        """
        Returns a string representing the relative time format of the timestamp in Discord's format.
        Example: "<t:1613075120:R>"
    
        Returns:
        --------
        str:
            A string representing the relative time format of the timestamp.
        """
        return f'<t:{self.timestamp}:R>'

`def short_date(self) ‑> str`

Returns a string representing the short date format of the timestamp in Discord's format. Example: ""

Returns:
--------

str: A string representing the short date format of the timestamp.

Expand source code

    def short_date(self) -> str:
        """
        Returns a string representing the short date format of the timestamp in Discord's format.
        Example: "<t:1613075120:d>"
    
        Returns:
        --------
        str:
            A string representing the short date format of the timestamp.
        """
        return f'<t:{self.timestamp}:d>'

`def short_datetime(self) ‑> str`

Returns a string representing the short date and time format of the timestamp in Discord's format. Example: "" Returns:

* * *

str: A string representing the short date and time format of the timestamp.

Expand source code

    def short_datetime(self) -> str:
        """
        Returns a string representing the short date and time format of the timestamp in Discord's format.
        Example: "<t:1613075120:f>"
        Returns:
        --------
        str:
            A string representing the short date and time format of the timestamp.
        """
        return f'<t:{self.timestamp}:f>'

`def short_time(self) ‑> str`

Returns a string representing the short time format of the timestamp in Discord's format. Example: ""

Returns:
--------

str: A string representing the short time format of the timestamp.

Expand source code

    def short_time(self) -> str:
        """
        Returns a string representing the short time format of the timestamp in Discord's format.
        Example: "<t:1613075120:t>"
    
        Returns:
        --------
        str:
            A string representing the short time format of the timestamp.
        """
        return f'<t:{self.timestamp}:t>'
