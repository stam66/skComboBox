# skCombobox - a better comboBox for LiveCode
#### A LiveCode group emulating an enhanced combobox replacement:
- placeholder text function to help guide user input
- search as you type to highlight a value in the popup
- New values that don’t exist in popup will show an ‘Add’ button to modify popup i
- Remove values in the popup by right-clicking on the value
- show/hide popup list with the return or escape keys
- arrow key navigation of popup list
- select a value in the popup list with the return or enter keys (or click on value)
- simple API to add list of values for popup and to clear popup.
- a handler skeleton to add action to be triggered after setting a value
- resize the height/width of  the popup list by adjusting the dimensions of the group 
  (make sure 'Select Group' is inactive or group won't resize properly!)

## API
#### - setValueList _pValueList_
Populates the popup values with the return-delimited list pValueList. 
Equivalent to setting the text of a button “ComboBox Menu”. 
_Example: dispatch “setValueList” to group “comboBox”  with tValueList_

#### - setValue _pValue_
Sets the displayed/selected text 
Equivalent to setting the label of a button “ComboBox Menu”. 
_Example: dispatch “setValue” to group “comboBox" with tValue_

#### - setPlaceholderText _pText_
Sets the placeholder text to the supplied parameter. 
_Example: dispatch “setPlaceholderText” to group “comboBox” with tText_

#### - getPlaceholderText
Get the placeholder text. 
_Example: send “getPlaceholderText” to group “comboBox —> ‘the result’ now contains the placeholder text_

#### - getValue
Gets the displayed/selected text. 
_Example: send “getValue” to group “comboBox —> ‘the result’ now contains the selected value_

#### - getValueList
Gets the list displayed in the popup (return delimited list). 
_Example: send “getValueList” to group “comboBox —> ‘the result' now contains the selected value_

#### - clearCombo
Clears the popup list and entry field of all values. 
_Example: send “clearCombo” to group “comboBox”_

#### - initState
forces popup closed when card/group containing combobox opens and display either value or the uPlaceholderText correctly. 
_Example: send "initState" to group "comboBox"_



## CHANGE LOG
#### Version 0.7
 - corrected a minor styling issue when first opening the field
 - added new command 'initState' - this forces the combobox to not display any values when the card or
   or group containing this is first openened, and displays correctly value or the uPlaceholderText
 - minor change to close popup when value selected

#### Version 0.6
 - corrected error with get functions, removed unnecessary custom properties
 - added placeholder text functionality

#### Version 0.5: 
- fixed get functions corrrectly using 'the result' instead of 'it'
- renamed populateCombo to setValueList for consistency
- added getValueList to get the current list of popup values, as user can modify these
- added doAction handler that triggers when the value of the display field is set, or exited.

#### Version 0.4: 
- changed filtering to search-as-you-type to hilight a value in the popup
- if entering text that doesn’t exist in popup, an ‘add’ button will appear to append to popup
- remove values from the popup by right-clicking on the line to remove
- toggle popup with either enter or escape keys
- API modified to avoid direct access of custom property
