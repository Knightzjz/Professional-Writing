## whitespace

Blank symbols include spaces, blank lines, etc., where spaces are divided into half-width spaces and full-width spaces.

### Blank usage

The following guidelines are recommended for the use of blank symbols in technical documentation.

| Blank Type | Corresponding Specification |
| ---- | -------------------------------------------- ---------------- |
| Space | - Full-width spaces are prohibited, **half-width spaces are always used**. <br> - Empty half-width spaces are prohibited between Chinese characters (including Chinese characters and Chinese punctuation) and Chinese characters. <br> - **English characters and Arabic numerals** generally use half-width format, so they should be surrounded by half-width spaces, with the following exceptions: 1) When it is at the beginning of a sentence, the left space is omitted; 2) Its right side is half-width punctuation or full-width When punctuation, spaces on the right are omitted. <br> - Two or more consecutive half-width spaces are prohibited, except for indentation, list level, inherent spaces in code blocks, and spaces in Markdown tables. <br> - Tabs are deprecated to replace spaces. |
| Blank Line | - A blank line is recommended to separate different paragraphs. <br> - It is recommended to use a blank line to separate different typeset formats, such as between the title and the following text, between the text and the code block, between the text and the table, etc. <br> - Two or more consecutive blank lines are prohibited. |
| Others | Line width: It is enough to keep the same typesetting format, and you can freely choose between 80 and 120 characters. In principle, the width should not exceed 160 characters. |

### Use of Tabs and Spaces

Tab and spacebars are often used in technical documents for indentation and alignment. Since the default length of Tab may be inconsistent in different editors, setting indentation with the Tab key may lead to formatting confusion. If you use the spacebar to set the indent, opening the document with any editor will show the same alignment.

Therefore it is recommended to:

- Use the space bar instead of the tab key to indent or align.
- Using the Tab key for indentation is acceptable, but **Mixing Tab and Space** for indentation is prohibited.
- In editors such as Visual Studio Code, uniformly set a Tab equal to four half-width spaces.
