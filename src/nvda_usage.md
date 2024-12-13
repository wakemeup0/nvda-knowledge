# Using NVDA

## Launching NVDA

If you have installed NVDA with the installer, then starting NVDA is as simple as either pressing control+alt+n, or choosing NVDA from the NVDA menu under Programs on the Start Menu.
Additionally you can type NVDA into the Run dialog and press Enter.
If NVDA is already running, it will be restarted.
You can also pass some command line options which allows you to quit (-q), disable add-ons (--disable-addons), etc.

For installed copies, NVDA stores the configuration in the roaming application data folder of the current user by default (e.g. "`C:\Users\<user>\AppData\Roaming`").
It is possible to change this in a way that NVDA loads its configuration from the local application data folder instead.
Consult the section about system wide parameters for more details.

### Starting the Portable Version

To start the portable version, go to the directory you unpacked NVDA to, and press enter or double click on nvda.exe.
If NVDA was already running, it will automatically stop before starting the portable version.

### Initial Startup

As NVDA starts, you will first hear an ascending set of tones (telling you that NVDA is loading).
Depending on how fast your computer is, or if you are running NVDA off a USB key or other slow media, it may take a little while to start.
If it is taking an extra-long time to start, NVDA should say "Loading NVDA. Please wait..."

If you don't hear any of this, or you hear the Windows error sound, or a descending set of tones, then this means that NVDA has an error, and you will need to possibly report a bug to the developers.
Please check out the NVDA website for how to do this.

### Welcome Dialog

When NVDA starts for the first time, you will be greeted by a dialog box which provides you with some basic information about the NVDA modifier key and the NVDA menu.
The dialog box also contains a combo box and three checkboxes:
- The combo box lets you select the keyboard layout
- The first checkbox lets you control if NVDA should use the Caps Lock as an NVDA modifier key
- The second specifies whether NVDA should start automatically after you log on to Windows (only available for installed copies)
- The third lets you control if this Welcome dialog should appear each time NVDA starts

### Data Usage Statistics Dialog

When starting NVDA for the first time, a dialog will appear asking if you want to accept sending data to NV Access while using NVDA, to help improve NVDA in the future.
You can read more info about the data gathered by NV Access in the general settings section.
Note: pressing "yes" or "no" will save this setting and the dialog will never appear again unless you reinstall NVDA.
However, you can enable or disable the data gathering process manually in NVDA's general settings panel.

## NVDA Keyboard Commands

### The NVDA Modifier Key

Most NVDA-specific keyboard commands consist of pressing a particular key called the NVDA modifier key in conjunction with one or more other keys.
Notable exceptions to this are the text review commands for the desktop keyboard layout which just use the numpad keys by themselves, but there are some other exceptions as well.

NVDA can be configured so that the `insert`, `numpadInsert`, and/or `capsLock` key can be used as the `NVDA` modifier key.
By default, both the `insert` and `numpadInsert` keys are set as NVDA modifier keys.

If you wish to cause one of the NVDA modifier keys to behave as it usually would if NVDA were not running (e.g. you wish to turn Caps Lock on when you have set Caps Lock to be an NVDA modifier key), you can press the key twice in quick succession.

#### Keyboard Layouts

NVDA currently comes with two sets of key commands (known as keyboard layouts): the desktop layout and the laptop layout.
By default, NVDA is set to use the Desktop layout, though you can switch to the Laptop layout in the Keyboard category of the [NVDA Settings](#NVDASettings "NVDA Settings") dialog, found under Preferences in the NVDA menu.

The Desktop layout makes heavy use of the numpad (with Num Lock off).
Although most laptops do not have a physical numpad, some laptops can emulate one by holding down the FN key and pressing letters and numbers on the right-hand side of the keyboard (7, 8, 9, u, i, o, j, k, l, etc.).
If your laptop cannot do this or does not allow you to turn Num Lock off, you may want to switch to the Laptop layout instead.

### NVDA Touch Gestures

If you are running NVDA on a device with a touchscreen, you can also control NVDA directly via touch commands.
While NVDA is running, unless touch interaction support is disabled, all touch input will go directly to NVDA.
Therefore, actions that can be performed normally without NVDA will not work.

To toggle touch interaction support, press NVDA+control+alt+t.

You can also enable or disable [touch interaction support](#TouchSupportEnable "touch interaction support") from the Touch Interaction category of the NVDA settings.

#### Exploring the Screen

The most basic action you can perform with the touch screen is to announce the control or text at any point on the screen.
To do this, place one finger anywhere on the screen.
You can also keep your finger on the screen and move it around to read other controls and text that your finger moves over.

#### Touch Gestures

When NVDA commands are described later in this user guide, they may list a touch gesture which can be used to activate that command with the touchscreen.
Following are some instructions on how to perform the various touch gestures.

##### Taps

Tap the screen quickly with one or more fingers.

Tapping once with one finger is simply known as a tap.
Tapping with 2 fingers at the same time is a 2-finger tap and so on.

If the same tap is performed one or more times again in quick succession, NVDA will instead treat this as a multi-tap gesture.
Tapping twice will result in a double-tap.
Tapping 3 times will result in a triple-tap and so on.
Of course, these multi-tap gestures also recognize how many fingers were used, so it's possible to have gestures like a 2-finger triple-tap, a 4-finger tap, etc.

##### Flicks

Quickly swipe your finger across the screen.

There are 4 possible flick gestures depending on the direction: flick left, flick right, flick up and flick down.

Just like taps, more than one finger can be used to perform the gesture.
Therefore, gestures such as 2-finger flick up and 4-finger flick left are all possible.

#### Touch Modes

As there are many more NVDA commands than possible touch gestures, NVDA has several touch modes you can switch between which make certain subsets of commands available.
The two modes are text mode and object mode.
Certain NVDA commands listed in this document may have a touch mode listed in brackets after the touch gesture.
For example, flick up (text mode) means that the command will be performed if you flick up, but only while in text mode.
If the command does not have a mode listed, it will work in any mode.

To toggle touch modes, perform a 3-finger tap.

#### Touch keyboard

The touch keyboard is used to enter text and commands from a touchscreen.
When focused on an edit field, you can bring up the touch keyboard by double-tapping the touch keyboard icon on the bottom of the screen.
For tablets such as Microsoft Surface Pro, the touch keyboard is always available when the keyboard is undocked.
To dismiss the touch keyboard, double-tap the touch keyboard icon or move away from the edit field.

While the touch keyboard is active, to locate keys on the touch keyboard, move your finger to where the touch keyboard is located (typically at the bottom of the screen), then move around the keyboard with one finger.
When you find the key you wish to press, double-tap the key or lift your finger, depending on options chosen from the [Touch Interaction Settings category](#TouchInteraction "Touch Interaction Settings category") of the NVDA Settings.

### Input Help Mode

Many NVDA commands are mentioned throughout the rest of this user guide, but an easy way to explore all the different commands is to turn on input help.

To turn on input help, press NVDA+1.
To turn it off, press NVDA+1 again.
While in input help, performing any input gesture (such as pressing a key or performing a touch gesture) will report the action and describe what it does (if anything).
The actual commands will not execute while in input help mode.

### The NVDA menu

The NVDA menu allows you to control NVDA's settings, access help, save/revert your configuration, Modify speech dictionaries, access additional tools and exit NVDA.

To get to the NVDA menu from anywhere in Windows while NVDA is running, you may do any of the following:

- press `NVDA+n` on the keyboard.
- Perform a 2-finger double-tap on the touch screen.
- Access the system tray by pressing `Windows+b`, `downArrow` to the NVDA icon, and press `enter`.
- Alternatively, access the system tray by pressing `Windows+b`, `downArrow` to the NVDA icon, and open the context menu by pressing the `applications` key located next to the right control key on most keyboards.
  On a keyboard without an `applications` key, press `shift+f10` instead.
- Right-click on the NVDA icon located in the Windows system tray

When the menu comes up, You can use the arrow keys to navigate the menu, and the `enter` key to activate an item.

### Basic NVDA commands

| Name                                     | Desktop key   | Laptop key    | Touch               | Description                                                                                                                                                                                                                                                                                                               |
| ---------------------------------------- | ------------- | ------------- | ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Starts or restarts NVDA                  | Control+alt+n | Control+alt+n | none                | Starts or restarts NVDA from the Desktop, if this Windows shortcut is enabled during NVDA's installation process. This is a Windows specific shortcut and therefore it cannot be reassigned in the input gestures dialog.                                                                                                 |
| Stop speech                              | Control       | control       | 2-finger tap        | Instantly stops speaking                                                                                                                                                                                                                                                                                                  |
| Pause Speech                             | shift         | shift         | none                | Instantly pauses speech. Pressing it again will continue speaking where it left off (if pausing is supported by the current synthesizer)                                                                                                                                                                                  |
| NVDA Menu                                | NVDA+n        | NVDA+n        | 2-finger double-tap | Pops up the NVDA menu to allow you to access preferences, tools, help, etc.                                                                                                                                                                                                                                               |
| Toggle Input Help Mode                   | NVDA+1        | NVDA+1        | none                | Pressing any key in this mode will report the key, and the description of any NVDA command associated with it                                                                                                                                                                                                             |
| Quit NVDA                                | NVDA+q        | NVDA+q        | none                | Exits NVDA                                                                                                                                                                                                                                                                                                                |
| Pass next key through                    | NVDA+f2       | NVDA+f2       | none                | Tells NVDA to pass the next key press straight through to the active application - even if it is normally treated as an NVDA key command                                                                                                                                                                                  |
| Toggle application sleep mode on and off | NVDA+shift+s  | NVDA+shift+z  | none                | sleep mode disables all NVDA commands and speech/braille output for the current application. This is most useful in applications that provide their own speech or screen reading features. Press this command again to disable sleep mode - note that NVDA will only retain the Sleep Mode setting until it is restarted. |

### Reporting System Information

| Name                  | key          | Description                                                                                  |
| --------------------- | ------------ | -------------------------------------------------------------------------------------------- |
| Report date/time      | NVDA+f12     | Pressing once reports the current time, pressing twice reports the date                      |
| Report battery status | NVDA+shift+b | Reports the battery status i.e. whether AC power is in use or the current charge percentage. |
| Report clipboard text | NVDA+c       | Reports the Text on the clipboard if there is any.                                           |

### Speech modes

The speech mode governs how screen content, notifications, responses to commands, and other output is spoken during operation of NVDA.
The default mode is "talk", which speaks in situations that are expected when using a screen reader.
However, under certain circumstances, or when running particular programs, you may find one of the other speech modes valuable.

The four available speech modes are:

- Talk (Default): NVDA will speak normally in reaction to screen changes, notifications, and actions such as moving the focus, or issuing commands.
- On-demand: NVDA will only speak when you use commands with a reporting function (e.g. report the title of the window); but it will not speak in reaction to actions such as moving the focus or the cursor.
- Off: NVDA will not speak anything, however unlike sleep mode, it will silently react to commands.
- Beeps: NVDA will replace normal speech with short beeps.

The Beeps mode may be useful when some very verbose output is scrolling in a terminal window, but you don't care what it is, only that it is continuing to scroll; or in other circumstances when the fact that there is output is more relevant than the output itself.

The On-demand mode may be valuable when you don't need constant feedback about what is happening on screen or on the computer, but you periodically need to check particular things using review commands, etc.
Examples include while recording audio, when using screen magnification, during a meeting or a call, or as an alternative to beeps mode.

A gesture allows cycling through the various speech modes:

| Name              | Key      | Description                  |
| ----------------- | -------- | ---------------------------- |
| Cycle Speech Mode | `NVDA+s` | Cycles between speech modes. |

If you only need to switch between a limited subset of speech modes, see [Modes available in the Cycle speech mode command](#SpeechModesDisabling "Modes available in the Cycle speech mode command") for a way to disable unwanted modes.
