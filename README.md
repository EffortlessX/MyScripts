How to use the Universal Gui.

Setup:

1. Load the gui using `loadstring(game.HttpGet("https://github.com/EffortlessX/MyScripts/blob/main/UniversalGui"))()`.
2. Wait until the gui has loaded using `repeat wait() until _G.EffortlessXLoaded`.


Customization:

You can easily customize the gui with premade functions. These functions are stored in `_G.EffortlessXFunctions`.
It is recommend to define that as a variable, as it can be annoying to write that for every function you call.
Example:
```
loadstring(game.HttpGet("https://github.com/EffortlessX/MyScripts/blob/main/UniversalGui"))()
repeat wait() until _G.EffortlessXLoaded
local Functions = _G.EffortlessXFunctions
Functions.CreateRow("Toggle","This is a toggle row.")
```

All functions:

`SetMainColor(color: Color3)`
Sets the color of the main background.

`SetTopbarColor(color: Color3)`
Sets the color of the topbar background.

`SetBackgroundColor(color: Color3, compensate: Bool)`
Sets the color of the topbar and main background.
Compensate: Make the topbar background a bit lighter, and the main background a bit darker.

`SetDecorColor(color: Color3)`
Sets the color of the 'Effortless X' text and line below the topbar.

`SetTextColor(color: Color3)`
Sets the color of all text.

`SetButtonColor(color: Color3)`
Sets the color of all buttons.

`SetRowColor(color: Color3)`
Sets the color of all rows.

`SetPlaceholderColor(color: Color3)`
Sets the color of the placeholder text.

`CreateRow(type: String, description: String)`
Create a row on the gui.
Type: The type of row to add.
Description: The description of the row.

`DraggableGui(enabled: Bool)`
Changes if the gui can be dragged around.




