# skComboBox
LiveCode combobox replacement

## New in version 0.4: 
- changed filtering to search-as-you-type to highlight a value in the popup
- if entering text that doesn't exist in popup, an 'add' button will appear to append to popup
- remove values from the popup by right-clicking on the line to remove
- toggle popup with either enter or escape keys
- API modified to avoid direct access of custom property

## Description
A LiveCode group simulating a better combobox replacement, which features:
- search as you type to highlight a value in the popup
- New values that don't exist in popup will show an 'Add' button to append to popup
- Remove values in the popup by right-clicking on the value
- show/hide popup list with the return or escape keys
- arrow key navigation of popup list
- select a value in the popup list with the return or enter keys (or click on value)
- simple API to add list of values for popup and to clear popup.
- resize the height/width of the popup list by adjusting the dimensions of the group

## API
#### populateCombo pValueList
Populates the popup values with the return-delimited list pValueList
Equivalent to setting the text of a button "ComboBox Menu"
Example: send "populateCombo tValueList" to group "comboBox" 

#### setValue pValue
Sets the displayed/selected text 
Equivalent to setting the label of a button "ComboBox Menu"
Example: send "setValue tValue" to group "comboBox

#### getValue
Gets the displayed/selected text 
Example: send "getValue" to group "comboBox -> 'it' now contains the selected value

#### getValueList
Gets the list displayed in the popup (return delimited list
Example: send "getValueList" to group "comboBox -> 'it' now contains the selected value

#### clearCombo
clears the popup list and entry field of all values
Example: send "clearCombo" to group "comboBox"
