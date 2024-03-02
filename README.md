# Text Formatting Utilities

A collection of Python functions and classes for formatting text with various styles and features.

## Introduction

This repository contains a set of utility functions and a class aimed at simplifying text formatting tasks in Python applications. These functions and classes can be used to apply formatting styles such as bold, italic, underline, strikethrough, code blocks, quotes, and more to strings of text.

## Functions

### `underline(text: str) -> str`

Returns a string with an underlined version of the input text.

### `italics(text: str) -> str`

Returns a string with an italicized version of the input text.

### `bold(text: str) -> str`

Returns a string with a bold version of the input text.

### `strikethrough(text: str) -> str`

Returns a string with a strikethrough version of the input text.

### `inline_code(text: str) -> str`

Returns a string with an inline code block containing the input text.

### `code_block(text: str, language: str = "") -> str`

Returns a string with a code block containing the input text.

### `quote(text: str, author: str = "") -> str`

Returns a string with a formatted quote of the input text.

### `blockquote(text: str) -> str`

Returns a string with a blockquote of the input text.

### `spoiler(text: str) -> str`

Returns a string with a spoiler tag enclosing the input text.

## Classes

### `mention`

A class that contains methods for formatting user, role, and channel mentions.

#### `mention.user(user_id: int) -> str`

Returns a string with a user mention given a user ID.

#### `mention.role(role_id: int) -> str`

Returns a string with a role mention given a role ID.

#### `mention.channel(channel_id: int) -> str`

Returns a string with a channel mention given a channel ID.

### `timestamp_popup`

A class that generates Discord timestamp strings based on a Unix timestamp.

#### `timestamp_popup.short_time() -> str`

Returns a string representing the short time format of the timestamp in Discord's format.

#### `timestamp_popup.long_time() -> str`

Returns a string representing the long time format of the timestamp in Discord's format.

#### `timestamp_popup.short_date() -> str`

Returns a string representing the short date format of the timestamp in Discord's format.

#### `timestamp_popup.long_date() -> str`

Returns a string representing the long date format of the timestamp in Discord's format.

#### `timestamp_popup.short_datetime() -> str`

Returns a string representing the short date and time format of the timestamp in Discord's format.

#### `timestamp_popup.long_datetime() -> str`

Returns a string representing the long date and time format of the timestamp in Discord's format.

#### `timestamp_popup.relative_time() -> str`

Returns a string representing the relative time format of the timestamp in Discord's format.

## Usage

To use these functions and classes in your Python project, simply import them into your code:

```python
from text_formatting_utils import underline, italics, bold, strikethrough, inline_code, code_block, quote, blockquote, spoiler, mention, timestamp_popup
#   d i s c o r d - m a r k d o w n  
 