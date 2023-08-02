How to use the Universal Gui.

Setup:

1. Load the gui using `loadstring(game:HttpGet("https://raw.githubusercontent.com/EffortlessX/MyScripts/main/UniversalGui"))()`.
2. Wait until the gui has loaded using `repeat wait() until _G.EXLoaded`.


Customization:

You can easily customize the gui with premade functions. These functions are stored in `_G.EXFunctions`.
It is recommend to define that as a variable, as it can be annoying to write that for every function you call.
It is also necessary to define the function you want to be called when the row is toggled/activated. You have to
create the function in `_G.EXClient`.
Example:
```
loadstring(game:HttpGet("https://raw.githubusercontent.com/EffortlessX/MyScripts/main/UniversalGui"))()
repeat wait() until _G.EXLoaded

local Functions = _G.EXFunctions
local Client = _G.EXClient

function Client.RowClicked()
  print("Row clicked!")
end

Functions.CreateRow("Toggle",Client.RowClicked,"This is a toggle row.")
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

`DraggableGui(enabled: Bool)`
Changes if the gui can be dragged around.

`CreateRow(type: String, function: Function, description: String)`
Create a row on the gui.
Type: The type of row to add.
Function: The function to call when the row is clicked.
Description: The description of the row.

Row Types:
- Toggle (Row with a toggle button)
- Activate (Row that can be activated once)
- UserInput (Row that can receive user input)


