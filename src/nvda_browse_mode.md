# Browse Mode

Complex read-only documents such as web pages are browsed in NVDA using browse mode.
This includes documents in the following applications:

- Mozilla Firefox
- Microsoft Internet Explorer
- Mozilla Thunderbird
- HTML messages in Microsoft Outlook
- Google Chrome
- Microsoft Edge
- Adobe Reader
- Foxit Reader
- Supported books in Amazon Kindle for PC

Browse mode is also optionally available for Microsoft Word documents.

In browse mode, the content of the document is made available in a flat representation that can be navigated with the cursor keys as if it were a normal text document.
All of NVDA's [system caret](#SystemCaret "system caret") key commands will work in this mode; e.g. say all, report formatting, table navigation commands, etc.
When [Visual Highlight](#VisionFocusHighlight "Visual Highlight") is enabled, the location of the virtual browse mode caret is also exposed visually.
Information such as whether text is a link, heading, etc. is reported along with the text as you move.

Sometimes, you will need to interact directly with controls in these documents.
For example, you will need to do this for editable text fields and lists so that you can type characters and use the cursor keys to work with the control.
You do this by switching to focus mode, where almost all keys are passed to the control.
When in Browse mode, by default, NVDA will automatically switch to focus mode if you tab to or click on a particular control that requires it.
Conversely, tabbing to or clicking on a control that does not require focus mode will switch back to browse mode.
You can also press enter or space to switch to focus mode on controls that require it.
Pressing escape will switch back to browse mode.
In addition, you can manually force focus mode, after which it will remain in effect until you choose to disable it.

| Name | Key | Description |
| --- | --- | --- |
| Toggle browse/focus modes | NVDA+space | Toggles between focus mode and browse mode |
| Exit focus mode | escape | Switches back to browse mode if focus mode was previously switched to automatically |
| Refresh browse mode document | NVDA+f5 | Reloads the current document content (useful if certain content seems to be missing from the document. Not available in Microsoft Word and Outlook.) |
| Find | NVDA+control+f | Pops up a dialog in which you can type some text to find in the current document. See [searching for text](#SearchingForText "searching for text") for more information. |
| Find next | NVDA+f3 | Finds the next occurrence of the text in the document that you previously searched for |
| Find previous | NVDA+shift+f3 | Finds the previous occurrence of the text in the document you previously searched for |

## Single Letter Navigation

While in browse mode, for quicker navigation, NVDA also provides single character keys to jump to certain fields in the document.
Note that not all of these commands are supported in every type of document.

The following keys by themselves jump to the next available element, while adding the shift key causes them to jump to the previous element:

- h: heading
- l: list
- i: list item
- t: table
- k: link
- n: nonLinked text
- f: form field
- u: unvisited link
- v: visited link
- e: edit field
- b: button
- x: checkbox
- c: combo box
- r: radio button
- q: block quote
- s: separator
- m: frame
- g: graphic
- d: landmark
- o: embedded object (audio and video player, application, dialog, etc.)
- 1 to 6: headings at levels 1 to 6 respectively
- a: annotation (comment, editor revision, etc.)
- `p`: text paragraph
- w: spelling error

To move to the beginning or end of containing elements such as lists and tables:

| Name | Key | Description |
| --- | --- | --- |
| Move to start of container | shift+comma | Moves to the start of the container (list, table, etc.) where the caret is positioned |
| Move past end of container | comma | Moves past the end of the container (list, table, etc.) where the caret is positioned |

Some web applications such as Gmail, Twitter and Facebook use single letters as shortcut keys.
If you want to use these while still being able to use your cursor keys to read in browse mode, you can temporarily disable NVDA's single letter navigation keys.

To toggle single letter navigation on and off for the current document, press NVDA+shift+space.

### Text paragraph navigation command

You can jump to the next or previous text paragraph by pressing `p` or `shift+p`.
Text paragraphs are defined by a group of text that appears to be written in complete sentences.
This can be useful to find the beginning of readable content on various webpages, such as:

- News websites
- Forums
- Blog posts

These commands can also be helpful for skipping certain kinds of clutter, such as:

- Ads
- Menus
- Headers

Please note, however, that while NVDA tries its best to identify text paragraphs, the algorithm is not perfect and at times can make mistakes.
Additionally, this command is different from paragraph navigation commands `control+downArrow/upArrow`.
Text paragraph navigation only jumps between text paragraphs, while paragraph navigation commands take the cursor to the previous/next paragraphs regardless of whether they contain text or not.

### Other navigation commands

In addition to the quick navigation commands listed above, NVDA has commands that have no default keys assigned.
To use these commands, you first need to assign gestures to them using the [Input Gestures dialog](#InputGestures "Input Gestures dialog").
Here is a list of available commands:

- Article
- Figure
- Grouping
- Tab
- Menu item
- Toggle button
- Progress bar
- Math formula
- Vertically aligned paragraph
- Same style text
- Different style text

Keep in mind that there are two commands for each type of element, for moving forward in the document and backward in the document, and you must assign gestures to both commands in order to be able to quickly navigate in both directions.
For example, if you want to use the `y` / `shift+y` keys to quickly navigate through tabs, you would do the following:

1. Open input gestures dialog from browse mode.
2. Find "moves to the next tab" item in the Browse mode section.
3. Assign `y` key for found gesture.
4. Find "moves to the previous tab" item.
5. Assign `shift+y` for found gesture.

### The Elements List

The elements list provides access to a list of various types of elements in the document as appropriate for the application.
For example, in web browsers, the elements list can list links, headings, form fields, buttons or landmarks.
Radio buttons allow you to switch between the different types of elements.
An edit field is also provided in the dialog which allows you to filter the list to help you search for a particular item on the page.
Once you have chosen an item, you can use the provided buttons in the dialog to move to or activate that item.

| Name | Key | Description |
| --- | --- | --- |
| Browse mode elements list | NVDA+f7 | Lists various types of elements in the current document |

### Searching for text

This dialog allows you to search for terms in the current document.
In the "Type the text you wish to find" field, the text to be found can be entered.
The "Case sensitive" checkbox makes the search consider uppercase and lowercase letters differently.
For example, with "Case sensitive" selected you can find "NV Access" but not "nv access".
Use the following keys for performing searches:

| Name | Key | Description |
| --- | --- | --- |
| Find text | NVDA+control+f | Opens the search dialog |
| Find next | NVDA+f3 | searches the next occurrence of the current search term |
| Find previous | NVDA+shift+f3 | searches the previous occurrence of the current search term |

### Embedded Objects

Pages can include rich content using technologies such as Oracle Java and HTML5, as well as applications and dialogs.
Where these are encountered in browse mode, NVDA will report "embedded object", "application" or "dialog", respectively.
You can quickly move to them using the o and shift+o embedded object single letter navigation keys.
To interact with these objects, you can press enter on them.
If it is accessible, you can then tab around it and interact with it like any other application.
A key command is provided to return to the original page containing the embedded object:

| Name | Key | Description |
| --- | --- | --- |
| Move to containing browse mode document | NVDA+control+space | Moves the focus out of the current embedded object and into the document that contains it |

### Native Selection Mode

By default when selecting text with the `shift+arrow` keys in Browse Mode, a selection is only made within NVDA's Browse Mode representation of the document, and not within the application itself.
This means that the selection is not visible on screen, and copying text with `control+c` will only copy NVDA's plain text representation of the content. i.e. formatting of tables, or whether something is a link will not be copied.
However, NVDA has a Native Selection Mode which can be turned on in particular Browse Mode documents (so far only Mozilla Firefox) which causes the document's native selection to follow NVDA's Browse Mode selection.

| Name | Key | Description |
| --- | --- | --- |
| Toggle Native Selection Mode on and off | `NVDA+shift+f10` | Toggles native selection mode on and off |

When Native Selection Mode is turned on, copying the selection with `control+c` will also use the application's own copy functionality, meaning that rich content will be copied to the clipboard, rather than plain text.
This means that pasting this content into a program such as Microsoft Word or Excel, formatting such as tables, or whether something is a link will be included.
Please note however that in native selection mode, some accessible labels or other information that NVDA generates in Browse Mode will not be included.
Also, although the application will try its best to match the native selection to NVDA's Browse Mode selection, it may not always be completely accurate.
However, for scenarios where you wish to copy an entire table or paragraph of rich content, this feature should prove useful.
