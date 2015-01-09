# Dwarf Fortress Automation
This is Dwarf Fortress Automation repository - home of Dwarf Fortress macro's

## Releases
Releases of Dwarf Fortress Automation project: https://github.com/TopStreamsNet/df-automation/releases

## Macro Manual
Some information on Dwarf Fortress macro's can be found in [Dwarf Fortress Wiki](http://dwarffortresswiki.org/index.php/DF2014:Macros_and_Keymaps)

### HelloWorld.mak - your first Dwarf Fortress macro
Simple macro that would designate a line of length 5 left from cursor position for mining.

Create HelloWorld.mak file with following content in **<DF directory>/data/init/macros** 

**!!!Important!!!** File name should match first line of the macro

```
HelloWorld
        DESIGNATE_DIG
        SELECT
        CURSOR_LEFT
        CURSOR_LEFT
        CURSOR_LEFT
        CURSOR_LEFT
        SELECT
End of macro
```
**Note**: There should be an empty line at the end of the macro file, or loading will fail with an error - "I/O error while loading macro"


Now in game use Ctrl+l to bring up load macro menu:

![Load Macro Menu](https://raw.githubusercontent.com/TopStreamsNet/df-automation/master/images/load_macro.png)

Select desired macro (in this example case HelloWorld is the only macro available) and press Enter.

To run the macro:

1. Switch into *Designation* menu - d
2. Place your cursor into position from where you wand macro to start
3. Press Ctrl+p - notice "Play" label indicator:

![Playing Macro](https://raw.githubusercontent.com/TopStreamsNet/df-automation/master/images/play_macro.png)

![Macro Done](https://raw.githubusercontent.com/TopStreamsNet/df-automation/master/images/done_macro.png)

### Reloading Dwarf Fortress macros on-the-fly
Dwarf Fortress uses some weird caching mechanism, so simply reloading previously loaded macro with Ctrl+l won't work. To "reload" a macro
one needs to delete existing macro, recreate it and then reload it. Here is how this can be done:

Having HelloWorld macro loaded lets say we want to modify it to designate a 5x5 area instead of 5x1. This means that original HelloWorld
macro needs to be modified to be the following:

```
HelloWorld
        DESIGNATE_DIG
        SELECT
        CURSOR_LEFT
        CURSOR_LEFT
        CURSOR_LEFT
        CURSOR_LEFT
        CURSOR_DOWN
        CURSOR_DOWN
        CURSOR_DOWN
        CURSOR_DOWN
        SELECT
End of macro
```
**Note**: There should be an empty line at the end of the macro file, or loading will fail with an error - "I/O error while loading macro"

1. Get into macro's management menu, to get there enter *Options* menu with Esc, then, using arrow keys to navigate and Enter to select, open *Key Bindings* menu and *Macros* would be the first submenu.
![Options Menu](https://raw.githubusercontent.com/TopStreamsNet/df-automation/master/images/options_menu.png)
![Key Bindings](https://raw.githubusercontent.com/TopStreamsNet/df-automation/master/images/key_bindings.png)
![Macros](https://raw.githubusercontent.com/TopStreamsNet/df-automation/master/images/macros.png)

2. Delete existing macro that to be reloaded (HelloWorld in this example) using BackSpace
**!!!WARNING!!!** Macro you are deleting is going to be also removed from **data/init/macros/** directory - so make sure that NEW content is not yet there and original is backed up if needed
![NoMacros](https://raw.githubusercontent.com/TopStreamsNet/df-automation/master/images/nomacros.png)

3. Now, before leaving the menu or doing anything else - place new content into **data/init/macros/**, then leave *Macros* menu pressing Esc and exit *Key Binding* menu saving changes
![Save and Exit](https://raw.githubusercontent.com/TopStreamsNet/df-automation/master/images/save_exit.png)

4. Exit *Options* menu by pressing Esc and load desired macro by using Ctrl+l
![ReLoad Macro Menu](https://raw.githubusercontent.com/TopStreamsNet/df-automation/master/images/load_macro.png)

5. Switch into *Designation* menu with d and run new (reloaded) macro with Ctrl+p
![ReLoad Macro Menu](https://raw.githubusercontent.com/TopStreamsNet/df-automation/master/images/result_macro.png)


