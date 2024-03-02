   dcmarkdown API documentation     :root{--highlight-color:#fe9}.flex{display:flex !important}body{line-height:1.5em}#content{padding:20px}#sidebar{padding:30px;overflow:hidden}#sidebar > \*:last-child{margin-bottom:2cm}.http-server-breadcrumbs{font-size:130%;margin:0 0 15px 0}#footer{font-size:.75em;padding:5px 30px;border-top:1px solid #ddd;text-align:right}#footer p{margin:0 0 0 1em;display:inline-block}#footer p:last-child{margin-right:30px}h1,h2,h3,h4,h5{font-weight:300}h1{font-size:2.5em;line-height:1.1em}h2{font-size:1.75em;margin:1em 0 .50em 0}h3{font-size:1.4em;margin:25px 0 10px 0}h4{margin:0;font-size:105%}h1:target,h2:target,h3:target,h4:target,h5:target,h6:target{background:var(--highlight-color);padding:.2em 0}a{color:#058;text-decoration:none;transition:color .3s ease-in-out}a:hover{color:#e82}.title code{font-weight:bold}h2\[id^="header-"\]{margin-top:2em}.ident{color:#900}pre code{background:#f8f8f8;font-size:.8em;line-height:1.4em}code{background:#f2f2f1;padding:1px 4px;overflow-wrap:break-word}h1 code{background:transparent}pre{background:#f8f8f8;border:0;border-top:1px solid #ccc;border-bottom:1px solid #ccc;margin:1em 0;padding:1ex}#http-server-module-list{display:flex;flex-flow:column}#http-server-module-list div{display:flex}#http-server-module-list dt{min-width:10%}#http-server-module-list p{margin-top:0}.toc ul,#index{list-style-type:none;margin:0;padding:0}#index code{background:transparent}#index h3{border-bottom:1px solid #ddd}#index ul{padding:0}#index h4{margin-top:.6em;font-weight:bold}@media (min-width:200ex){#index .two-column{column-count:2}}@media (min-width:300ex){#index .two-column{column-count:3}}dl{margin-bottom:2em}dl dl:last-child{margin-bottom:4em}dd{margin:0 0 1em 3em}#header-classes + dl > dd{margin-bottom:3em}dd dd{margin-left:2em}dd p{margin:10px 0}.name{background:#eee;font-weight:bold;font-size:.85em;padding:5px 10px;display:inline-block;min-width:40%}.name:hover{background:#e0e0e0}dt:target .name{background:var(--highlight-color)}.name > span:first-child{white-space:nowrap}.name.class > span:nth-child(2){margin-left:.4em}.inherited{color:#999;border-left:5px solid #eee;padding-left:1em}.inheritance em{font-style:normal;font-weight:bold}.desc h2{font-weight:400;font-size:1.25em}.desc h3{font-size:1em}.desc dt code{background:inherit}.source summary,.git-link-div{color:#666;text-align:right;font-weight:400;font-size:.8em;text-transform:uppercase}.source summary > \*{white-space:nowrap;cursor:pointer}.git-link{color:inherit;margin-left:1em}.source pre{max-height:500px;overflow:auto;margin:0}.source pre code{font-size:12px;overflow:visible}.hlist{list-style:none}.hlist li{display:inline}.hlist li:after{content:',\\2002'}.hlist li:last-child:after{content:none}.hlist .hlist{display:inline;padding-left:1em}img{max-width:100%}td{padding:0 .5em}.admonition{padding:.1em .5em;margin-bottom:1em}.admonition-title{font-weight:bold}.admonition.note,.admonition.info,.admonition.important{background:#aef}.admonition.todo,.admonition.versionadded,.admonition.tip,.admonition.hint{background:#dfd}.admonition.warning,.admonition.versionchanged,.admonition.deprecated{background:#fd4}.admonition.error,.admonition.danger,.admonition.caution{background:lightpink} @media screen and (min-width:700px){#sidebar{width:30%;height:100vh;overflow:auto;position:sticky;top:0}#content{width:70%;max-width:100ch;padding:3em 4em;border-left:1px solid #ddd}pre code{font-size:1em}.item .name{font-size:1em}main{display:flex;flex-direction:row-reverse;justify-content:flex-end}.toc ul ul,#index ul{padding-left:1.5em}.toc > ul > li{margin-top:.5em}} @media print{#sidebar h1{page-break-before:always}.source{display:none}}@media print{\*{background:transparent !important;color:#000 !important;box-shadow:none !important;text-shadow:none !important}a\[href\]:after{content:" (" attr(href) ")";font-size:90%}a\[href\]\[title\]:after{content:none}abbr\[title\]:after{content:" (" attr(title) ")"}.ir a:after,a\[href^="javascript:"\]:after,a\[href^="#"\]:after{content:""}pre,blockquote{border:1px solid #999;page-break-inside:avoid}thead{display:table-header-group}tr,img{page-break-inside:avoid}img{max-width:100% !important}@page{margin:0.5cm}p,h2,h3{orphans:3;widows:3}h1,h2,h3,h4,h5,h6{page-break-after:avoid}} window.addEventListener('DOMContentLoaded', () => hljs.initHighlighting())

Module `dcmarkdown`
===================

Expand source code

    NOT_FOUND = "❌ Not Found"
    
    def underline(text:str)->str:
        """
        Returns a string with an underlined version of the input text.
    
        Parameters:
            - text (str): The text to be underlined.
    
        Returns:
            A string with the underlined version of the input text.
        """
        return f"__{text}__"
    
    def italics(text:str)->str:
        """
        Returns a string with an italicized version of the input text.
    
        Parameters:
            - text (str): The text to be italicized.
    
        Returns:
            A string with the italicized version of the input text.
        """
        return f"*{text}*"
    
    def bold(text: str) -> str:
        """
        Returns a string with a bold version of the input text.
    
        Parameters:
            - text (str): The text to be made bold.
    
        Returns:
            A string with the bold version of the input text.
        """
        return f"**{text}**"
    
    def strikethrough(text: str) -> str:
        """
        Returns a string with a strikethrough version of the input text.
    
        Parameters:
            - text (str): The text to be given a strikethrough.
    
        Returns:
            A string with the strikethrough version of the input text.
        """
        return f"~~{text}~~"
    
    def inline_code(text: str) -> str:
        """
        Returns a string with an inline code block containing the input text.
    
        Parameters:
            - text (str): The text to be enclosed in the code block.
    
        Returns:
            A string with the input text enclosed in an inline code block.
        """
        return f"`{text}`"
    
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
    
    def spoiler(text: str) -> str:
        """
        Returns a string with a spoiler tag enclosing the input text.
    
        Parameters:
            - text (str): The text to be enclosed in the spoiler tag.
    
        Returns:
            A string with the input text enclosed in a spoiler tag.
        """
        return f'||{text}||'
    
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

Index
=====

*   ### [Functions](#header-functions)
    
    *   `[blockquote](#dcmarkdown.blockquote "dcmarkdown.blockquote")`
    *   `[bold](#dcmarkdown.bold "dcmarkdown.bold")`
    *   `[code_block](#dcmarkdown.code_block "dcmarkdown.code_block")`
    *   `[hyperlink](#dcmarkdown.hyperlink "dcmarkdown.hyperlink")`
    *   `[inline_code](#dcmarkdown.inline_code "dcmarkdown.inline_code")`
    *   `[italics](#dcmarkdown.italics "dcmarkdown.italics")`
    *   `[quote](#dcmarkdown.quote "dcmarkdown.quote")`
    *   `[spoiler](#dcmarkdown.spoiler "dcmarkdown.spoiler")`
    *   `[strikethrough](#dcmarkdown.strikethrough "dcmarkdown.strikethrough")`
    *   `[underline](#dcmarkdown.underline "dcmarkdown.underline")`
*   ### [Classes](#header-classes)
    
    *   #### `[mention](#dcmarkdown.mention "dcmarkdown.mention")`
        
        *   `[channel](#dcmarkdown.mention.channel "dcmarkdown.mention.channel")`
        *   `[role](#dcmarkdown.mention.role "dcmarkdown.mention.role")`
        *   `[user](#dcmarkdown.mention.user "dcmarkdown.mention.user")`
    *   #### `[timestamp_popup](#dcmarkdown.timestamp_popup "dcmarkdown.timestamp_popup")`
        
        *   `[long_date](#dcmarkdown.timestamp_popup.long_date "dcmarkdown.timestamp_popup.long_date")`
        *   `[long_datetime](#dcmarkdown.timestamp_popup.long_datetime "dcmarkdown.timestamp_popup.long_datetime")`
        *   `[long_time](#dcmarkdown.timestamp_popup.long_time "dcmarkdown.timestamp_popup.long_time")`
        *   `[relative_time](#dcmarkdown.timestamp_popup.relative_time "dcmarkdown.timestamp_popup.relative_time")`
        *   `[short_date](#dcmarkdown.timestamp_popup.short_date "dcmarkdown.timestamp_popup.short_date")`
        *   `[short_datetime](#dcmarkdown.timestamp_popup.short_datetime "dcmarkdown.timestamp_popup.short_datetime")`
        *   `[short_time](#dcmarkdown.timestamp_popup.short_time "dcmarkdown.timestamp_popup.short_time")`

Generated by [pdoc 0.10.0](https://pdoc3.github.io/pdoc "pdoc: Python API documentation generator").
