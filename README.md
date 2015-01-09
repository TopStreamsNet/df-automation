# Dwarf Fortress Automation
This is Dwarf Fortress Automation repository - home of Dwarf Fortress macro's

## Releases
Releases of Dwarf Fortress Automation project: https://github.com/TopStreamsNet/df-automation/releases

## Macro Manual
Some information on Dwarf Fortress macro's can be found in [Dwarf Fortress Wiki](http://dwarffortresswiki.org/index.php/DF2014:Macros_and_Keymaps)

### HelloWorld.mak - your first Dwarf Fortress macro
Simple macro that would designate a line of length 5 left from cursor position for mining.

Create HelloWorld.mak file with following content in **<DF directory>/data/init/macros** 
**Important:** File name should match first line of macro

```
HelloWorld
        DESIGNATE_DIG
    End of group
        SELECT
    End of group
        CURSOR_LEFT
    End of group
        CURSOR_LEFT
    End of group
        CURSOR_LEFT
    End of group
        CURSOR_LEFT
    End of group
        SELECT
    End of group
End of macro
```

Now in game use Ctrl+l to bring up load macro menu:

![Load Macro Menu](https://raw.githubusercontent.com/TopStreamsNet/df-automation/master/images/load_macro.png)

Select desired macro (in this example case HelloWorld is the only macro available) and press Enter.

To run macro press Ctrl+p - notice "Play" label indicator:

![Playing Macro](https://raw.githubusercontent.com/TopStreamsNet/df-automation/master/images/load_macro.png)

