# skCombobox - a better comboBox for LiveCode
#### A LiveCode group control for an enhanced combobox control
Current version: 0.96.4 ([changelog](/changelog.md))  
  
### Features
- Placeholder text function to help guide user input
- Search as you type to highlight a value in the popup
- Show/hide popup list with the return or escape keys
- Arrow key navigation of popup list
- Select a value in the popup list with the return or enter keys (or click on value)
- Get/Set the textContent, listContent, placeholderText. Properteis with getters/setters listed below
- On setting text content, a "comboAction" message is emitted to pass the long id of the group and its text
- Reiszing when collapsed resizes with of the widget and the height of the field (not restricted to default/OS height)
- Resizing when expanded resizes the width of the widgt and the height of the dropdown. Dropdown will remain visible when switching to pointer tool if the mouse within the rect of the group or if optionKey is down.
  
### Usage
Stack intended as plugin. Drag & drop or double-click to place on a topLevel stack.  
Selecting a placed group allows editing of properties in the plugin/controller stack.  
skComboBox | Controller when no selection | When an skComboBox is selected
:--- | :--- | ---
<img width="212" alt="skComboBox" src="https://github.com/stam66/skComboBox/assets/5677273/b6f28b4a-94a0-429b-9f9d-e921583c473e"> | <img width="250" alt="Screenshot 2024-03-31 at 11 11 14" src="https://github.com/stam66/skComboBox/assets/5677273/407bdc30-ee1f-4461-8b93-8ad44265ffe7"> | <img width="250" alt="Screenshot 2024-03-31 at 11 11 21" src="https://github.com/stam66/skComboBox/assets/5677273/6ba5ea52-075a-4c5a-a47d-cd37ab9de32f">


  
### API
#### Public handlers
- _resetProps_: Command to reset all properties to default values

#### Messages
- _comboAction pID, pText_: emitted when setting the textContent - can be handled further up the message path (eg parent, card or stack) and passes the long id of the group and the textContent of the group.  
  
**Text content properties**  
- _textContent_: get/set the text typed or selected (string)  
- _listContent_: get/set the text displayed in the drop-down (return-delimited list)  
- _placeholderText_: get/set the placeholder/default (text; default: “Type or Select…”)  
  
**Text appearance properties**  
- _placeholderColor_: get/set the textColor of placeholder text (color; default: 180,180,180)  
- _placeholderStyle_: get/set the textStyle of the placeholder text (enum; default: italic)  
- _normalColor_: get/set the textColor of user-entered text (color; default: 66,66,66)  
- _normalStyle_: get/set the textStyle of user-entered text (enum; default: Plain)  
- _fieldTextSize_: get/set textSize of entry field; the dropdown size is 1 point smaller (default: 13 points)

**Group properties properties**  
- _groupColor_: get/set the backgroundColor of the field/dropdown (Color; default: 255,255,255)
- _groupHiliteColor_: get/set the hilite colours for field and dropdown selections (Color; default: 173,204,250)

