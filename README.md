# skCombobox - a better comboBox for LiveCode
#### A LiveCode group emulating an enhanced combobox replacement  

Current version: 0.9 ([changelog](/changelog.md))  
Code simplified and updated; appearance updated. The entire code is in the group script (potentially to convert to script widget).

### API
#### Public handlers
- _resetProps_: Command to reset all properties to default values

#### Messages
- _comboAction_ pID, pText: emitted when setting the textContent - can be handled further up the message path and passes the long id of the group and the textContent of the group.  
  
**Text content properties**  
- _textContent_: get/set the text typed or selected (string)  
- _listContent_: get/set the text displayed in the drop-down (return-delimited list)  
- _placeholderText_: get/set the placeholder/default (text; default: “Type or Select…”)  
  
**Text appearance properties**  
- _placeholderColor_: get/set the textColor of placeholder text (color; default: 180,180,180)  
- _placeholderStyle_: get/set the textStyle of the placeholder text (enum; default: italic)  
- _normalColor_: get/set the textColor of user-entered text (color; default: 66,66,66)  
- _normalStyle_: get/set the textStyle of user-entered text (enum; default: Plain)  
  
**Group properties properties**  
- _groupColor_: get/set the backgroundColor of the field/dropdown (Color; default: 255,255,255)
- _groupHiliteColor_: get/set the hilite colours for field and dropdown selections (Color; default: 173,204,250)

