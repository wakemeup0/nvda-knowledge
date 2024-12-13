# Navigating with NVDA

NVDA allows you to explore and navigate the system in several ways, including both normal interaction and review.

## Objects

Each Application and the operating system itself consist of many objects.
An object is a single item such as a piece of text, button, checkbox, slider, list or editable text field.

### Navigating with the System Focus

The system focus, also known simply as the focus, is the [object](#objects "object") which receives keys typed on the keyboard.
For example, if you are typing into an editable text field, the editable text field has the focus.

The most common way of navigating around Windows with NVDA is to simply move the system focus using standard Windows keyboard commands, such as pressing tab and shift+tab to move forward and back between controls, pressing alt to get to the menu bar and then using the arrows to navigate menus, and using alt+tab to move between running applications.
As you do this, NVDA will report information about the object with focus, such as its name, type, value, state, description, keyboard shortcut and positional information.
When [Visual Highlight](#VisionFocusHighlight "Visual Highlight") is enabled, the location of the current system focus is also exposed visually.

There are some key commands that are useful when moving with the System focus:

| Name                 | Desktop key     | Laptop key             | Description                                                                                                                                     |
| -------------------- | --------------- | ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| Report current focus | NVDA+tab        | NVDA+tab               | announces the current object or control that has the System focus. Pressing twice will spell the information                                    |
| Report title         | NVDA+t          | NVDA+t                 | Reports the title of the currently active window. Pressing twice will spell the information. Pressing three times will copy it to the clipboard |
| Read active window   | NVDA+b          | NVDA+b                 | reads all the controls in the currently active window (useful for dialogs)                                                                      |
| Report Status Bar    | NVDA+end        | NVDA+shift+end         | Reports the Status Bar if NVDA finds one. Pressing twice will spell the information. Pressing three times will copy it to the clipboard         |
| Report Shortcut Key  | `shift+numpad2` | `NVDA+control+shift+.` | Reports the shortcut (accelerator) key of the currently focused object                                                                          |

### Navigating with the System Caret

When an [object](#objects "object") that allows navigation and/or editing of text is [focused](#SystemFocus "focused"), you can move through the text using the system caret, also known as the edit cursor.

When the focus is on an object that has the system caret, you can use the arrow keys, page up, page down, home, end, etc. to move through the text.
You can also change the text if the control supports editing.
NVDA will announce as you move by character, word and line, and will also announce as you select and unselect text.

NVDA provides the following key commands in relation to the system caret:

| Name                        | Desktop key        | Laptop key    | Description                                                                                                                                                                                                                                                                        |
| --------------------------- | ------------------ | ------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Say all                     | NVDA+downArrow     | NVDA+a        | Starts reading from the current position of the system caret, moving it along as it goes                                                                                                                                                                                           |
| Read current line           | NVDA+upArrow       | NVDA+l        | Reads the line where the system caret is currently situated. Pressing twice spells the line. Pressing three times spells the line using character descriptions.                                                                                                                    |
| Read current text selection | NVDA+Shift+upArrow | NVDA+shift+s  | Reads any currently selected text                                                                                                                                                                                                                                                  |
| Report text formatting      | NVDA+f             | NVDA+f        | Reports the formatting of the text where the caret is currently situated. Pressing twice shows the information in browse mode                                                                                                                                                      |
| Report link destination     | `NVDA+k`           | `NVDA+k`      | Pressing once speaks the destination URL of the link at the current caret or focus position. Pressing twice shows it in a window for more careful review                                                                                                                           |
| Report caret location       | NVDA+numpadDelete  | NVDA+delete   | Reports information about the location of the text or object at the position of system caret. For example, this might include the percentage through the document, the distance from the edge of the page or the exact screen position. Pressing twice may provide further detail. |
| Next sentence               | alt+downArrow      | alt+downArrow | Moves the caret to the next sentence and announces it. (only supported in Microsoft Word and Outlook)                                                                                                                                                                              |
| Previous sentence           | alt+upArrow        | alt+upArrow   | Moves the caret to the previous sentence and announces it. (only supported in Microsoft Word and Outlook)                                                                                                                                                                          |

When within a table, the following key commands are also available:

| Name                    | Key                           | Description                                                                                 |
| ----------------------- | ----------------------------- | ------------------------------------------------------------------------------------------- |
| Move to previous column | control+alt+leftArrow         | Moves the system caret to the previous column (staying in the same row)                     |
| Move to next column     | control+alt+rightArrow        | Moves the system caret to the next column (staying in the same row)                         |
| Move to previous row    | control+alt+upArrow           | Moves the system caret to the previous row (staying in the same column)                     |
| Move to next row        | control+alt+downArrow         | Moves the system caret to the next row (staying in the same column)                         |
| Move to first column    | control+alt+home              | Moves the system caret to the first column (staying in the same row)                        |
| Move to last column     | control+alt+end               | Moves the system caret to the last column (staying in the same row)                         |
| Move to first row       | control+alt+pageUp            | Moves the system caret to the first row (staying in the same column)                        |
| Move to last row        | control+alt+pageDown          | Moves the system caret to the last row (staying in the same column)                         |
| Say all in column       | `NVDA+control+alt+downArrow`  | Reads the column vertically from the current cell downwards to the last cell in the column. |
| Say all in row          | `NVDA+control+alt+rightArrow` | Reads the row horizontally from the current cell rightwards to the last cell in the row.    |
| Read entire column      | `NVDA+control+alt+upArrow`    | Reads the current column vertically from top to bottom without moving the system caret.     |
| Read entire row         | `NVDA+control+alt+leftArrow`  | Reads the current row horizontally from left to right without moving the system caret.      |

### Object Navigation

Most of the time, you will work with applications using commands which move the [focus](#SystemFocus "focus") and the [caret](#SystemCaret "caret").
However, sometimes, you may wish to explore the current application or the Operating System without moving the focus or caret.
You may also wish to work with [objects](#objects "objects") that cannot be accessed normally using the keyboard.
In these cases, you can use object navigation.

Object navigation allows you to move between and obtain information about individual [objects](#objects "objects").
When you move to an object, NVDA will report it similarly to the way it reports the system focus.
For a way to review all text as it appears on the screen, you can instead use [screen review](#ScreenReview "screen review").

Rather than having to move back and forth between every single object on the system, the objects are organized hierarchically.
This means that some objects contain other objects and you must move inside them to access the objects they contain.
For example, a list contains list items, so you must move inside the list in order to access its items.
If you have moved to a list item, moving next and previous will take you to other list items in the same list.
Moving to a list item's containing object will take you back to the list.
You can then move past the list if you wish to access other objects.
Similarly, a toolbar contains controls, so you must move inside the toolbar to access the controls in the toolbar.

If you yet prefer to move back and forth between every single object on the system, you can use commands to move to the previous/next object in a flattened view.
For example, if you move to the next object in this flattened view and the current object contains other objects, NVDA will automatically move to the first object that it contains.
Alternatively, if the current object doesn't contain any objects, NVDA will move to the next object at the current level of the hierarchy.
If there is no such next object, NVDA will try to find the next object in the hierarchy based on containing objects until there are no more objects to move to.
The same rules apply to moving backwards in the hierarchy.

The object currently being reviewed is called the navigator object.
Once you navigate to an object, you can review its content using the [text review commands](#ReviewingText "text review commands") while in [Object review mode](#ObjectReview "Object review mode").
When [Visual Highlight](#VisionFocusHighlight "Visual Highlight") is enabled, the location of the current navigator object is also exposed visually.
By default, the navigator object moves along with the System focus, though this behaviour can be toggled on and off.

Note: Braille following Object Navigation can be configured via [Braille Tether](#BrailleTether "Braille Tether").

To navigate by object, use the following commands:

| Name                                                  | Desktop key             | Laptop key            | Touch                     | Description                                                                                                                                                                                                                                                             |
| ----------------------------------------------------- | ----------------------- | --------------------- | ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --- |
| Report current object                                 | NVDA+numpad5            | NVDA+shift+o          | none                      | Reports the current navigator object. Pressing twice spells the information, and pressing 3 times copies this object's name and value to the clipboard.                                                                                                                 |
| Move to containing object                             | NVDA+numpad8            | NVDA+shift+upArrow    | flick up (object mode)    | Moves to the object containing the current navigator object                                                                                                                                                                                                             |
| Move to previous object                               | NVDA+numpad4            | NVDA+shift+leftArrow  | none                      | Moves to the object before the current navigator object                                                                                                                                                                                                                 |
| Move to previous object in flattened view             | NVDA+numpad9            | NVDA+shift+\[         | flick left (object mode)  | Moves to the previous object in a flattened view of the object navigation hierarchy                                                                                                                                                                                     | \   |
| Move to next object                                   | NVDA+numpad6            | NVDA+shift+rightArrow | none                      | Moves to the object after the current navigator object                                                                                                                                                                                                                  | \   |
| Move to next object in flattened view                 | NVDA+numpad3            | NVDA+shift+\]         | flick right (object mode) | Moves to the next object in a flattened view of the object navigation hierarchy                                                                                                                                                                                         |
| Move to first contained object                        | NVDA+numpad2            | NVDA+shift+downArrow  | flick down (object mode)  | Moves to the first object contained by the current navigator object                                                                                                                                                                                                     |
| Move to focus object                                  | NVDA+numpadMinus        | NVDA+backspace        | none                      | Moves to the object that currently has the system focus, and also places the review cursor at the position of the System caret, if it is showing                                                                                                                        |
| Activate current navigator object                     | NVDA+numpadEnter        | NVDA+enter            | double-tap                | Activates the current navigator object (similar to clicking with the mouse or pressing space when it has the system focus)                                                                                                                                              |
| Move System focus or caret to current review position | NVDA+shift+numpadMinus  | NVDA+shift+backspace  | none                      | pressed once Moves the System focus to the current navigator object, pressed twice moves the system caret to the position of the review cursor                                                                                                                          |
| Report review cursor location                         | NVDA+shift+numpadDelete | NVDA+shift+delete     | none                      | Reports information about the location of the text or object at the review cursor. For example, this might include the percentage through the document, the distance from the edge of the page or the exact screen position. Pressing twice may provide further detail. |
| Move review cursor to status bar                      | none                    | none                  | none                      | Reports the Status Bar if NVDA finds one. It also moves the navigator object to this location.                                                                                                                                                                          |

Note: numpad keys require the Num Lock to be turned off to work properly.

### Reviewing Text

NVDA allows you to read the contents of the [screen](#ScreenReview "screen"), current [document](#DocumentReview "document") or current [object](#ObjectReview "object") by character, word or line.
This is mostly useful in places (including Windows command consoles) where there is no [system caret](#SystemCaret "system caret").
For example, you might use it to review the text of a long information message in a dialog.

When moving the review cursor, the System caret does not follow along, so you can review text without losing your editing position.
However, by default, when the System caret moves, the review cursor follows along.
This can be toggled on and off.

Note: Braille following the review cursor can be configured via [Braille Tether](#BrailleTether "Braille Tether").

The following commands are available for reviewing text:

| Name                                    | Desktop key     | Laptop key              | Touch                            | Description                                                                                                                                                                                                                                                                                                                   |
| --------------------------------------- | --------------- | ----------------------- | -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Move to top line in review              | shift+numpad7   | NVDA+control+home       | none                             | Moves the review cursor to the top line of the text                                                                                                                                                                                                                                                                           |
| Move to previous line in review         | numpad7         | NVDA+upArrow            | flick up (text mode)             | Moves the review cursor to the previous line of text                                                                                                                                                                                                                                                                          |
| Report current line in review           | numpad8         | NVDA+shift+.            | none                             | Announces the current line of text where the review cursor is positioned. Pressing twice spells the line. Pressing three times spells the line using character descriptions.                                                                                                                                                  |
| Move to next line in review             | numpad9         | NVDA+downArrow          | flick down (text mode)           | Move the review cursor to the next line of text                                                                                                                                                                                                                                                                               |
| Move to bottom line in review           | shift+numpad9   | NVDA+control+end        | none                             | Moves the review cursor to the bottom line of text                                                                                                                                                                                                                                                                            |
| Move to previous word in review         | numpad4         | NVDA+control+leftArrow  | 2-finger flick left (text mode)  | Moves the review cursor to the previous word in the text                                                                                                                                                                                                                                                                      |
| Report current word in review           | numpad5         | NVDA+control+.          | none                             | Announces the current word in the text where the review cursor is positioned. Pressing twice spells the word. Pressing three times spells the word using character descriptions.                                                                                                                                              |
| Move to next word in review             | numpad6         | NVDA+control+rightArrow | 2-finger flick right (text mode) | Move the review cursor to the next word in the text                                                                                                                                                                                                                                                                           |
| Move to start of line in review         | shift+numpad1   | NVDA+home               | none                             | Moves the review cursor to the start of the current line in the text                                                                                                                                                                                                                                                          |
| Move to previous character in review    | numpad1         | NVDA+leftArrow          | flick left (text mode)           | Moves the review cursor to the previous character on the current line in the text                                                                                                                                                                                                                                             |
| Report current character in review      | numpad2         | NVDA+.                  | none                             | Announces the current character on the line of text where the review cursor is positioned. Pressing twice reports a description or example of that character. Pressing three times reports the numeric value of the character in decimal and hexadecimal.                                                                     |
| Move to next character in review        | numpad3         | NVDA+rightArrow         | flick right (text mode)          | Move the review cursor to the next character on the current line of text                                                                                                                                                                                                                                                      |
| Move to end of line in review           | shift+numpad3   | NVDA+end                | none                             | Moves the review cursor to the end of the current line of text                                                                                                                                                                                                                                                                |
| Move to previous page in review         | `NVDA+pageUp`   | `NVDA+shift+pageUp`     | none                             | Moves the review cursor to the previous page of text if supported by the application                                                                                                                                                                                                                                          |
| Move to next page in review             | `NVDA+pageDown` | `NVDA+shift+pageDown`   | none                             | Moves the review cursor to the next page of text if supported by the application                                                                                                                                                                                                                                              |
| Say all with review                     | numpadPlus      | NVDA+shift+a            | 3-finger flick down (text mode)  | Reads from the current position of the review cursor, moving it as it goes                                                                                                                                                                                                                                                    |
| Select then Copy from review cursor     | NVDA+f9         | NVDA+f9                 | none                             | Starts the select then copy process from the current position of the review cursor. The actual action is not performed until you tell NVDA where the end of the text range is                                                                                                                                                 |
| Select then Copy to review cursor       | NVDA+f10        | NVDA+f10                | none                             | On the first press, text is selected from the position previously set as start marker up to and including the review cursor's current position. If the system caret can reach the text, it will be moved to the selected text. After pressing this key stroke a second time, the text will be copied to the Windows clipboard |
| Move to marked start for copy in review | NVDA+shift+f9   | NVDA+shift+f9           | none                             | Moves the review cursor to the position previously set start marker for copy                                                                                                                                                                                                                                                  |
| Report text formatting                  | NVDA+shift+f    | NVDA+shift+f            | none                             | Reports the formatting of the text where the review cursor is currently situated. Pressing twice shows the information in browse mode                                                                                                                                                                                         |
| Report current symbol replacement       | None            | None                    | none                             | Speaks the symbol where the review cursor is positioned. Pressed twice, shows the symbol and the text used to speak it in browse mode.                                                                                                                                                                                        |

Note: numpad keys require the Num Lock to be turned off to work properly.

A good way to remember the basic text review commands when using the Desktop layout is to think of them as being in a grid of three by three, with top to bottom being line, word and character and left to right being previous, current and next.
The layout is illustrated as follows:

| .                  | .                 | .              |
| ------------------ | ----------------- | -------------- |
| Previous line      | Current line      | Next line      |
| Previous word      | Current word      | Next word      |
| Previous character | Current character | Next character |

### Review Modes

NVDA's [text review commands](#ReviewingText "text review commands") can review content within the current navigator object, current document or screen, depending on the review mode selected.

The following commands switch between review modes:

| Name                           | Desktop key  | Laptop key    | Touch               | Description                                    |
| ------------------------------ | ------------ | ------------- | ------------------- | ---------------------------------------------- |
| Switch to next review mode     | NVDA+numpad7 | NVDA+pageUp   | 2-finger flick up   | switches to the next available review mode     |
| Switch to previous review mode | NVDA+numpad1 | NVDA+pageDown | 2-finger flick down | switches to the previous available review mode |

#### Object Review

While in object review mode, you are able to only review the content of the current [navigator object](#ObjectNavigation "navigator object").
For objects such as editable text fields or other basic text controls, this will generally be the text content.
For other objects, this may be the name and/or value.

#### Document Review

When the [navigator object](#ObjectNavigation "navigator object") is within a browse mode document (e.g. web page) or other complex document (e.g. a Lotus Symphony document), it is possible to switch to the document review mode.
The document review mode allows you to review the text of the entire document.

When switching from object review to document review, the review cursor is placed in the document at the position of the navigator object.
When moving around the document with review commands, the navigator object is automatically updated to the object found at the current review cursor position.

Note that NVDA will switch to document review from object review automatically when moving around browse mode documents.

#### Screen Review

The screen review mode allows you to review the text of the screen as it appears visually within the current application.
This is similar to the screen review or mouse cursor functionality in many other Windows screen readers.

When switching to screen review mode, the review cursor is placed at the screen position of the current [navigator object](#ObjectNavigation "navigator object").
When moving around the screen with review commands, the navigator object is automatically updated to the object found at the screen position of the review cursor.

Note that in some newer applications, NVDA may not see some or all text displayed on the screen due to the use of newer screen drawing technologies which are impossible to support at this time.

### Navigating with the Mouse

When you move the mouse, NVDA by default reports the text that is directly under the mouse pointer as the pointer moves over it.
Where supported, NVDA will read the surrounding paragraph of text, though some controls may only read by line.

NVDA can be configured to also announce the type of [object](#objects "object") under the mouse as it moves (e.g. list, button, etc.).
This may be useful for totally blind users, as sometimes, the text isn't enough.

NVDA provides a way for users to understand where the mouse is located relative to the dimensions of the screen by playing the current mouse coordinates as audio beeps.
The higher the mouse is on the screen, the higher the pitch of the beeps.
The further left or right the mouse is located on the screen, the further left or right the sound will be played (assuming the user has stereo speakers or headphones).

These extra mouse features are not turned on by default in NVDA.
If you wish to take advantage of them, you can configure them from the [Mouse settings](#MouseSettings "Mouse settings") category of the [NVDA Settings](#NVDASettings "NVDA Settings") dialog, found in the NVDA Preferences menu.

Although a physical mouse or trackpad should be used to navigate with the mouse, NVDA provides some commands related to the mouse:

| Name                                   | Desktop key          | Laptop key      | Touch        | Description                                                                                                                                                                                                            |
| -------------------------------------- | -------------------- | --------------- | ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --- |
| Left mouse button click                | numpadDivide         | NVDA+\[         | none         | Clicks the left mouse button once. The common double click can be performed by pressing this key twice in quick succession                                                                                             | \   |
| Left mouse button lock                 | shift+numpadDivide   | NVDA+control+\[ | none         | Locks the left mouse button down. Press again to release it. To drag the mouse, press this key to lock the left button down and then move the mouse either physically or use one of the other mouse routing commands   | \   |
| Right mouse click                      | numpadMultiply       | NVDA+\]         | tap and hold | Clicks the right mouse button once, mostly used to open context menu at the location of the mouse.                                                                                                                     | \   |
| Right mouse button lock                | shift+numpadMultiply | NVDA+control+\] | none         | Locks the right mouse button down. Press again to release it. To drag the mouse, press this key to lock the right button down and then move the mouse either physically or use one of the other mouse routing commands |
| Scroll up at the mouse position        | none                 | none            | none         | Scrolls the mouse wheel up at the current mouse position                                                                                                                                                               |
| Scroll down at the mouse position      | none                 | none            | none         | Scrolls the mouse wheel down at the current mouse position                                                                                                                                                             |
| Scroll left at the mouse position      | none                 | none            | none         | Scrolls the mouse wheel left at the current mouse position                                                                                                                                                             |
| Scroll right at the mouse position     | none                 | none            | none         | Scrolls the mouse wheel right at the current mouse position                                                                                                                                                            |
| Move mouse to current navigator object | NVDA+numpadDivide    | NVDA+shift+m    | none         | Moves the mouse to the location of the current navigator object and review cursor                                                                                                                                      |
| Navigate to the object under the mouse | NVDA+numpadMultiply  | NVDA+shift+n    | none         | Set the navigator object to the object located at the position of the mouse                                                                                                                                            |
